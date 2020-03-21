# Module Development Specification

This document introduces the module development specification of the EasyAbp organization. Follow these rules and designs if you want to join and contribute.

## Basic Knowledges

Please read through the ABP official document: [Module Development](https://docs.abp.io/en/abp/latest/Module-Development-Basics).

## Standardization

We have some standards based on the official document: [Module Development Best Practices & Conventions](https://docs.abp.io/en/abp/latest/Best-Practices/Index).

### Abstraction

Todo.

### Module Naming

Example of application module solution name: `EasyAbp.TodoManagement`.

Example of framework module solution name: `EasyAbp.Abp.Todo` (including the prefix `Abp.`).

### Solution Structure

Todo.

### More Virtual Methods

According to: https://github.com/abpframework/abp/issues/3166

> * Make all public/protected methods virtual (including entities, domain services, application services, page models, view components...) to make them easily overridable.
> * Make all private methods of domain & application services "propected virtual" to also be able to override them.

Generally, please virtualize the above methods, but you should also think about maintainability and consider to protect some methods if necessary.

### Multi-tenancy

Todo.

### User Data

Todo.

### Using IClock

Todo.

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
