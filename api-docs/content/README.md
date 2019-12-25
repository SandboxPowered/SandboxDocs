# Content

## Registering Content

Content registration is a fairly straight forward process:

{% tabs %}
{% tab title="API Reference" %}
```java
SandboxAPI#register(Identity, Content)
```
{% endtab %}

{% tab title="Example" %}
```java
@Override
public void init(SandboxAPI api) {
    api.register(Identity.of("modid", "item"), new BaseItem(new Item.Settings()));
}
```
{% endtab %}
{% endtabs %}



