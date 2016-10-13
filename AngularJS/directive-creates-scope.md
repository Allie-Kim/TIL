# Directive creates scope

### problem

```xml
  <div ng-if="memoInputType === 'textarea'">
    <textarea ng-model="memo"></textarea>
  </div>
  <div ng-if="memoInputType === 'input'">
    <input type="text" ng-model="memo">
  </div>
  <button type="button" ng-click="ok()">{{okBtnText}}</button>
```

### References
* [AngularJS posting: Understanding Scopes](https://github.com/angular/angular.js/wiki/Understanding-Scopes)
* [AngularJS document: ngIf](https://docs.angularjs.org/api/ng/directive/ngIf)
* [Stack Overflow: Angularjs ng-model doesn't work inside ng-if](http://stackoverflow.com/questions/18342917/angularjs-ng-model-doesnt-work-inside-ng-if)