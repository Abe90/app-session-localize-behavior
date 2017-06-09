# \<app-session-localize-behavior\>

Polymer behaviour to internationalize all your aplication

## Usage
The usage is like the app-localize-behavior component, but this save your resurces and language in session storage

## Example

```html

<dom-module id="x-element">
   <template>
    <div>{{localize('hello', 'name', 'Batman')}}</div>
   </template>
   <script>
      Polymer({
        is: "x-element",

        behaviors: [
          Polymer.AppSessionLocalizeBehavior
        ],
      });
   </script>
</dom-module>

<dom-module id="x-app">
   <template>
    <div>{{localize('hello', 'name', 'Batman')}}</div>
	<x-element></x-element>
   </template>
   <script>
      Polymer({
        is: "x-app",

        behaviors: [
          Polymer.AppSessionLocalizeBehavior
        ],

        properties: {
          language: {
            value: 'en'
          },
        }

        attached: function() {
          this.loadSessionResources('locales.json');
        },
      });
   </script>
</dom-module>
```

## Install

```
$ bower install --save Abe90/app-session-localize-behavior
```
