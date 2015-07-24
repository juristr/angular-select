# angular-select

AngularJS select directive

## Features

- Single Select
- Multi Select
- Tagging
- Rich templates
- AJAX
- Item Locking
- Item Disabling
- Allow clearing
- Placeholder
- Search ( filters )
- Expressive
- Material Design
- Position / Collision Detection
- Support Object and Property Binding ( track by, value as )

## API

_Example 1_

Example using `ng-repeat` with selected template and search.

    <selector ng-model="myModel" disabled="!ctrl.isEnabled">
      <selector-selected locked="$selected.locked">
        <span ng-bind-html="$selected.name"></span>
      </selector-selected>
      <selector-search placeholder="Select something..."></selector-search>
      <selector-choice value="row.value" ng-repeat="row in rows" disabled="row.disabled">
        <span ng-bind-html="row.name | highlight: search"></div>
      </selector-choice>
    </selector>

_Example 2_

Example using declaritive markup.
  
    <selector ng-model="myModel" disabled="!ctrl.isEnabled">
      <selector-selected locked="$selected.locked">
        <span ng-bind-html="$selected.name"></span>
      </selector-selected>
      <selector-choice value="panda">Panda</selector-choice>
      <selector-choice value="cow">Cow</selector-choice>
      <selector-choice value="dog">Dog</selector-choice>
    </selector>

_Example 3_

Using similar [Angular ng-option API](https://docs.angularjs.org/api/ng/directive/ngOptions)

    <selector ng-model="myColor"
      selector-choices="color.name group by color.shade disable when color.notAnOption for color in colors">
    </selector>

## Inspirations

- http://ui.lumapps.com/directives/selects
- https://github.com/angular-ui/ui-select
- https://material.angularjs.org/latest/#/demo/material.components.select
