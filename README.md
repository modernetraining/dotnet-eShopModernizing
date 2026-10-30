# eShopModernizing: legacy .NET Framework apps

This repository holds the three legacy .NET Framework sample apps from Microsoft's
[dotnet-architecture/eShopModernizing](https://github.com/dotnet-architecture/eShopModernizing)
(MIT licensed, archived). It is the starting point for Moderne demos that migrate
.NET Framework code to .NET 10 with OpenRewrite recipes and agents.

## What's included

| Solution | Projects | Framework |
|---|---|---|
| `eShopLegacyMVCSolution` | ASP.NET MVC 5 / Web API 2 catalog app, plus `eShopLegacy.Utilities` | 4.7.2 (utilities 4.6.1) |
| `eShopLegacyWebFormsSolution` | ASP.NET Web Forms catalog app | 4.7.2 |
| `eShopLegacyNTier` | WCF service and WinForms client | 4.6.1 / 4.7 |

The supporting folders (`ACI`, `Kubernetes`, `Kubernetes-DockerForWindows`, `VM`, `Setup`,
`Docs`, `img`, `assets`) are kept as they were upstream.

## What's removed

The upstream repo also contains finished ports of these apps. They are left out so that a
migration starts from the legacy code only:

- `eShopPorted` (the MVC app already ported to .NET Core)
- `eShopModernizedMVCSolution`, `eShopModernizedWebFormsSolution`, `eShopModernizedNTier`
- `ServiceFabric`, and the container build scripts for the modernized apps

The content matches upstream `main` at
[`63bc9ec`](https://github.com/dotnet-architecture/eShopModernizing/commit/63bc9ec4414d7e281dc9f9d7bdcf70030950457d)
apart from those removals and this README. Upstream history is not included.

## Running the apps

Open a solution in Visual Studio on Windows. The MVC app reads `UseMockData` from
`Web.config`: set it to `true` to run without SQL Server. The Web Forms app uses mock data
by default.

## Branches

`main` is the baseline and does not change. Demo runs work on their own branches or
Moderne changesets.
