# Customer JavaScript GitHub Action

## Demo javascript action
This action prints "Hello Snoopy" or "Hello" + the name of a person

### Inputs

#### `name-of-you`

**Required** The name of a user. Default `"GitHub User"`.

### Outputs

#### `time`

The time of the message.

### Example usage

uses: dliu-repo/demojsaction@v1.0
with:
name-of-you: 'Snoopy'

# Setup

```
mkdir demojsaction && cd demojsaction
npm init -y
touch README.md
touch action.yml
touch index.js
touch license.txt
```

```
npm install @actions/core
npm install @actions/github
```

```
sudo npm i -g @vercel/ncc
ncc build index.js --license licenses.txt
```

```
git init
git add action.yml index.js package.json package-lock.json README.md dist/*
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/dliu-repo/lab07-js-action.git
git push -u origin main

