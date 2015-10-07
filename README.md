# PX4 Developer Guide

[![Build Status](https://travis-ci.org/PX4/Devguide.svg?branch=master)](https://travis-ci.org/PX4/Devguide)

This guide *is published by Travis CI* online at: http://dev.px4.io/

### Prerequisites

To start editing, install [GitBook](https://www.gitbook.com/) (requires Node.js):

On Mac OS:

```
brew install npm
```

On Linux - you're using Linux, so you should know!

```sh
sudo apt-get install npm
```

### Installing Gitbook

```
npm install grunt-cli -g
npm install gitbook-cli -g
```

Change to the directory of this repo:

```
cd px4devguide
npm install
gitbook install book

```

### Running

Build once with grunt every time the HTML template changes:

```
grunt
```

Then view it locally. *NOTE*: The local view will update when the markup files are changed,
so there is no need to re-run this command.

```
gitbook serve book
```

Open <http://localhost:4000/>. Files will update live as you edit them.

See [CONTRIBUTING.md](CONTRIBUTING.md) for information on how to submit to this guide.

## Deployment

Install required packages:

```sh
sudo gem install dotenv aws-sdk thread bundler git mime
```


```sh
export BUCKET=dev.px4.io
export AWS_KEY=[KEY]
export AWS_SECRET=[SECRET]
./deploy.rb
```

## License

Content: CC-BY

README & Template: CC-BY-SA 4.0 Template based on the 3DR px4 Dev Guide.
