# Module Review Standard

## Application Project

* TodoAppService should implement ITodoAppService.

## Application.Contracts Project

* ITodoAppService interface should contains all the public methods.

## Domain Project

* All the repository public methods should have cancellationToken param.
* If the Todo entity has relationships, all the custom repository query methods should have `includeDetails` param, the default value for get list methods is `false` and for get/find methods is `false`.

## Web Project

* In Pages folder, the Todo folders should in the TodoManagement (module name) folder.
* List pages should have the `Title`, `BreadCrumb` and `MenuItemName` configurations in PageLayout.Content.
* List pages should have actions permission check.
* Localizations of Modal pages should work.
* Sub list pages should show the parent entity identification. For example, using `PageLayout.Content.Title = "TodoItem (TodoName1)";` and `<abp-card-title>TodoItem (TodoName1)</abp-card-title>`
```
