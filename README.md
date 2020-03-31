# EasyAbp

An open source organization to enhance your ABP project development efficiency.

## Abp vNext Framework

[ABP vNext](https://github.com/abpframework/abp) is an open source web application framework for [ASP.NET Core](https://docs.microsoft.com/en-us/aspnet/core). All of EasyAbp organization's work is for ABP vNext framework.

## AbpHelper

AbpHelper is a tool that help you with developing Abp vNext applications. 

* We provide [AbpHelper.GUI](https://github.com/EasyAbp/AbpHelper.GUI) to help you use it more visually.

* You can also use [AbpHelper.CLI](https://github.com/EasyAbp/AbpHelper.CLI) directly if you are more used to command line.

## Modules Overview

ABP is a modular application framework. We made a lot of useful and interesting modules, you can install them to your solution easily and use them for free.

### Application Modules

| Name             | Description                    | Status                                                               |
| ---------------- |--------------------------------| -------------------------------------------------------------------- |
| [Forum](https://github.com/EasyAbp/Forum) | An abp forum application module. | ![Unplanned](https://img.shields.io/badge/-Unplanned-lightgrey) |
| [GiftCard](https://github.com/EasyAbp/GiftCard) | An abp application module where you can create gift cards and your app user can use them to exchange something. | ![Coming](https://img.shields.io/badge/-Coming-blue) |
| [FileUpload](https://github.com/EasyAbp/FileUpload) | An abp application module that allows users to upload files depending on EasyAbp.Abp.StorageService. | ![Unplanned](https://img.shields.io/badge/-Unplanned-lightgrey) |
| [PrivateMessaging](https://github.com/EasyAbp/PrivateMessaging) | An abp application module that allows users to send private messages to each other. | ![Released](https://img.shields.io/badge/-Released-brightgreen) |
| [InstantMessaging](https://github.com/EasyAbp/InstantMessaging) | An abp application module that allows users to chat with each other instantly. | ![Unplanned](https://img.shields.io/badge/-Unplanned-lightgrey) |
| [SeedingTool](https://github.com/EasyAbp/SeedingTool) | An abp application module to help host/tenants re seed the initial data with background job in launched applications. | ![Unplanned](https://img.shields.io/badge/-Unplanned-lightgrey) |
| [CacheManagement](https://github.com/EasyAbp/CacheManagement) | An abp application module helps administrators to manage the app cache data. | ![Released](https://img.shields.io/badge/-Released-brightgreen) |
| [UniappManagement](https://github.com/EasyAbp/UniappManagement) | 实现uni-app的应用版本管理、整包更新、热更新、差量热更新等功能的Abp应用模块 | ![Released](https://img.shields.io/badge/-Released-brightgreen) |

### Framework Modules

| Name             | Description                    | Status                                                               |
| ---------------- |--------------------------------| -------------------------------------------------------------------- |
| [Abp.RelatedDtoLoader](https://github.com/EasyAbp/Abp.RelatedDtoLoader) | An Abp module that help you automatically load related DTO (like ProductDto in OrderDto) under DDD. | ![Released](https://img.shields.io/badge/-Released-brightgreen) |
| [Abp.UsingLimiter](https://github.com/EasyAbp/Abp.UsingLimiter) | An Abp module helps you control how often your service is used. | ![Coming](https://img.shields.io/badge/-Coming-blue) |
| [Abp.StorageService](https://github.com/EasyAbp/Abp.StorageService) | An ABP module to realize storage, which helps you upload to the storage and manage the stored data. | ![Unplanned](https://img.shields.io/badge/-Unplanned-lightgrey) |
| [Abp.Captcha](https://github.com/EasyAbp/Abp.Captcha) | An Abp module to generate CAPTCHAs and provide verification for app users through email, SMS or more. | ![Unplanned](https://img.shields.io/badge/-Unplanned-lightgrey) |
| [Abp.Sms](https://github.com/EasyAbp/Abp.Sms) | Abp SMS module. | ![Unplanned](https://img.shields.io/badge/-Unplanned-lightgrey) |
| [Abp.Elk](https://github.com/EasyAbp/Abp.Elk) | Abp ELK (Elasticsearch + Logstash + Kibana) module. | ![Unplanned](https://img.shields.io/badge/-Unplanned-lightgrey) |
| [Abp.Workflow](https://github.com/EasyAbp/Abp.Workflow) | Abp workflow module. | ![Unplanned](https://img.shields.io/badge/-Unplanned-lightgrey) |
| [Abp.SignalR](https://github.com/EasyAbp/Abp.SignalR) | Abp SignalR module. | ![Unplanned](https://img.shields.io/badge/-Unplanned-lightgrey) |
| [Abp.EventBus.CAP](https://github.com/EasyAbp/Abp.EventBus.CAP) | This is a repository integrated CAP with ABP EventBus. | ![Released](https://img.shields.io/badge/-Released-brightgreen) |
| [Abp.SettingUi](https://github.com/EasyAbp/Abp.SettingUi) | An ABP module used to manage ABP settings. | ![Released](https://img.shields.io/badge/-Released-brightgreen) |
| [Abp.WeChat](https://github.com/EasyAbp/Abp.WeChat) | 专门为 ABP vNext 封装的微信模块，包括微信公众号和微信支付相关接口 | ![Released](https://img.shields.io/badge/-Released-brightgreen) |
| [Abp.TencentCloud](https://github.com/EasyAbp/Abp.TencentCloud) | 专门为 ABP vNext 封装的腾讯云 SDK 模块 | ![Released](https://img.shields.io/badge/-Released-brightgreen) |
| [Abp.Aliyun](https://github.com/EasyAbp/Abp.Aliyun) | 专门为 ABP vNext 封装的阿里云 SDK 模块 | ![Released](https://img.shields.io/badge/-Released-brightgreen) |

### UI Theme Modules

| UI Framework | Name                    | Description                              | Status           |
| ------------ |-------------------------| ---------------------------------------- | ---------------- |
| MVC          | [Easy](https://github.com/EasyAbp/Abp.AspNetCore.Mvc.UI.Theme.Easy) | EasyAbp's first Abp MVC UI theme module. | ![Unplanned](https://img.shields.io/badge/-Unplanned-lightgrey) |

## How to Contribute?

If you want to contribute codes or a new module to EasyAbp organization, please read the [Module Development Specification](Module-Development-Specification.md) document.
