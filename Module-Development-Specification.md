# Module Development Specification

This document introduces the module development specification of the EasyAbp organization. Follow these rules and designs if you want to join and contribute.

## Basic Knowledges

Please read through the ABP official document: [Module Development](https://docs.abp.io/en/abp/latest/Module-Development-Basics).

## Standardization

We have some standards based on the official document: [Module Development Best Practices & Conventions](https://docs.abp.io/en/abp/latest/Best-Practices/Index).

### Abstraction

Try to design an abstract module and provide more implementations.

* Good practice: `EasyAbp.Abp.Sms`, `EasyAbp.Abp.Sms.Aws`, `EasyAbp.Abp.Sms.Azure`.
* Bad practice: `EasyAbp.Abp.AzureSms`.

### Module Naming

Example of module solution name:
* Application module: `EasyAbp.TodoManagement`.
* Framework module: `EasyAbp.Abp.Todo` (including the prefix `Abp.`).

### Solution Structure

Todo.

### More Virtual Methods

According to https://github.com/abpframework/abp/issues/3166

> * Make all public/protected methods virtual (including entities, domain services, application services, page models, view components...) to make them easily overridable.
> * Make all private methods of domain & application services "protected virtual" to also be able to override them.

Generally, please virtualize the above methods, but you should also think about maintainability and consider protecting some methods if necessary.

### Multi-tenancy

* Let your entities implement `IMultiTenant` if your module can be designed to support multi-tenancy.
* Make sure the module is hidden from tenant users on the menu when it is host only.

### User Data

Todo.

### Using IClock

Use `IClock.Now` instead of `DateTime.Now` or `DateTime.UtcNow` in all your code.

### Using ConfigureAwait.Fody

Please refer to the [common.props](https://github.com/EasyAbp/PrivateMessaging/blob/master/common.props) and the [FodyWeavers.xml](https://github.com/EasyAbp/PrivateMessaging/blob/master/src/EasyAbp.PrivateMessaging.Domain/FodyWeavers.xml) demos.

* Add `Fody` and `ConfigureAwait.Fody` references to module projects.
* Set `<ConfigureAwait ContinueOnCapturedContext="false" />`.

### Testing

Todo.

### common.props

1. Copy the [common.props](https://github.com/EasyAbp/PrivateMessaging/blob/master/common.props) demo to your module.
1. Edit `Version`, `Description`, `PackageTags` and `PackageLicenseExpression`. (Don't follow the ABP framework's version.)

### README.md

Please refer to the [README.md](https://github.com/EasyAbp/PrivateMessaging/blob/master/README.md) demo. You can customize the structure, but in fact similar formats are more readable.

### Packaging and Publishing

Todo.

### Continuous Updating

Todo.

## Contribute to EasyAbp

Todo.

### Publishing New Modules

Todo.

### Improving Existing Modules

Todo.
