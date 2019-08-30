## newRunner

This project was setup in less than a minute.

### Setup

(This is assuming you're ready to run `npm` commands - check by running `npm -v` in your favorite commandline tool. If you need to install npm: https://www.npmjs.com/get-npm)

Get your Screener API Key from your screener.io account API Key page: https://screener.io/v2/account/api-key

1. On your machine, export your Screener API Key in your .bashrc or .bash_profile file:
```
export SCREENER_API_KEY="ENTER_YOUR_APIKEY_HERE"
```
Remember to run `source .bashrc` or `source .bash_profile` after updating the file.

### Setup Process

1. In your favorite filesystem location, on the commandline, run `npm init`

2. It's going to ask you questions about the project. You can name the project whatever you'd like, and accept the defaults.

3. On the commandline in your project's folder, install Screener-Runner:

```
$ npm install --save-dev screener-runner
```

4. Create a new file in your new project called `screener.config.js`

5. Copy the example code from Screener Runner's git: https://github.com/screener-io/screener-runner#installation (under screener.config.js). You'll want to remove lines 15, 16, and 17 (or add another `url` there!)

6. In a text/code editor of your choice, edit your new project's `package.json` by finding the `scripts` object and adding `"test-screener": "screener-runner --conf screener.config.js"`, like this:

```
"scripts": {
  "test-screener": "screener-runner --conf screener.config.js"
},
```

### Run Tests

Run this command:

```
$ npm run test-screener
```

### Modify

To make updates, add/change urls in the `screener.config.js` file. You can also add:

- [Interactions](https://github.com/screener-io/screener-runner/blob/master/README.md#testing-interactions), which are similar to lightweight selenium steps

- [Responsive Design Tests](https://github.com/screener-io/screener-runner/blob/master/README.md#testing-interactions)

- [Cross Browser Tests](https://github.com/screener-io/screener-runner/blob/master/README.md#testing-interactions)
