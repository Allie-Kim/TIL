# Directive creates scope

### problem

```xml
  <div class="row" ng-if="memoInputType === 'textarea'">
      <div class="col-md-10 col-md-offset-1">
        <textarea class="form-control" rows="5" ng-model="$parent.memo" placeholder="한글{{$parent.maxByte / 2}}자/영문{{$parent.maxByte}}자" kr-input></textarea>
      </div>
    </div>
    <div class="row" ng-if="memoInputType === 'input'">
      <label class="col-md-2 control-label">{{memoLabel}}</label>
      <div class="col-md-9">
        <input type="text" class="form-control" placeholder="{{$parent.placeholder}}" ng-model="$parent.memo" kr-input>
      </div>
    </div>
```

### References
* [AngularJS posting: Understanding Scopes](https://github.com/angular/angular.js/wiki/Understanding-Scopes)
* [AngularJS document: ngIf](https://docs.angularjs.org/api/ng/directive/ngIf)
* [Stack Overflow: Angularjs ng-model doesn't work inside ng-if](http://stackoverflow.com/questions/18342917/angularjs-ng-model-doesnt-work-inside-ng-if)