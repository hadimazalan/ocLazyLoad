ocLazyLoad
==========

Load modules on demand (lazy load) in AngularJS

### Key features
- Dependencies are automatically loaded
- Debugger like (no eval code)
- The ability to mix normal boot and load on demand
- Load via the service or the directive
- Use your own async loader (requireJS, script.js ...)

#### Using
1. Put ocLazyLoad.js into you project
2. Add the module ```oc.lazyLoad``` to your application
3. Configure the service provider ```$loadOnDemandProvider```
4. Load on demand using the service or the directive :

```javascript
$ocLazyLoad.load({
	name: 'TestModule',
	files: ['testModule.js']
}).then(function() {
	console.log('done');
});
```

```html
<div oc-lazy-load="{name: 'TestModule', files: ['js/testModule.js'], template: 'partials/testLazyLoad.html'}"></div>
```

See the example in the 'example' folder to know how to integrate ocLazyLoad with your router.