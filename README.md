[![Netlify Status](https://api.netlify.com/api/v1/badges/093cf292-2fed-44ac-8a6e-be9fd452e3db/deploy-status)](https://app.netlify.com/sites/hungry-bell-ae2a9d/deploys)
# Hugo Site Build Notes

Step 1

```bash
hugo new site classic
```

Step 2

```bash
echo "# my-new-hugo-blog" >> README.md
```

Step 3

```bash
git init
```

Step 4

```bash
git add README.md
```

Step 5

```bash
git commit -m "first commit"
```

Step 6

```bash
git branch -M main
```

Step 7

```bash
git remote add origin https://github.com/<Your-GitHub-username>/my-new-hugo-blog.git
```

Step 8 

```bash
git push -u origin main
```

Step 9

```jsx
cd themes/
// make this directory if it doesnt exist
```

Step 10

```bash
git submodule add https://github.com/goodroot/hugo-classic.git
```

This is necessary to deploy to Netlify. Also it seems that submodules are required if you want to keep your theme updated. I just discovered submodules three days ago so I'm learning as I go.

Step 11

```bash
cp -a hugo-classic/exampleSite/. ../
```

This command must be executed from the themes folder. It copies and archives (the -a flag) the hugo-classic/exampleSite/. directory and its contents and put the contents in the folder one level above, the main classic/ folder.

Step 12

```bash
cd .. && hugo server
```

SUCCESS!!! You should have a working hugo server on your local machine and be able to see the site at the [localhost](http://localhost) address output in the terminal after this command.
