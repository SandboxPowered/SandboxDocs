---
description: Everything you need to know about how the API is structured
---

# The Sandbox API Structure

Differently from other monolithic projects, Sandbox has been built with modularity in mind, allowing you to depend only on the specific parts of the API you need in your project.

Modules in the Sandbox API are split into two categories: **Main** and **Low Level**.  
**Main** modules allow you to program against a common subset of the features that are guaranteed to exist across all Sandbox implementations. Most addons should only rely on these.  
**Low Level** modules, on the other hand, give you more access to the internals of the various Sandbox implementations, but at the same time do not guarantee compatibility across various implementations.

As an example, the `rendering` module is a Main module, allowing you to access common functions like drawing a GUI or rendering a special block model. These are functions that are guaranteed to be implemented across all implementations.  
`rendering-vulkan`, on the other hand, is a Low Level module that provides you with access to implementation details of the Vulkan rendering engine that powers some Sandbox implementations, at the cost of not guaranteeing compatibility with certain implementations, such as Fabric.

For more information about which modules are available on which platform, refer to the [API Modules Parity](../implementations/api-modules-parity.md) page.

