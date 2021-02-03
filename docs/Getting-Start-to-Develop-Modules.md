# Getting Start to Develop Modules
This article will show you how to develop ABP modules that follow the [Module Development Specification](/docs/Module-Development-Specification.md) document.

## Step 1: Generate a new ABP module

Use ABP CLI to generate a new ABP module solution with the name prefix `EasyAbp.`, see: https://docs.abp.io/en/abp/latest/CLI#new.

## Step 2: Complete the project structure

1. For each project (except the Web project), create folders according to namespace and move all the original files and folders in, for example: `EasyAbp/(Abp)/MyModuleName/`.

2. Search `<RootNamespace>EasyAbp.MyModuleName</RootNamespace>` in **src** folder and replace with `<RootNamespace />`.

3. Move all the files in `EasyAbp.MyModuleName.Domain.Shared/EasyAbp/MyModuleName/Localization/MyModuleName/` to `EasyAbp.MyModuleName.Domain.Shared/EasyAbp/MyModuleName/Localization/`.

4. Open **MyModuleNameDomainSharedModule.cs**:
   * Change `.AddVirtualJson("/Localization/MyModuleName");` to `.AddVirtualJson("/EasyAbp/MyModuleName/Localization");`.
   * Change `options.MapCodeNamespace("MyModuleName", typeof(MyModuleNameResource));` to ``options.MapCodeNamespace("EasyAbp.MyModuleName", typeof(MyModuleNameResource));``.

5. Open **EasyAbp.MyModuleName.Domain.Shared.csproj**:
   * Change `<EmbeddedResource Include="Localization\MyModuleName\*.json" />` to `<EmbeddedResource Include="EasyAbp\MyModuleName\Localization\*.json" />`.
   * Change `<Content Remove="Localization\MyModuleName\*.json" />` to `<Content Remove="EasyAbp\MyModuleName\Localization\*.json" />`.
   * Delete other unused `<EmbeddedResource ... />` configurations.

## Step 3: Adjust pages

> Tip: Skip this step if you do not need Web project.

1. **Pages** folder should have only **MyModuleName** subfolder, other folders should be in the **MyModuleName** folder. If you adjust the structure as above, ensure the namespaces are correct.

2. Open all the **index.js** for entity management pages:
   * Change `abp.localization.getResource('MyProjectName');` to `abp.localization.getResource('EasyAbpMyProjectName');`

3. Open all the **index.cshtml** for entity management pages:
   * Change the **PageLayout.Content.MenuItemName** value to `MyModuleNameMenus.MyEntityName`.

<details>
<summary>Optional steps</summary>

1. Open all the **index.js** for entity management pages:
   * Ensure the param value in `new abp.ModalManager()` is correct.
   * Ensure the param value in `abp.auth.isGranted()`is correct.

2. Open all the **index.cshtml** for entity management pages:
   * Ensure the src value in `<abp-script ... />` and `<abp-style ... />` is correct.

3. Open **MyModuleNameMenuContributor.cs**:
   * Ensure the url of each menu item is correct.
   
</details>

## Step 4: Change the name constants

1. Open `MyModuleNamePermissions.cs` and change **GroupName** to `EasyAbp.MyModuleName`.

2. Open `MyModuleNameSettings.cs` and change **GroupName** to `EasyAbp.MyModuleName`.

3. Open `MyModuleNameMenus.cs` and change **Prefix** to a public property with the value `EasyAbp.MyModuleName`.

4. Open `MyModuleNameDbProperties.cs` and change **DbTablePrefix** and **ConnectionStringName** to `EasyAbpMyModuleName`.

5. Open `MyModuleNameHttpApiClientModule.cs` and change **RemoteServiceName** to `EasyAbpMyModuleName`.

6. Open `MyModuleNameResource.cs` and replace `[LocalizationResourceName("MyModuleName")]` with `[LocalizationResourceName("EasyAbpMyModuleName")]`.

## Step 5: Project configurations

1. Modify the **common.prop** file according to: https://github.com/EasyAbp/PrivateMessaging/blob/master/common.props.

2. Unified ABP version number.
  1. Put ABP version number into the **Directory.Build.props** file (see [demo](https://github.com/EasyAbp/PrivateMessaging/blob/master/Directory.Build.props)).
  2. Replace `<PackageReference Include="Volo.Abp.xxx" Version="x.x.x" />` to `<PackageReference Include="Volo.Abp.xxx" Version="$(AbpVersion)" />` in all the .csproj files of the solution.

3. After Building all the projects, **FodyWeavers.xml** will be generated to every project. Global replace `<ConfigureAwait />` to `<ConfigureAwait ContinueOnCapturedContext="false" />`.
