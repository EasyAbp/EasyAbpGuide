# EasyAbp

An open source organization to enhance your ABP project development efficiency.

## Abp vNext Framework

[ABP vNext](https://github.com/abpframework/abp) is an open-source web application framework based on [ASP.NET Core](https://docs.microsoft.com/en-us/aspnet/core). All the products of EasyAbp organization are designed for ABP vNext framework.

## AbpHelper

AbpHelper is a tool that helps you with developing Abp vNext applications. 

* We provide [AbpHelper.GUI](https://github.com/EasyAbp/AbpHelper.GUI) to help you use it more visually.

* You can also use [AbpHelper.CLI](https://github.com/EasyAbp/AbpHelper.CLI) directly if you are more used to command line.

## Modules

ABP is a modular application framework. We made a lot of useful and interesting modules, you can install them to your solution easily and use them for free.

### Application Modules

| Name             | Description                    | Release                                                               |
| ---------------- |--------------------------------| -------------------------------------------------------------------- |
| [Forum](https://github.com/EasyAbp/Forum) | An abp forum application module. | ![Backlog](https://img.shields.io/badge/-Backlog-lightgrey?style=flat-square) |
| [Cms](https://github.com/EasyAbp/Cms) | An abp CMS application module. | ![Backlog](https://img.shields.io/badge/-Backlog-lightgrey?style=flat-square) |
| [EShop](https://github.com/EasyAbp/EShop) | An abp application module group that provides basic e-shop service. | [![NuGet](https://img.shields.io/nuget/v/EasyAbp.EShop.Domain.Shared.svg?style=flat-square&label=)](https://www.nuget.org/packages/EasyAbp.EShop.Domain.Shared) |
| [PaymentService](https://github.com/EasyAbp/PaymentService) | An abp application module that provides payment service. | [![NuGet](https://img.shields.io/nuget/v/EasyAbp.PaymentService.Domain.Shared.svg?style=flat-square&label=)](https://www.nuget.org/packages/EasyAbp.PaymentService.Domain.Shared) |
| [WarehouseManagement](https://github.com/EasyAbp/WarehouseManagement) | An abp application module that provides basic features to build a warehouse management system (WMS). | ![Backlog](https://img.shields.io/badge/-Backlog-lightgrey?style=flat-square) |
| [SharedResources](https://github.com/EasyAbp/SharedResources) | An abp application module that allows users to share resources with each other. | [![NuGet](https://img.shields.io/nuget/v/EasyAbp.SharedResources.Domain.Shared.svg?style=flat-square&label=)](https://www.nuget.org/packages/EasyAbp.SharedResources.Domain.Shared) |
| [CalendarManagement](https://github.com/EasyAbp/CalendarManagement) | An abp application module that allows users to arrange times for people or things, it is also easy to help you build a reservation system. | ![Backlog](https://img.shields.io/badge/-Backlog-lightgrey?style=flat-square) |
| [GiftCardManagement](https://github.com/EasyAbp/GiftCardManagement) | An abp application module where you can create gift cards and your app user can use them to exchange something. | [![NuGet](https://img.shields.io/nuget/v/EasyAbp.GiftCardManagement.Domain.Shared.svg?style=flat-square&label=)](https://www.nuget.org/packages/EasyAbp.GiftCardManagement.Domain.Shared) |
| [FileUpload](https://github.com/EasyAbp/FileUpload) | An abp application module that allows users to upload files based on EasyAbp.Abp.StorageService. | ![Backlog](https://img.shields.io/badge/-Backlog-lightgrey?style=flat-square) |
| [PrivateMessaging](https://github.com/EasyAbp/PrivateMessaging) | An abp application module that allows users to send private messages to each other. | [![NuGet](https://img.shields.io/nuget/v/EasyAbp.PrivateMessaging.Domain.Shared.svg?style=flat-square&label=)](https://www.nuget.org/packages/EasyAbp.PrivateMessaging.Domain.Shared) |
| [InstantMessaging](https://github.com/EasyAbp/InstantMessaging) | An abp application module that allows users to chat with each other instantly. | ![Backlog](https://img.shields.io/badge/-Backlog-lightgrey?style=flat-square) |
| [Oa.Workflow](https://github.com/EasyAbp/Oa.Workflow) | An abp application module you can use to create OA workflows with customized rules and data. | ![Backlog](https://img.shields.io/badge/-Backlog-lightgrey?style=flat-square) |
| [SeedingTool](https://github.com/EasyAbp/SeedingTool) | An abp application module to help host/tenants re seed the initial data with background job in launched applications. | ![Backlog](https://img.shields.io/badge/-Backlog-lightgrey?style=flat-square) |
| [CacheManagement](https://github.com/EasyAbp/CacheManagement) | An abp application module helps administrators to manage the app cache data. | [![NuGet](https://img.shields.io/nuget/v/EasyAbp.CacheManagement.Domain.Shared.svg?style=flat-square&label=)](https://www.nuget.org/packages/EasyAbp.CacheManagement.Domain.Shared) |
| [EasyComment](https://github.com/EasyAbp/EasyComment) | An ABP application module provides a flexible comment system. | ![Backlog](https://img.shields.io/badge/-Backlog-lightgrey?style=flat-square) |
| [WeChatManagement](https://github.com/EasyAbp/WeChatManagement) | 基于EasyAbp.Abp.WeChat模块实现微信登录、微信用户信息存储、微信服务器管理等高级功能的Abp应用模块 | ![Backlog](https://img.shields.io/badge/-Backlog-lightgrey?style=flat-square) |
| [UniappManagement](https://github.com/EasyAbp/UniappManagement) | 实现uni-app的应用版本管理、整包更新、热更新、差量热更新等功能的Abp应用模块 | [![NuGet](https://img.shields.io/nuget/v/EasyAbp.UniappManagement.Domain.Shared.svg?style=flat-square&label=)](https://www.nuget.org/packages/EasyAbp.UniappManagement.Domain.Shared) |

### Framework Modules

| Name             | Description                    | Release                                                               |
| ---------------- |--------------------------------| -------------------------------------------------------------------- |
| [Abp.RelatedDtoLoader](https://github.com/EasyAbp/Abp.RelatedDtoLoader) | An Abp module that help you automatically load related DTO (like ProductDto in OrderDto) under DDD. | [![NuGet](https://img.shields.io/nuget/v/EasyAbp.Abp.RelatedDtoLoader.svg?style=flat-square&label=)](https://www.nuget.org/packages/EasyAbp.Abp.RelatedDtoLoader) |
| [Abp.AspNetCoreRateLimit](https://github.com/EasyAbp/Abp.AspNetCoreRateLimit) | An Abp module helps you control how often your service is used. | [![NuGet](https://img.shields.io/nuget/v/EasyAbp.Abp.AspNetCoreRateLimit.svg?style=flat-square&label=)](https://www.nuget.org/packages/EasyAbp.Abp.AspNetCoreRateLimit) |
| [Abp.StorageService](https://github.com/EasyAbp/Abp.StorageService) | An ABP module to realize storage, which helps you upload to the storage and manage the stored data. | ![Backlog](https://img.shields.io/badge/-Backlog-lightgrey?style=flat-square) |
| [Abp.Cqrs](https://github.com/EasyAbp/Abp.Cqrs) | An Abp module to implement CQRS. | ![Backlog](https://img.shields.io/badge/-Backlog-lightgrey?style=flat-square) |
| [Abp.Captcha](https://github.com/EasyAbp/Abp.Captcha) | An Abp module to generate CAPTCHAs and provide verification for app users through email, SMS or more. | ![Backlog](https://img.shields.io/badge/-Backlog-lightgrey?style=flat-square) |
| [Abp.Sms](https://github.com/EasyAbp/Abp.Sms) | Abp SMS module. | ![Backlog](https://img.shields.io/badge/-Backlog-lightgrey?style=flat-square) |
| [Abp.TagHelperPlus](https://github.com/EasyAbp/Abp.TagHelperPlus) | An Abp MVC UI tag-helper enhancement module to provide enhanced ABP built in tag-helpers, rich text editor, dynamic tag selector and more. | ![Backlog](https://img.shields.io/badge/-Backlog-lightgrey?style=flat-square) |
| [Abp.DataDictionary](https://github.com/EasyAbp/Abp.DataDictionary) | Abp data dictionary module. | ![Backlog](https://img.shields.io/badge/-Backlog-lightgrey?style=flat-square) |
| [Abp.Elasticsearch](https://github.com/EasyAbp/Abp.Elasticsearch) | Abp Elasticsearch module. | ![Backlog](https://img.shields.io/badge/-Backlog-lightgrey?style=flat-square) |
| [Abp.WorkflowCore](https://github.com/EasyAbp/Abp.WorkflowCore) | Abp Workflow Core module. | ![Backlog](https://img.shields.io/badge/-Backlog-lightgrey?style=flat-square) |
| [Abp.EventBus.CAP](https://github.com/EasyAbp/Abp.EventBus.CAP) | This is a repository integrated CAP with ABP EventBus. | [![NuGet](https://img.shields.io/nuget/v/EasyAbp.Abp.EventBus.CAP.svg?style=flat-square&label=)](https://www.nuget.org/packages/EasyAbp.Abp.EventBus.CAP) |
| [Abp.SettingUi](https://github.com/EasyAbp/Abp.SettingUi) | An ABP module used to manage ABP settings. | [![NuGet](https://img.shields.io/nuget/v/EasyAbp.Abp.SettingUi.Domain.Shared.svg?style=flat-square&label=)](https://www.nuget.org/packages/EasyAbp.Abp.SettingUi.Domain.Shared) |
| [Abp.Trees](https://github.com/EasyAbp/Abp.Trees) | An abp module that provides standard tree structure entity implement. | [![NuGet](https://img.shields.io/nuget/v/EasyAbp.Abp.Trees.Domain.Shared.svg?style=flat-square&label=)](https://www.nuget.org/packages/EasyAbp.Abp.Trees.Domain.Shared) |
| [Abp.WeChat](https://github.com/EasyAbp/Abp.WeChat) | 专门为 ABP vNext 封装的微信模块，包括微信公众号和微信支付相关接口 | [![NuGet](https://img.shields.io/nuget/v/EasyAbp.Abp.WeChat.Common.svg?style=flat-square&label=)](https://www.nuget.org/packages/EasyAbp.Abp.WeChat.Common) |
| [Abp.TencentCloud](https://github.com/EasyAbp/Abp.TencentCloud) | 专门为 ABP vNext 封装的腾讯云 SDK 模块 | [![NuGet](https://img.shields.io/nuget/v/EasyAbp.Abp.TencentCloud.Common.svg?style=flat-square&label=)](https://www.nuget.org/packages/EasyAbp.Abp.TencentCloud.Common) |
| [Abp.Aliyun](https://github.com/EasyAbp/Abp.Aliyun) | 专门为 ABP vNext 封装的阿里云 SDK 模块 | [![NuGet](https://img.shields.io/nuget/v/EasyAbp.Abp.Aliyun.Common.svg?style=flat-square&label=)](https://www.nuget.org/packages/EasyAbp.Abp.Aliyun.Common) |

### UI Theme Modules

| UI Framework | Name                    | Description                              | Release           |
| ------------ |-------------------------| ---------------------------------------- | ---------------- |
| MVC          | [Easy](https://github.com/EasyAbp/Abp.AspNetCore.Mvc.UI.Theme.Easy) | EasyAbp's first Abp MVC UI theme module. | ![Backlog](https://img.shields.io/badge/-Backlog-lightgrey?style=flat-square) |

## Applications

ABP application startup template or installer with pre-built modules.

| Name             | Description                    | Release                                                               |
| ---------------- |--------------------------------| -------------------------------------------------------------------- |
| [EasyMall](https://github.com/EasyAbp/EasyMall) | Quickly build an e-commerce application based on EasyAbp.EShop. | [![Release](https://img.shields.io/github/v/release/EasyAbp/EasyMall?style=flat-square&label=)](https://github.com/EasyAbp/EasyMall/releases) |

## Q & A

**Q: How to make ABP modules that meet the EasyAbp standard?<br/>**
A: See [Getting Start to Develop Modules](Getting-Start-to-Develop-Modules.md) document.

**Q: How to Contribute?<br/>**
A: See [Module Development Specification](Module-Development-Specification.md#contribute-to-easyabp) document.
