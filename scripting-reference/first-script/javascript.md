# In JavaScript

{% hint style="info" %}
For TypeScript development there are is a type definitions package available on NPM [here](https://www.npmjs.com/package/@sandboxpowered/api)
{% endhint %}

## Basic Server Client Script

These two scripts set up a basic way for the server and client to communicate with each other.

### Client Script

{% code title="client.js" %}
```javascript
// Runs when this resource loads
sandbox.on("onResourceLoad", () => {
    console.log("Loaded Example")
    
    sandbox.emitServer("clientReady")
});

// Runs when the event `serverResponse` is called
sandbox.on("serverResponse", (response)=> {
    // Calls this event on the same side
    sandbox.emit("chat:sendMessage", response);
})
```
{% endcode %}

### Server Script

{% code title="server.js" %}
```javascript
// Allows clients to call this event, server can call any event on clients without registration
sandbox.registerNetEvent("clientReady")

// Runs when the event `clientReady` is called
sandbox.on("clientReady", (client, data) => {
    // Calls this event on the client
    sandbox.emitClient(client, "serverResponse", data);
    
    // Alternatively
    client.emit("serverResponse", data)
});
```
{% endcode %}

