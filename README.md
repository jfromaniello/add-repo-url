Add the repository information to a package.json.

## Install

```
npm i -g add-repo-url
```

## Usage

Let's say you are working on a new package for npm and you have a sad package.json as follows:

```
{
  "name": "add-repo-url",
  "version": "1.0.0",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "MIT",
  "dependencies": {
  }
}
```

But you already have the remote url for git:

```
$ git remote -v
origin	git@github.com:jfromaniello/add-repo-url.git (fetch)
origin	git@github.com:jfromaniello/add-repo-url.git (push)
```

Run add-repo-url:

```
$ add-repo-url
$ cat package.json
{
  "name": "add-repo-url",
  "version": "1.0.0",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "MIT",
  "dependencies": {
  },
  "homepage": "https://github.com/jfromaniello/add-repo-url",
  "repository": {
    "type": "git",
    "url": "https://github.com/jfromaniello/add-repo-url.git"
  },
  "bugs": {
    "url": "https://github.com/jfromaniello/add-repo-url/issues"
  }
}
```

As you can see **add-repo-url** will add `homepage`, `repository` and `bugs`.

## License

MIT 2015 - José F. Romaniello
