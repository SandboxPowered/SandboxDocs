# Blocks

All blocks in Sandbox implement the [`Block` interface](), which provides access to most of the features of both vanilla and modded blocks.

## Creating a Block

While addons can implement the `Block` interface directly, most cases are already covered by the implementation provided by `BaseBlock`.

`BaseBlock` can be constructed by passing an instance of `Block.Settings` to its constructor. This allows you to fine tune most of the blocks properties, as specified in the text that follows. Refer to the full API documentation for more information on the specific methods.

* `material` - The block's `Material`, which defines properties such as whether the block can burn or lets light through.
* `hardness` - The hardness of a block: the higher this number, the longer the time required to mine it with a pickaxe.
* `resistance` - The resistance of a block against explosions: higher numbers means that the block requires more strength to be exploded.
* `slipperiness` - The slipperiness of a block: higher values identify blocks where friction applies less.
* `velocity` - The multiplier by which the entity's speed is multiplied when it passes over this block.
* `jumpVelocity` - The multiplier by which the entity's jump speed is multiplied when it passes over this block.
* `luminance` - The light level emitted from a block: it ranges between 0 \(no light\) and 15 \(radiates up until 15 blocks away\).
* `opacity` - The amount of light that is blocked from passing through this block, ranging from 0 \(all lights goes through\) and 15 \(all light is blocked\).

