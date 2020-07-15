# Content

Content in Sandbox is everything that can be represented by something physical in-game, such as blocks, items, and entities.

## Registering Content

All created content must be registered during the initialization phase of the addon. This allows Sandbox to correctly modify your Minecraft instance as needed.

To do this you can use the following simple method:

{% tabs %}
{% tab title="API Reference" %}
```java
Registrar#register(Identity, Content)
```
{% endtab %}

{% tab title="Example" %}
```java
@Override
public void register(Registrar registrar) {
    registrar.register(Identity.of("modid", "item"), new BaseItem(new Item.Settings()));
}
```
{% endtab %}
{% endtabs %}



