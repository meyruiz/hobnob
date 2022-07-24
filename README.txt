// Replace this in VSCode debugger config

launch.json
https://code.visualstudio.com/docs/nodejs/nodejs-debugging#_launch-configuration

{
	"folders": [
		{
			"path": "/Users/mruiz/Docs/hobnob"
		},
		{
			"path": "/Users/mruiz/.Trash/spec"
		}
	],
	"settings": {
		"launch": {
			"version": "0.2.0",
			"configurations": [
				{
					"name": "Node",
					"type": "node",
					"request": "launch",
					"program": "${file}"
				},
				{
					"name": "Babel node",
					"type": "node",
					"request": "launch",
					"runtimeExecutable": "/Users/mruiz/Docs/hobnob/node_modules/.bin/babel-node",
					"runtimeArgs": [
						"--presets",
						"@babel/env"
					],
					"program": "${file}",
					"env": {
						"BABEL_ENV": "debug"
					}
				},
				{
					"name": "Node with experimental modules",
					"type": "node",
					"request": "launch",
					"runtimeExecutable": "~/.nvm/versions/node/v16.6.0/bin/node",
					"runtimeArgs": [
						"--experimental-modules"
					],
					"program": "${file}"
				}
			],
			"compounds": []
		}
	}
}