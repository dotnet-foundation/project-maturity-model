# TerraFX

[TerraFX](https://github.com/terrafx/terrafx) is a framework for developing multimedia-based applications. It is still in the early development stages, but is quickly ramping up.

Currently there are low-level, high-performance interop bindings provided for:
* [Xlib](https://github.com/terrafx/terrafx.interop.xlib)
* [Pulse Audio](https://github.com/terrafx/terrafx.interop.pulseaudio)
* [Vulkan](https://github.com/terrafx/terrafx.interop.vulkan)
* [Windows](https://github.com/terrafx/terrafx.interop.windows)
  * D2D1
  * D3D12
  * DWrite
  * DXGI
  * WinCodec
  * Minimal Win32 Bindings

These are used by various "[component providers](https://github.com/terrafx/terrafx/tree/master/sources/Provider)" which provide platform, architecture, or framework specific implementations of various subsystems used by TerraFX (for example: graphics, windowing, audio, etc).

The component providers are pulled into the application via MEFv2 ([System.Composition](https://docs.microsoft.com/en-us/dotnet/api/system.composition)) and which providers are used can be configured by the program.

This allows users to write simple code that works in a cross-platform manner: <https://github.com/terrafx/terrafx/blob/master/samples/TerraFX/Graphics/HelloWindow.cs>

## Project Info

* Info: https://github.com/terrafx/terrafx/blob/master/docs/README.md
* GitHub: terrafx/terrafx
* NuGet: Nightlies - https://ci.terrafx.dev/_packaging?_a=feed&feed=terrafx%40Local
* License: MIT
* Main contact: @tannergooding

## Maturity Ladder

TerraFX is a level 1 project.

See [.NET Foundation Maturity Ladder](../maturity-ladder.md).

## Governance

The project has one maintainer: @tannergooding
