# Two way binding problem in Korean (and special characters like *, !..)

### Problem
When typing text in Korean, two way binding failed especially in IE(11).
'keyword' ng-model is not changed.
```xml
  <input type="text" ng-model="keyword">
```

### Root Causes
Composed characters like Korean, Japanease and Chinese fire composition events which are compositionstart, compositioneupdate and compositionend.
'compositionend' event is not fired when blur or focusout from the input, textarea etc.. only in IE(11).

### Solution
'krInput' directive
```javascript
  function krInput() {
    'ngInject';

    return {
      priority : 2,
      restrict : 'A',
      compile : function(element) {
        element.on('compositionstart', function(e) {
          e.stopImmediatePropagation();
        });
      }
    };
  }

  export default {
    name: 'krInput',
    fn: krInput
  }; 
```

```xml
  <input type="text" ng-model="keyword" kr-input>
```

### References
* [AngularJS issue: textarea ng-model is not updated in IE with Korean IME](https://github.com/angular/angular.js/issues/6656)
* [[Angular JS] 한글 입력시 바인딩 오류 수정하기](http://118k.tistory.com/135)