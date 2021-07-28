# Events

## Core Events

### OnResourceStart

{% tabs %}
{% tab title="Definition" %}
```typescript
onResourceStart(): void
```
{% endtab %}

{% tab title="Javascript" %}
```javascript
sandbox.on("onResourceLoad", () => {
    console.log("Loaded Example")
});
```
{% endtab %}
{% endtabs %}

An event that is run after a resource has started.  
**Parameters** `none`   
**Returns** `void`  
**Side** `both`

### OnResourceStop

{% tabs %}
{% tab title="Definition" %}
```typescript
onResourceStop(): void
```
{% endtab %}

{% tab title="Javascript" %}
```javascript
sandbox.on("onResourceStop", () => {
    console.log("Stopping Example")
});
```
{% endtab %}
{% endtabs %}

An event that is run before a resource is stopped.  
**Parameters** `none`   
**Returns** `void`  
**Side** `both`

## Chat Events

### chat:addMessage

{% tabs %}
{% tab title="Definition" %}
```typescript
chat:addMessage(): void
```
{% endtab %}

{% tab title="Javascript" %}
```javascript
sandbox.on("onResourceStop", () => {
    console.log("Stopping Example")
});
```
{% endtab %}
{% endtabs %}

An event that is run before a resource is stopped.  
**Parameters** `none`   
**Returns** `void`  
**Side** `both`

