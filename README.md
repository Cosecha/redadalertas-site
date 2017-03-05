# RedadAlertas Static Site
Static website for local Phoenix tire shop at [http://redadalertas.com](http://redadalertas.com).

## Requirements

- Harp (static site generator)
- Gulp (node.js task runner)
- Surge (free static site hosting)

```
npm install -g harp gulp surge
```

## How To Use

Assuming you have NPM (Node Package Manager) on your machine, just run:
```
sudo npm install
```

First clone the repository to your working directory
```
git clone https://github.com/cosecha/redadalertas-site.git
```
Move into that directory
```
cd redadalertas-site
```
To start a local server with live reload, run:
```
gulp
```

### Compiling and Deploying

Once your are done editing it is time to compile and deploy to surge. To get that output simply run the command:
```
gulp compile
```
This will generate a `/www` folder in your directory where the compile and minified html, css, and JavaScript will be.

To deploy:
```
surge
```

## Set up your repo for GitHub Pages

From the root of the project repo:
```
cd _harp
```
Create the `gh-pages` directory:
```
mkdir gh-pages
```
Clone the project repo into that directory, and change into that directory:
```
git clone https://github.com/cosecha/redadalertas-site.git --branch gh-pages --single-branch gh-pages

```
You now have a `./_harp/gh-pages` directory that is ignored by git. Inside this directory is another git repository of this same project, but ONLY the gh-pages branch.


## Deploy to GitHub pages

Now that you have generated new HTML, it is time to 'deploy' to GitHub Pages.

From the root of the project repo, change into the `gh-pages` directory:
```
cd _harp/gh-pages
```
Add and commit any changes to the generated documentation:
```
git add -all
git commit -m "Your commit message here"
```
And now push the changes to the only remote available, `gh-pages`:
```
git push origin gh-pages
```
