# bestjobs.github.io Happy New Year!
Portal for bestjobs @ GitHub

This repository is rendered online at http://bestjobs.github.io, it contains a listing of repositories that are open source and maintained by bestjobs teams.

//=========

There's nothing wrong with the above, especially now that CSS support is universal in all browsers. For example, you could have a file named TEMPLATE.html on your webserver that looks like this:
```
<!DOCTYPE html>
<html lang='en-US'>
<head>
    <meta charset='UTF-8'>
    <title>Change Me</title>
    <link rel='stylesheet' href='/css.css'>
    <script defer src='/js.js'>
</head>
<body>
    <h1>Change Me</h1>
</body>
</html>
```
You'd then copy this template to /index.html, /about/index.html, /wuffles/index.html to have a root page, an about page, and a page about your dog, respectively. Because you have common CSS and Javascript, you can change some things in common files and have the entire site change when you change just one file.

However, what if you want to have a sidebar with links in it to a bunch of different sections of your site? Sure, you can copy and paste one into every single page on your site, but what if you want to change it later? Editing every single page on your site just to add a single link that shows up everywhere is a royal pain in the rear. This sort of repetitive work is better handled by some sort of HTML generator like a static-site generator or a dynamic generator.

    or a cached dynamic site (Like workPress Cache for example)

Do you know how many remote exploits WordPress has had in the past five years? Probably thousands. Do you know how many remote exploits Apache or nginx have had in the past five years that an attacker can use to mess up your website and infect your visitors' computers? Maybe one. I used to use WordPress for my site, but realized I was spending more time patching WordPress it than writing things to put on it. I moved to an SSG and haven't looked back.

=========//

NOT ready yet!!!
Adding a new repo to the listing

In order to have your repository show up at http://bestjobs.github.io, a minor change to orgs.js is required.

    To add a single repository add a new entry to orgs.js, specify the Github organization name and the repository name (separate them with a /), and set the type to repo, an example can be seen below:

  {
      "name": "RuntimeTools/appmetrics",
      "type": "repo"
  }

    To add all the repositories in a Github organization add a new entry to orgs.js, specify the Github organization name, and set the type to org, an example can be seen below:

  {
      "name": "bestjobsResilient",
      "type": "org"
  }

To test changes locally

From within the top level folder of the cloned repository run:

$ python -m SimpleHTTPServer 8000

Then open the following URL in a browser:

http://localhost:8000/

Quick Git tutorial

    Clone the repository and checkout a new branch

$ git clone https://github.com/bestjobs/bestjobs.github.io
$ git checkout -b branch_name

    Update the files you'd like to change
    Push the changes upstream

$ git add file1 file2
$ git commit -m "add your commit message here"
$ git push origin branch_name

    View your branch in Github and create a Pull Request
