# Open Ria Services

[Open Ria Services](https://github.com/OpenRIAServices/OpenRiaServices) is a framework for 
 helping with the development of rich internet connected native "n-tier" applications. 
It is the evolved Open Source version of *WCF RIA Services*.

Some of ther features are: 
 * Client side entity change tracking similar in concept to Entity Framework
   * Batch save (all or nothing) and undo functionality
 * Excellent support for data binding in with built in support for validation, INotifyPropertyChanged, INotifyCollectionChanged .. 
 * Support for client side queries (where, orderby, skip, take ..)
 * Saves you from having to duplicated lots of code on the server and client
   * Code generation which generates code for client (Model and API) based on server code
   * Automatically handles DTO creation and mapping based on attributes or configuration
   * Allows sharing validation and other logic by using partial classes and automatic linking of files

## Project Info

* GitHub: [OpenRiaServices/OpenRiaServices](https://github.com/OpenRIAServices/OpenRiaServices)
* NuGet: [packages owned by OpenRiaServices](https://www.nuget.org/profiles/OpenRIAServices)
* License: Apache 2 for core libraries (MIT for samples and some community contributed libraries) 
* Main contact: @Daniel-Svensson
* [Wiki](https://github.com/OpenRIAServices/OpenRiaServices/wiki)

## Maturity Ladder

OpenRiaServices is a level 2 project.

See [.NET Foundation Maturity Ladder](../maturity-ladder.md).

## Governance

The project has a single maintainer: @Daniel-Svensson

The libraries for [fluent configuration](https://github.com/OpenRIAServices/OpenRiaServices.FluentMetadata) and [support for many-2-many relationship](https://github.com/OpenRIAServices/OpenRiaServices.M2M) have 2 maintainers: @Daniel-Svensson and @merijndejonge 

## Trusted Successors

The following contributors are [trusted successors](../project-continuation-policies.md#trusted-successor) of this project.

**None** at the moment 

Successors are requested to periodically update the timestamp beside their handle to demonstrate that they remain available for the role. An old timestamp might suggest that the successor is no longer available.

## Quick Links

* The original documentation for WCF RIA Services is still relevant and can be found at https://docs.microsoft.com/en-us/previous-versions/dotnet/wcf-ria/ee707344(v=vs.91). Namespaces and assembly names are no longer correct since they changed with the release of OpenRiaServices.
* Documentation for changes since WCF RIA Services can be found under https://github.com/OpenRIAServices/OpenRiaServices/releases and in wiki
  and for later releases in the `Changelog.md` file in the root folder
* [Wiki](https://github.com/OpenRIAServices/OpenRiaServices/wiki)
* [Roadmap](https://github.com/OpenRIAServices/OpenRiaServices/wiki/Vision---Roadmap) 
