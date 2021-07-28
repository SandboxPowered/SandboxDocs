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
sandbox.on("serverResponse", (response) => {
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

## Listening to third-party events

Any resource can listen to events from other resources by prefixing the event with the resource name.

{% hint style="info" %}
Third-party events always run **after** their first-party variant
{% endhint %}

An example of listening to other resource loading events

{% code title="example/server.js" %}
```javascript
// Listening to 'resource' load
sandbox.on("resource:onResourceLoad", () => {
    console.log("Resource Loaded")
}
// Listening to 'chat' load
sandbox.on("chat:onResourceLoad", () => {
    console.log("Chat Loaded")
}
// Listening to own load
sandbox.on("onResourceLoad", () => {
    console.log("Example Loaded")
}
// Listening to own load through third-party
sandbox.on("example:onResourceLoad", () => {
    console.log("Example Loaded")
}
```
{% endcode %}

