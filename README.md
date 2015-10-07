# PX4 Developer Guide

This guide *will be* published online at: http://dev.px4.io/

To start editing, install [GitBook](https://www.gitbook.com/) (requires Node.js):

On Mac OS:

```
brew install npm
```

On Linux - you're using Linux, so you should know!

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

Build once with grunt:

```
grunt
```

Then view it locally:

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
