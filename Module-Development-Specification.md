# Module Development Specification

This document introduces the module development specification of the EasyAbp organization. Follow these rules and designs if you want to join and contribute.

## Basic Knowledges

Please read through the ABP official document: [Module Development](https://docs.abp.io/en/abp/latest/Module-Development-Basics).

## Standardization

We have some standards based on the official document: [Module Development Best Practices & Conventions](https://docs.abp.io/en/abp/latest/Best-Practices/Index).

### Abstraction

Try to design an abstract module and provide more implementations.

> For example: `EasyAbp.Abp.Sms`, `EasyAbp.Abp.Sms.Aws`, `EasyAbp.Abp.Sms.Azure`

### Module Naming

Example of module solution name:
* Application module: `EasyAbp.TodoManagement`.
* Framework module: `EasyAbp.Abp.Todo` (including the prefix `Abp.`).

### Solution Structure

Todo.

### More Virtual Methods

According to: https://github.com/abpframework/abp/issues/3166

> * Make all public/protected methods virtual (including entities, domain services, application services, page models, view components...) to make them easily overridable.
> * Make all private methods of domain & application services "propected virtual" to also be able to override them.

Generally, please virtualize the above methods, but you should also think about maintainability and consider to protect some methods if necessary.

### Multi-tenancy

* Let your entities implement `IMultiTenant` if your module can be designed to support multi-tenancy.
* Make sure the module is hidden from tenant users in the menu when it is host only.

### User Data

Todo.

### Using IClock

Use `IClock.Now` instead of `DateTime.Now` or `DateTime.UtcNow` in all your code.

### Using ConfigureAwait.Fody

Todo.

### Testing

Todo.

### common.props

Todo.

### README.md

Todo.

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
