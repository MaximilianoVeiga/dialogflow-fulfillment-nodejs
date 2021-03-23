<a name="Context"></a>

## Context
This is the class that handles Dialogflow's contexts for the WebhookClient class

**Kind**: global class  

* [Context](#Context)
    * [new Context(inputContexts, session)](#new_Context_new)
    * [.contexts](#Context+contexts) : <code>object</code>
    * [.set(name, [lifespan], [params])](#Context+set)
    * [.get(name)](#Context+get) ⇒ <code>Object</code> \| <code>null</code>
    * [.delete(name)](#Context+delete)
    * [.getV1OutputContextsArray()](#Context+getV1OutputContextsArray) ⇒ <code>Array.&lt;Object&gt;</code>
    * [.getV2OutputContextsArray()](#Context+getV2OutputContextsArray) ⇒ <code>Array.&lt;Object&gt;</code>

<a name="new_Context_new"></a>

### new Context(inputContexts, session)
Constructor for Context objectTo be used in by Dialogflow's webhook client classcontext objects take are formatted as follows:  { "context-name": {       "lifespan": 5,       "parameters": {         "param": "value"       }    }  }


| Param | Type | Description |
| --- | --- | --- |
| inputContexts | <code>Object</code> | input contexts of a v1 or v2 webhook request |
| session | <code>string</code> | for a v2 webhook request & response |

**Example**  
```js
const context = new Context(inputContexts);context.get('name of context')context.set('another context name', 5, {param: 'value'})context.delete('name of context') // set context lifespan to 0
```
<a name="Context+contexts"></a>

### context.contexts : <code>object</code>
Dialogflow contexts included in the request or empty object if no valuehttps://dialogflow.com/docs/contexts

**Kind**: instance property of [<code>Context</code>](#Context)  
<a name="Context+set"></a>

### context.set(name, [lifespan], [params])
Set a new Dialogflow outgoing context: https://dialogflow.com/docs/contexts

**Kind**: instance method of [<code>Context</code>](#Context)  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| name | <code>string</code> \| <code>Object</code> |  | of context or an object representing a context |
| [lifespan] | <code>number</code> | <code>5</code> | lifespan of context, number with a value of 0 or greater |
| [params] | <code>Object</code> |  | parameters of context (can be arbitrary key-value pairs) |

**Example**  
```js
const { WebhookClient } = require('dialogflow-webhook');const agent = new WebhookClient({request: request, response: response});agent.context.set('sample context name');const context = {'name': 'weather', 'lifespan': 2, 'parameters': {'city': 'Rome'}};
```
<a name="Context+get"></a>

### context.get(name) ⇒ <code>Object</code> \| <code>null</code>
Get an context from the Dialogflow webhook request: https://dialogflow.com/docs/contexts

**Kind**: instance method of [<code>Context</code>](#Context)  
**Returns**: <code>Object</code> \| <code>null</code> - context object with lifespan and parameters (if defined) or null  

| Param | Type | Description |
| --- | --- | --- |
| name | <code>string</code> | of an context present in the Dialogflow webhook request |

**Example**  
```js
const { WebhookClient } = require('dialogflow-webhook');const agent = new WebhookClient({request: request, response: response});let context = agent.context.get('sample context name');
```
<a name="Context+delete"></a>

### context.delete(name)
Delete an context a Dialogflow session (set the lifespan to 0)

**Kind**: instance method of [<code>Context</code>](#Context)  
**Access**: public  

| Param | Type | Description |
| --- | --- | --- |
| name | <code>string</code> | of context to be deleted |

**Example**  
```js
const { WebhookClient } = require('dialogflow-webhook');const agent = new WebhookClient({request: request, response: response});agent.context.delete('no-longer-relevant-context-name');
```
<a name="Context+getV1OutputContextsArray"></a>

### context.getV1OutputContextsArray() ⇒ <code>Array.&lt;Object&gt;</code>
Get array of context objects formatted for v1 webhook response

**Kind**: instance method of [<code>Context</code>](#Context)  
**Returns**: <code>Array.&lt;Object&gt;</code> - array of v1 context objects for webhook response  
<a name="Context+getV2OutputContextsArray"></a>

### context.getV2OutputContextsArray() ⇒ <code>Array.&lt;Object&gt;</code>
Get array of context objects formatted for v2 webhook response

**Kind**: instance method of [<code>Context</code>](#Context)  
**Returns**: <code>Array.&lt;Object&gt;</code> - array of v2 context objects for webhook response  
