---
description: List of internal events Sandbox has
---

# Events

## Using Events

{% tabs %}
{% tab title="JavaScript" %}
```javascript
sandbox.on("event", (arg1, arg2) => {
    console.log("Example Event")
});
```
{% endtab %}

{% tab title="Lua" %}
```lua
AddEventHandler("event", function(arg1, arg2)
    print("Example Event")
end)
```
{% endtab %}
{% endtabs %}

## Core Events

### OnResourceStart

```typescript
onResourceStart(): void
```

An event that is run after a resource has started.  
**Parameters** `none`   
**Returns** `void`  
**Side** `both`

### OnResourceStop

```typescript
onResourceStop(): void
```

An event that is run before a resource is stopped.  
**Parameters** `none`   
**Returns** `void`  
**Side** `both`

## Chat Events

### chat:addMessage

