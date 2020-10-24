# Introduction

## What is Sandbox?

Sandbox is an API designed to make modding Minecraft easier from both a newcomer and an experienced developer perspective, it aims to eliminate the continuous updating to new versions or new mappings.

With Sandbox, you have the full power of both client-side and server-side modding, without having to ask your users to install anything except the implementation of their choice.

Sandbox is composed primarily of A version agnostic API that developers can use to create addons. It is designed to be stable across Minecraft versions & mod loaders. For more information on stability, refer to the [Release Policy](../api-guides/release-policy.md) page.

Sandbox is also a lazily-loaded API, meaning addons are not loaded until a world is loading, this allows you to have different worlds with different mod selections active. Even join servers and have the servers tell you what mods you need to load allowing servers the power of clientside modding without the user needing to download an extra modpack for that server specifically.

A downside of this is that certain aspects of regular modding arent possible, Mixins and ASM for example, since addons load after the game & are meant to be platform-agnostic, mixins cant work & access the base game. Because of this, we aim to provide as many hooks, events & APIs as needed for almost any mod to be made, if you feel something is missing you can always make an issue on our API [issue tracker](https://github.com/SandboxPowered/SandboxAPI/issues) or [join our discord](https://discord.gg/m9DMfnD) & talk to us.

To use a SandboxAPI addon in the game you'd have to install one of the implementations designed for it, different implementations differ in many ways and you should check what you need to decide which implementation you should use in the [Feature Parity](../platforms/feature-parity.md) page.



