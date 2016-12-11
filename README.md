# felt-example-riot

A minimal example for [Riot](https://github.com/riot/riot) with [Felt](https://github.com/cognitom/felt).

## Run example

```bash
$ npm insatll
$ npm start
```

## DIY Tutorial

Start from our [tutorial branch](https://github.com/cognitom/felt-example-riot/tree/tutorial).

The branch has only HTML and JavaScript. You need to add some files.

### Install dependencies

Open your Terminal, then run commands below:

```bash
$ cd path/to/example
$ npm init -y
```

*Note*: `npm init` will make `package.json`. If `-y` flag is added, it will generate one with default values.

The files depend on some modules on npm. Download them by the command below:

```bash
$ npm install -S riot marked
$ npm install -D felt felt-recipe-riot
```

The first line will install modules actually imported from `main.js` or `components/md.tag`. The next line will install `felt` server and its recipe for Riot.

### Write a npm script

To launch a web server, add `start` script to `package.json`:

```javascript
{
  "name": "felt-example-riot",
  ...
  "scripts": {
    "start": "felt -r riot --debug"
  },
  ...
  "dependencies": {
    "marked": "^0.3.6",
    "riot": "^3.0.2"
  },
  "devDependencies": {
    "felt": "^0.3.0",
    "felt-recipe-riot": "^0.2.1"
  }
}
```

`--debug` flag is optional. If you add this flag, you will see a debug info and it's convenient to know what Felt is doing.

### Run the server

```bash
$ npm start
```

Open `http://localhost:3000` in your browser.
