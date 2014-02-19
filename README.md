## jshint-teamcity

JSHint TeamCity Reporter which group by files using TeamCity Test Suites

### Install

Install with npm: `npm install --save-dev jshint-teamcity`

### Usage

Use it with:

#### JSHint CLI

```
jshint --reporter node_modules/jshint-teamcity/teamcity.js file.js
```

#### gulp-jshint

```
gulp.task('default', function () {
	gulp.src(['file.js'])
		.pipe(jshint('.jshintrc'))
		.pipe(jshint.reporter('jshint-teamcity'));
});
```

#### grunt-contrib-jshint

```
grunt.initConfig({
	jshint: {
		options: {
			reporter: require('jshint-teamcity')
		},
		target: ['file.js']
	}
});

grunt.loadNpmTasks('grunt-contrib-jshint');
grunt.registerTask('default', ['jshint']);
```

### License

Thanks to [jshint-stylish](https://github.com/sindresorhus/jshint-stylish) and [jshint-teamcity-reporter](https://github.com/e-conomic/jshint-teamcity-reporter).

MIT © David Hong
