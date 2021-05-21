---
title: WebAccountProviderConfig
author: shweaver-MSFT
description: Configuration values for what type of authentication providers to enable via the WindowsProvider.
keywords: netstandard, windows, community, toolkit, graph, login, authentication, provider, providers, identity
dev_langs:
  - csharp
---

# WebAccountProviderConfig

Configuration values for what type of authentication providers to  enable via the [WindowsProvider](./WindowsProvider.md).

| Property | Type | Description |
| -- | -- | -- |
| ClientId | string | Client Id obtained from Azure registration. |
| WebAccountProviderType | [WebAccountProviderType](./WebAccountProviderType.md) | The types of accounts providers that should be available to the user. |