# ngWrite

[![Build Status](https://img.shields.io/github/workflow/status/ngfelixl/ng-write/Node.js%20CI)](https://github.com/ngfelixl/ng-write/actions?query=workflow%3A%22Node.js+CI%22)
![npm](https://img.shields.io/npm/v/ng-write)
![dependencies](https://img.shields.io/librariesio/release/npm/ng-write)
![downloads documentations](https://img.shields.io/npm/dt/documentations?label=documentations)
![downloads ng-write](https://img.shields.io/npm/dt/ng-write?label=ng-write)
[![website](https://img.shields.io/website?url=https%3A%2F%2Fngfelixl.github.io%2Fng-write)](https://ngfelixl.github.io/ng-write)

Article editor and article visualization for Angular. Just property-bind the returned object of the article editor to the article visualization. This library is ready for usage with the Ivy rendering engine at version `9.0.2` and following. See this library in action [here](https://ngfelixl.github.io/ng-write).

Note: This library has been renamed from *documentations* to *ng-write*.


[![Animation (View on Github)](https://raw.githubusercontent.com/ngfelixl/ng-write/master/img/animation.gif)](https://raw.githubusercontent.com/ngfelixl/ng-write/master/img/animation.gif)

## Installation

Add the package to your angular project using

```bash
npm install ng-write
```

## The Editor

Make sure to have the `DocuEditorModule` imported. 

```typescript
@NgModule({
  imports: [ DocuEditorModule ]
})
export class ApplicationModule {}
```

The module provides a complete form with live rendering. It should integrate with your **@angular/material** configuration. In the template simply use the editor tag to create a complete form for the article.

```html
<docu-editor (save)="doc = $event"></docu-editor>
```

In the component you can define a function to handle the `save` event. For example like:

```typescript
@Component({...})
export class AppComponent {
  doc: Documentation;
}
```

You addition to that you can also define a `documentation` input data binding to the `docu-editor` tag to patch the documentation form.

- `@Output() save($event)`: When the user saves the form, the save event will emit and contain the complete nested form.
- `@Input() documentation: Documentation`: The user can patch the form with a previously created documentation.

## The Article

Make sure to import the `DocuModule`.

```typescript
@NgModule({
  imports: [ DocuModule ]
})
export class ApplicationModule {}
```

Then you can use the following tag to display the documentation

```html
<docu-article [documentation]="doc"></docu-article>
```

- `@Input() documentation: Documentation` interface.

## Contributing

Contributions are welcome. Please stick to the Angular commit message guidelines as described in this [document](https://github.com/angular/angular/blob/master/CONTRIBUTING.md) and describe your problems as detailed as possible.

## Get in touch

[![twitter](https://img.shields.io/badge/twitter-%40ngfelixl-blue.svg?logo=twitter)](https://twitter.com/intent/follow?screen_name=ngfelixl)
[![github](https://img.shields.io/badge/github-%40ngfelixl-blue.svg?logo=github)](https://github.com/ngfelixl)

Hi, I am Felix,<br>
Senior Software Engineer, Angular, RxJS and NgRX contributor. For direct contact please add me on twitter, github or visit my personal [website](https://felixlemke.dev).

![avatar](https://avatars2.githubusercontent.com/u/24190530?s=150&v=4)
