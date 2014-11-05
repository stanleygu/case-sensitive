`case-sensitive`
==============

Directive that allows `ng-attr-*` to bind to case sensitive attributes. See example usage below.

Provides a fix for issue discussed in [angular/angular.js#1925](https://github.com/angular/angular.js/issues/1925)

# Installation

Using `bower`

`bower install --save stanleygu/case-sensitive`

Including into your Angular module

```javascript
angular.module('myModule', ['sg.case.sensitive']);
```

# Example Usage

SVG is picky about case for its attributes, such as `refX` and `refY`. Using `ng-attr-refX={{myVal}}` by default decapitalizes the attribute and results in `refx="myVal"`, which breaks the SVG. The `case-sensitive` directive lets you pass through case sensitive attributes.

```html
<marker case-sensitive="refX,refY" viewBox="0 0 10 10" markerWidth="30"
    markerHeight="30" ng-attr-refX="{{ref.x}}" ng-attr-refY="{{ref.y}}" orient="auto">
</marker>
```
