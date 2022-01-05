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
> For framework modules, the better name of `XxxxxxModule` class for framework module is `AbpXxxxxxModule`.

### Solution Structure

Read the document [Getting Start to Develop Modules](https://github.com/EasyAbp/EasyAbpGuide/blob/master/docs/Getting-Start-to-Develop-Modules.md) and follow it to adjust your module solution from the startup template.

### More Virtual Methods

According to https://github.com/abpframework/abp/issues/3166

* Make all public/protected methods virtual (including entities, domain services, application services, page models, view components...) to make them easily overridable.
* Make all private methods of domain & application services "protected virtual" to also be able to override them.

Generally, please virtualize the above methods, but you should also think about maintainability and consider protecting some methods if necessary.

### Multi-tenancy

* Let your entities implement `IMultiTenant` if your module can be designed to support multi-tenancy.
* Make sure permissions are host-side only if they should be hidden from tenant users and vice versa.

### Menu Items

Refer to the [MenuContributor demo](https://github.com/EasyAbp/GiftCardManagement/blob/master/src/EasyAbp.GiftCardManagement.Web/GiftCardManagementMenuContributor.cs).

* The name of menu item should have a `CompanyName+ModuleName` prefix, for example: `EasyAbpGiftCardManagementGiftCard` is the `GiftCard` using the `EasyAbpGiftCardManagement` prefix.
* Create a `CompanyName+ModuleName` menu item as the root of the module and put other menu items into it, hide it if there is nosub menu item inside.

### User Data

There are two ways to get user data (such as UserName and PhoneNumber):

1. Get from ABP's identity module.

    * Use `IExternalUserLookupServiceProvider` instead of `IIdentityUserRepository` or `IIdentityUserAppService` in all your code to get user's data.

2. Create an local extra user entity (like `BlogUser`) and synchronize data from IdentityUser.

    * See ABP document: [Creating a New Entity with Its Own Database Table/Collection](https://docs.abp.io/en/abp/latest/Customizing-Application-Modules-Extending-Entities#creating-a-new-entity-with-its-own-database-table-collection).
    * Use `IDistributedEventHandler` instead of `ILocalEventHandler` to synchronize user data.

### Inherits ExtensibleObject

Classes with ExtraProperties should inherit `ExtensibleObject`. Otherwise, you should add `[Serializable]` attribute to the class and add `[JsonInclude]` to the ExtraProperties property.

### Using IClock

Use `IClock.Now` instead of `DateTime.Now` or `DateTime.UtcNow` in all your code to get current date time.

### Using ConfigureAwait.Fody

Refer to the [common.props](https://github.com/EasyAbp/PrivateMessaging/blob/master/common.props) and the [FodyWeavers.xml](https://github.com/EasyAbp/PrivateMessaging/blob/master/src/EasyAbp.PrivateMessaging.Domain/FodyWeavers.xml) demos.

* Add `Fody` and `ConfigureAwait.Fody` references to module projects.
* Set `<ConfigureAwait ContinueOnCapturedContext="false" />`.

### Don't Use the Auto API Controllers

The ABP auto API controllers is not friendly to tiered solutions, so please use the [AbpHelper](https://github.com/EasyAbp/AbpHelper.GUI/blob/master/doc/AbpHelper-CLI/Generate-Controller-Code/Usage.md) to generate controllers manually.

### Change and Use Name Constants

* Open `MyModuleNamePermissions.cs` and change **GroupName** to `EasyAbp.MyModuleName`.
* Open `MyModuleNameSettings.cs` and change **GroupName** to `EasyAbp.MyModuleName`.
* Open `MyModuleNameRemoteServiceConsts.cs` and change **RemoteServiceName** to `EasyAbpMyModuleName`.
* Open `MyModuleNameRemoteServiceConsts.cs` and change **ModuleName** to `easyAbpMyModuleName`.
* Open `MyModuleNameResource.cs` and replace `[LocalizationResourceName("MyModuleName")]` with `[LocalizationResourceName("EasyAbpMyModuleName")]`.
* Open `MyModuleNameController.cs` and add **[Area(MyModuleNameServiceConsts.ModuleName)]** attribute.

### Depend on Other Modules

Todo.

### Testing

Todo.

### common.props

Follow the steps below:
1. Copy the [common.props](https://github.com/EasyAbp/FileManagement/blob/master/common.props) demo to your module.
1. Edit `Version`, `Description`, `PackageTags` and `PackageLicenseExpression`. (Don't follow the ABP framework's version.)

### README.md

Refer to the [README.md](https://github.com/EasyAbp/FileManagement/blob/master/README.md) demo. You can customize the structure, but in fact similar formats are more readable.

### Packaging and Publishing

Refer to the [GitHub Action demo](https://github.com/EasyAbp/FileManagement/tree/master/.github/workflows/publish.yml), configure your project publication jobs. The NuGet packages will be automatic built and published after you commit code to the **master** branch with a new module version.

### Continuous Updating

* EasyAbp modules always follow the latest version of ABP framework, so when a new version ABP released, you should upgrade your modules as soon as possible.
* Write down the roadmap in README.md with reference to this [demo](https://github.com/EasyAbp/FileManagement/blob/master/docs/README.md#road-map) and implement them when you have time and inspiration.
* Create a new GitHub release and announce all the **breaking changes** before publish new version pacakges to NuGet.

## Contribute to EasyAbp

Welcome to contribute to EasyAbp organization, you can publish new modules or improve existing modules for us.

### Publish New Modules

If you want to contribute a new module to EasyAbp, please create an issue [here](https://github.com/EasyAbp/EasyAbpGuide/issues) to introduce your design and provide the link to your module Github repository. We will evaluate your design and review your code, if the module is well-designed and needed, we will add it to EasyAbp org.

### Improve Existing Modules

If you want to improve an existing module, please create a PR in the module Github repository, which we will review and merge if it is needed.
