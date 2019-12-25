# Input API

#### Keyboard

#### Mouse

### Controller Support

{% hint style="warning" %}
Not all implementations support controllers, check the feature parity page to see which implementations support this.
{% endhint %}

{% page-ref page="../../implementations/feature-parity.md" %}

#### Gamepad Controllers

Gamepad controllers like PlayStation and Xbox controllers should be fully supported by addons

{% tabs %}
{% tab title="API Definition" %}
```java
float getAxis(Stick, Axis)
float getTrigger(Trigger)
boolean isDown(Button)
boolean areDown(Button...)
```
{% endtab %}

{% tab title="Example" %}
```java
boolean move_forward = gamepad.getAxis(Gamepad.Stick.LEFT, Gamepad.Axis.Y) > 0;
boolean jump = gamepad.isDown(Gamepad.Button.A);
boolean dpad = gamepad.areDown(Gamepad.Button.DPAD_DOWN, Gamepad.Button.DPAD_LEFT, Gamepad.Button.DPAD_RIGHT, Gamepad.Button.DPAD_UP);
```
{% endtab %}
{% endtabs %}



