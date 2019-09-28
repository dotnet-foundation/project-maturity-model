# .NET Foundation Project Continuation Policies

Project continuation is one of the most important, but least obvious, concerns for a project. As a consumer of a project, you should want to know what will happen to a project given a set of circumstances that challenge continued predictable functioning. There are high profile industry cases where project continuation did not follow a desired path, resulting in significant harm to consumers. These policies are in place to encourage project continuation in the best interests of consumers, and to make project continuation more straightforward to achieve for maintainers.

## Trusted Successor

Level 3 projects must register a trusted successor in the case that the maintainer becomes unavailable. The successor can be a specific person or an organization. In the case that the project maintainer becomes unavailable, the trusted successor will be given access to project source, packages and any other critical assets, so that the project can continue functioning.

The [project application process](maturity-profiles-policies.md#application) includes listing trusted successors.

The (yet unproven) assumption is that services like NuGet.org and GitHub will respect these maintainer-defined policies and enable adding the trusted successor(s) as an admin to an org, repo or package. Alternatively, projects can add a .NET Foundation account to act as a mechanical mediator between the maintainer and their successor, as required, using the same "unavailable" policy.

A maintainer is considered unavailable if they cannot be contacted or are otherwise unresponsive for a period of 90 days. If the maintainer is fundamentally unavailable (for example, due to death or incarceration), then they are immediately considered unavailable. These examples may seem extreme, but they are actual challenges that have occurred and that caused significant continuity challenges that were resolved in ad-hoc and time consuming ways.

Corporate-backed projects are considered to self-manage the need for a trusted successor. It is recommended that such projects use a corporate account on source and packages, such that possible breaks in continuity can be managed by corporate staff. In the case that the corporate-backer has a risk of or has gone out of business, it is recommended for maintainers to reach out to the .NET Foundation to select a successor.

Both source and packages are key artifacts in the .NET ecosystem (and many others). In terms of actual mechanics, packages are the most important resource given that a specific package may be referred to (by name and version) in thousands, even millions, of project files. If a trusted successor is able to get owner access to a package, and has a copy of the source (but maybe not admin access to the GitHub repo(s)), then they should be able to reasonably maintain project continuity. The Foundation may maintain private forks of projects in order to preserve source.

## Project forking policy

There are multiple scenarios where a project may leave the maturity ladder program. It may be a dependency of other projects, such that removing it from the program causes an undesired and viral effect on other projects. The .NET Foundation may fork the project, and publish the library under a new name, with the goal maintaining the requirements of higher-level projects that have a dependency. This down-stream fork may be temporary or enduring, as required, on a case-by-case basis.

After forking, existing GitHub repo(s) and NuGet packages would remain as-is and under maintainer control. The Foundation would need to select an appropriately differentiated package name (proposal: "dotnetfoundation.foo" in place of "foo"). The repo name could be the same, in a different org (that's how GitHub forks work).

Forking a community project is a last resort and is a messy option. It should be avoided if at all possible. Other options, like the trusted successor system is a much better solution to some of the situations where forking might be used (as a last resort).
