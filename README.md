# ib-api-dotnet

An unofficial repackaging of the C# client from Interactive Brokers' official [TWS API](https://interactivebrokers.github.io/), stripped down to the bare socket client components and built for modern .NET. Use it to interact with TWS or IB Gateway directly over a socket — the code is Interactive Brokers' own client, published here as a NuGet package because IB does not publish one themselves.

Most applications want the higher-level [opentws-dotnet](https://github.com/OpenTWS/opentws-dotnet) library instead, which wraps this package's callback-based API in async request/response methods.

## Install

```sh
dotnet add package OpenTws.IbApi
```

This package was previously published as [InteractiveBrokers.TwsClient](https://www.nuget.org/packages/InteractiveBrokers.TwsClient/), which is deprecated in favor of `OpenTws.IbApi`.

## Notes

- Since August 2019, IB ships the C# client library in .NET Standard themselves. [Download the official TWS API here](https://interactivebrokers.github.io/).
- The API code in this repository is written and owned by Interactive Brokers; this repository only trims and repackages it for NuGet distribution.

## The OpenTWS project

| Repository | Description | Distribution |
|---|---|---|
| [opentws-dotnet](https://github.com/OpenTWS/opentws-dotnet) | Async .NET client library for the TWS API | [`OpenTws`](https://www.nuget.org/packages/OpenTws/) on NuGet |
| [opentws-mcp](https://github.com/OpenTWS/opentws-mcp) | Read-only MCP server exposing TWS data to AI clients like Claude | [`ghcr.io/opentws/opentws-mcp`](https://github.com/OpenTWS/opentws-mcp/pkgs/container/opentws-mcp) |
| [ib-api-dotnet](https://github.com/OpenTWS/ib-api-dotnet) | Interactive Brokers' official C# client, repackaged for modern .NET (this repository) | [`OpenTws.IbApi`](https://www.nuget.org/packages/OpenTws.IbApi/) on NuGet |

## Build

[![Build Status](https://dev.azure.com/amittleider/InteractiveBrokers.TwsClient/_apis/build/status/amittleider.tws-api-dotnet-standard?branchName=master)](https://dev.azure.com/amittleider/InteractiveBrokers.TwsClient/_build/latest?definitionId=6&branchName=master)

## Disclaimer

OpenTWS is an unofficial, community-maintained project and is not affiliated with or endorsed by Interactive Brokers.
