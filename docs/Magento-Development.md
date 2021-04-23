Magento Development
===================

### Remove all static

```shell
rm -rf pub/static/*
```

### Debugging Knockout

Debugging
```html
<div data-bind="text: ko.computed(function() { debugger; })"></div>
```

Print Data
```html
<div data-bind="text: ko.toJSON(method.method_code)"></div>
```

