<a name="RichResponse"></a>

## RichResponse
Class representing a rich responseThese classes construct v1&v2 message objects for Dialogflowv1 Message object docs:https://dialogflow.com/docs/reference/agent/message-objectsv2 Message object docs:https://dialogflow.com/docs/reference/api-v2/rest/v2beta1/projects.agent.intents#Message

**Kind**: global class  
<a name="RichResponse+setPlatform"></a>

### richResponse.setPlatform(platform) ⇒ [<code>RichResponse</code>](#RichResponse)
Set the platform for a specific RichResponse (optional)

**Kind**: instance method of [<code>RichResponse</code>](#RichResponse)  

| Param | Type | Description |
| --- | --- | --- |
| platform | <code>string</code> | representing desired rich response target platform |

**Example**  
```js
let richResponse = new RichResponse();richResponse.setPlatform(PLATFORMS.ACTIONS_ON_GOOGLE)
```
<a name="Card"></a>

## Card ⇐ [<code>RichResponse</code>](#RichResponse)
Class representing a card response

**Kind**: global class  
**Extends**: [<code>RichResponse</code>](#RichResponse)  

* [Card](#Card) ⇐ [<code>RichResponse</code>](#RichResponse)
    * [new Card(card)](#new_Card_new)
    * [.setTitle(title)](#Card+setTitle) ⇒ [<code>Card</code>](#Card)
    * [.setText(text)](#Card+setText) ⇒ [<code>Card</code>](#Card)
    * [.setImage(imageUrl)](#Card+setImage) ⇒ [<code>Card</code>](#Card)
    * [.setButton(button)](#Card+setButton) ⇒ [<code>Card</code>](#Card)
    * [.setPlatform(platform)](#RichResponse+setPlatform) ⇒ [<code>RichResponse</code>](#RichResponse)

<a name="new_Card_new"></a>

### new Card(card)
Constructor for Card object.


| Param | Type | Description |
| --- | --- | --- |
| card | <code>string</code> \| <code>Object</code> | response title string or an object representing a card response |

**Example**  
```js
let card = new Card('card title');card.setImage('https://developers.google.com/actions/images/badges/XPM_BADGING_GoogleAssistant_VER.png');card.setText('This is the body text of a card.  You can even use line\nbreaks and emoji! 💁');card.setButton({text: 'This is a button', url: 'https://assistant.google.com/'});const anotherCard = new Card({    title: 'card title',    text: 'card text',    imageUrl: https://developers.google.com/actions/images/badges/XPM_BADGING_GoogleAssistant_VER.png,    buttonText: This is a button',    buttonUrl: 'https://assistant.google.com/',    platform: 'ACTIONS_ON_GOOGLE'});
```
<a name="Card+setTitle"></a>

### card.setTitle(title) ⇒ [<code>Card</code>](#Card)
Set the title for a Card

**Kind**: instance method of [<code>Card</code>](#Card)  

| Param | Type | Description |
| --- | --- | --- |
| title | <code>string</code> | containing the title content |

**Example**  
```js
let card = new Card();card.setTitle('sample card title')
```
<a name="Card+setText"></a>

### card.setText(text) ⇒ [<code>Card</code>](#Card)
Set the text for a Card

**Kind**: instance method of [<code>Card</code>](#Card)  

| Param | Type | Description |
| --- | --- | --- |
| text | <code>string</code> | containing the card body text content |

**Example**  
```js
let card = new Card();card.setText('sample card body text')
```
<a name="Card+setImage"></a>

### card.setImage(imageUrl) ⇒ [<code>Card</code>](#Card)
Set the image for a Card

**Kind**: instance method of [<code>Card</code>](#Card)  

| Param | Type |
| --- | --- |
| imageUrl | <code>string</code> | 

**Example**  
```js
let card = new Card();card.setImage('https://assistant.google.com/static/images/molecule/Molecule-Formation-stop.png');
```
<a name="Card+setButton"></a>

### card.setButton(button) ⇒ [<code>Card</code>](#Card)
Set the button for a Card

**Kind**: instance method of [<code>Card</code>](#Card)  

| Param | Type | Description |
| --- | --- | --- |
| button | <code>Object</code> | JSON configuration |
| options.text | <code>Object</code> | button text |
| options.url | <code>Object</code> | button link URL |

**Example**  
```js
let card = new Card();card.setButton({    text: 'button text',    url: 'https://assistant.google.com/'});
```
<a name="RichResponse+setPlatform"></a>

### card.setPlatform(platform) ⇒ [<code>RichResponse</code>](#RichResponse)
Set the platform for a specific RichResponse (optional)

**Kind**: instance method of [<code>Card</code>](#Card)  
**Overrides**: [<code>setPlatform</code>](#RichResponse+setPlatform)  

| Param | Type | Description |
| --- | --- | --- |
| platform | <code>string</code> | representing desired rich response target platform |

**Example**  
```js
let richResponse = new RichResponse();richResponse.setPlatform(PLATFORMS.ACTIONS_ON_GOOGLE)
```
<a name="Suggestion"></a>

## Suggestion ⇐ [<code>RichResponse</code>](#RichResponse)
Class representing a suggestions response

**Kind**: global class  
**Extends**: [<code>RichResponse</code>](#RichResponse)  

* [Suggestion](#Suggestion) ⇐ [<code>RichResponse</code>](#RichResponse)
    * [new Suggestion(suggestion)](#new_Suggestion_new)
    * [.setReply(reply)](#Suggestion+setReply) ⇒ [<code>Suggestion</code>](#Suggestion)
    * [.setPlatform(platform)](#RichResponse+setPlatform) ⇒ [<code>RichResponse</code>](#RichResponse)

<a name="new_Suggestion_new"></a>

### new Suggestion(suggestion)
Constructor for Suggestion object


| Param | Type | Description |
| --- | --- | --- |
| suggestion | <code>string</code> \| <code>Object</code> | reply string or an object representing a suggestion response |

**Example**  
```js
let suggestion = new Suggestion('suggestion');const anotherSuggestion = new Suggestion({    title: 'Choose an item:',    reply: 'suggestion',    platform: 'FACEBOOK'});
```
<a name="Suggestion+setReply"></a>

### suggestion.setReply(reply) ⇒ [<code>Suggestion</code>](#Suggestion)
Set the reply for a Suggestion

**Kind**: instance method of [<code>Suggestion</code>](#Suggestion)  

| Param | Type |
| --- | --- |
| reply | <code>string</code> | 

**Example**  
```js
let suggestion = new Suggestion('reply to be overwritten');suggestion.setReply('reply overwritten');
```
<a name="RichResponse+setPlatform"></a>

### suggestion.setPlatform(platform) ⇒ [<code>RichResponse</code>](#RichResponse)
Set the platform for a specific RichResponse (optional)

**Kind**: instance method of [<code>Suggestion</code>](#Suggestion)  
**Overrides**: [<code>setPlatform</code>](#RichResponse+setPlatform)  

| Param | Type | Description |
| --- | --- | --- |
| platform | <code>string</code> | representing desired rich response target platform |

**Example**  
```js
let richResponse = new RichResponse();richResponse.setPlatform(PLATFORMS.ACTIONS_ON_GOOGLE)
```
<a name="Image"></a>

## Image ⇐ [<code>RichResponse</code>](#RichResponse)
Class representing a image response.

**Kind**: global class  
**Extends**: [<code>RichResponse</code>](#RichResponse)  

* [Image](#Image) ⇐ [<code>RichResponse</code>](#RichResponse)
    * [new Image(image)](#new_Image_new)
    * [.setImage(imageUrl)](#Image+setImage) ⇒ [<code>Image</code>](#Image)
    * [.setPlatform(platform)](#RichResponse+setPlatform) ⇒ [<code>RichResponse</code>](#RichResponse)

<a name="new_Image_new"></a>

### new Image(image)
Constructor for Image object


| Param | Type | Description |
| --- | --- | --- |
| image | <code>string</code> \| <code>Object</code> | URL string or an object representing a image response |

**Example**  
```js
const imageUrl = 'https://developers.google.com/actions/images/badges/XPM_BADGING_GoogleAssistant_VER.png'let image = new Image(imageUrl);const anotherImage = new Image({    imageUrl: imageUrl,    platform: 'ACTIONS_ON_GOOGLE'});
```
<a name="Image+setImage"></a>

### image.setImage(imageUrl) ⇒ [<code>Image</code>](#Image)
Set the image for a Image

**Kind**: instance method of [<code>Image</code>](#Image)  

| Param | Type |
| --- | --- |
| imageUrl | <code>string</code> | 

**Example**  
```js
let image = new Image('https://example.com/placeholder.png');image.setImage('https://assistant.google.com/static/images/molecule/Molecule-Formation-stop.png');
```
<a name="RichResponse+setPlatform"></a>

### image.setPlatform(platform) ⇒ [<code>RichResponse</code>](#RichResponse)
Set the platform for a specific RichResponse (optional)

**Kind**: instance method of [<code>Image</code>](#Image)  
**Overrides**: [<code>setPlatform</code>](#RichResponse+setPlatform)  

| Param | Type | Description |
| --- | --- | --- |
| platform | <code>string</code> | representing desired rich response target platform |

**Example**  
```js
let richResponse = new RichResponse();richResponse.setPlatform(PLATFORMS.ACTIONS_ON_GOOGLE)
```
<a name="Payload"></a>

## Payload ⇐ [<code>RichResponse</code>](#RichResponse)
Class representing a payload response

**Kind**: global class  
**Extends**: [<code>RichResponse</code>](#RichResponse)  

* [Payload](#Payload) ⇐ [<code>RichResponse</code>](#RichResponse)
    * [new Payload(platform, payload)](#new_Payload_new)
    * [.setPayload(payload)](#Payload+setPayload) ⇒ [<code>Payload</code>](#Payload)
    * [.setPlatform(platform)](#RichResponse+setPlatform) ⇒ [<code>RichResponse</code>](#RichResponse)

<a name="new_Payload_new"></a>

### new Payload(platform, payload)
Constructor for Payload object


| Param | Type | Description |
| --- | --- | --- |
| platform | <code>string</code> | string indicating target platform of payload |
| payload | <code>Object</code> | contents for indicated platform |
| options.sendAsMessage | <code>boolean</code> | to include the payload in the   messages field. Defaults to false to only send in the payload data field. |
| options.rawPayload | <code>boolean</code> | to prevent nesting the payload under   the platform string, e.g. {"google": payload}. |

**Example**  
```js
const googlePayloadJson = {  expectUserResponse: true,  isSsml: false,  noInputPrompts: [],  richResponse: {    items: [{ simpleResponse: { textToSpeech: 'hello', displayText: 'hi' } }]  },  systemIntent: {    intent: 'actions.intent.OPTION',  }}const payload = new Payload(    'ACTIONS_ON_GOOGLE',    googlePayloadJson});
```
<a name="Payload+setPayload"></a>

### payload.setPayload(payload) ⇒ [<code>Payload</code>](#Payload)
Set the payload contents for a Payload

**Kind**: instance method of [<code>Payload</code>](#Payload)  

| Param | Type |
| --- | --- |
| payload | <code>string</code> | 

**Example**  
```js
const googlePayloadJson = {  expectUserResponse: true,  isSsml: false,  noInputPrompts: [],  richResponse: {    items: [{ simpleResponse: { textToSpeech: 'hello', displayText: 'hi' } }]  },  systemIntent: {    intent: 'actions.intent.OPTION',  }}let payload = new Payload(PLATFORMS.ACTIONS_ON_GOOGLE, {});payload.setPayload(googlePayloadJson);
```
<a name="RichResponse+setPlatform"></a>

### payload.setPlatform(platform) ⇒ [<code>RichResponse</code>](#RichResponse)
Set the platform for a specific RichResponse (optional)

**Kind**: instance method of [<code>Payload</code>](#Payload)  
**Overrides**: [<code>setPlatform</code>](#RichResponse+setPlatform)  

| Param | Type | Description |
| --- | --- | --- |
| platform | <code>string</code> | representing desired rich response target platform |

**Example**  
```js
let richResponse = new RichResponse();richResponse.setPlatform(PLATFORMS.ACTIONS_ON_GOOGLE)
```
<a name="Text"></a>

## Text ⇐ [<code>RichResponse</code>](#RichResponse)
Class representing a text response

**Kind**: global class  
**Extends**: [<code>RichResponse</code>](#RichResponse)  

* [Text](#Text) ⇐ [<code>RichResponse</code>](#RichResponse)
    * [new Text(text)](#new_Text_new)
    * [.setText(text)](#Text+setText) ⇒ [<code>Text</code>](#Text)
    * [.setSsml(ssml)](#Text+setSsml) ⇒ [<code>Text</code>](#Text)
    * [.setPlatform(platform)](#RichResponse+setPlatform) ⇒ [<code>RichResponse</code>](#RichResponse)

<a name="new_Text_new"></a>

### new Text(text)
Constructor for Text object


| Param | Type | Description |
| --- | --- | --- |
| text | <code>string</code> \| <code>Object</code> | response string or an object representing a text response |

**Example**  
```js
let text = new Text('response string');let anotherText = new Text({    text:'response string',    platform: "ACTIONS_ON_GOOGLE"});
```
<a name="Text+setText"></a>

### text.setText(text) ⇒ [<code>Text</code>](#Text)
Set the text for a Text

**Kind**: instance method of [<code>Text</code>](#Text)  

| Param | Type | Description |
| --- | --- | --- |
| text | <code>string</code> | containing the text response content |

**Example**  
```js
let text = new Text();text.setText('sample text response')
```
<a name="Text+setSsml"></a>

### text.setSsml(ssml) ⇒ [<code>Text</code>](#Text)
Set the SSML for a Text

**Kind**: instance method of [<code>Text</code>](#Text)  

| Param | Type | Description |
| --- | --- | --- |
| ssml | <code>string</code> | containing the SSML response content |

**Example**  
```js
let text = new Text();text.setSsml('<speak>This is <say-as interpret-as="characters">SSML</say-as>.</speak>')
```
<a name="RichResponse+setPlatform"></a>

### text.setPlatform(platform) ⇒ [<code>RichResponse</code>](#RichResponse)
Set the platform for a specific RichResponse (optional)

**Kind**: instance method of [<code>Text</code>](#Text)  
**Overrides**: [<code>setPlatform</code>](#RichResponse+setPlatform)  

| Param | Type | Description |
| --- | --- | --- |
| platform | <code>string</code> | representing desired rich response target platform |

**Example**  
```js
let richResponse = new RichResponse();richResponse.setPlatform(PLATFORMS.ACTIONS_ON_GOOGLE)
```
