grunt-nuget
================

[Grunt][grunt] NuGet Interface - Create and publish your NuGet packages using GruntJS.

## Getting Started

Install this grunt plugin next to your project's gruntfile with: `npm install grunt-nuget --save-dev`

NOTE : if you are on a unix system, you should install [Mono][mono] first.

Then add this line to your project's `Gruntfile.js` :

```javascript
grunt.loadNpmTasks('grunt-nuget');
```

Then specify your config: ([more informations][doc-options])

```javascript
grunt.initConfig({
```

For package creation : ([more informations][pack-options])

```javascript
    nugetpack: {
        dist: {
            src: 'tests/Package.nuspec',
            dest: 'tests/'
        }
    }
```

For package publication : ([more informations][push-options])

```javascript
	nugetpush: {
		dist: {
			src: 'tests/*.nupkg',
 
			options: {
				apiKey: 'XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX'
			}
		}
	}
```

For package restore : ([more informations][restore-options])

```javascript
	nugetrestore: {
		restore: {
			src: 'tests/packages.config',
			dest: 'packages/'
		}
	}
```

```javascript
});
```

In order to avoid specifying your API Key inside your package you can use command line task : ([more informations][key-options])

```
grunt nugetkey --key=XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

[grunt]: https://github.com/gruntjs/grunt
[mono]: http://www.go-mono.com/mono-downloads/download.html
[pack-options]: https://github.com/spatools/grunt-nuget/wiki/Pack-Options
[push-options]: https://github.com/spatools/grunt-nuget/wiki/Push-Options
[restore-options]: https://github.com/spatools/grunt-nuget/wiki/Restore-Options
[key-options]: https://github.com/spatools/grunt-nuget/wiki/Key-Options

## Release History
* 0.1.0 Initial Release
* 0.1.1 Fix some issues

