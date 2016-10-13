# Directive creates scope

### Problem
can't get memo($scope.memo) from controller.

```xml
  <div ng-if="memoInputType === 'textarea'">
    <textarea ng-model="memo"></textarea>
  </div>
  <div ng-if="memoInputType === 'input'">
    <input type="text" ng-model="memo">
  </div>
  <button type="button" ng-click="ok()">{{okBtnText}}</button>
```



### Root Cause
* Directive like ng-if creates new scope. memoInputType and memo is not in same scope.



### Solution

```xml
  <div ng-if="memoInputType === 'textarea'">
    <textarea ng-model="$parent.memo"></textarea>
  </div>
  <div ng-if="memoInputType === 'input'">
    <input type="text" ng-model="$parent.memo">
  </div>
  <button type="button" ng-click="ok()">{{okBtnText}}</button>
```

* The scope created within ng-if inherits property from parent scope. So 'memo' gets value from parent, if child scope doesn't have memo variable. I input sth to input-text, child scope set memo to its own property.
*  ng-repeat, ng-switch, ng-view and ng-include all create new child scopes



### References
* [AngularJS posting: Understanding Scopes](https://github.com/angular/angular.js/wiki/Understanding-Scopes)
* [AngularJS document: ngIf](https://docs.angularjs.org/api/ng/directive/ngIf)
* [Stack Overflow: Angularjs ng-model doesn't work inside ng-if](http://stackoverflow.com/questions/18342917/angularjs-ng-model-doesnt-work-inside-ng-if)