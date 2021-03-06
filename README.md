<p align="center">
    <img alt="Gatsby" src="./w2g.jpg" width="400" />
</p>
<h1 align="center">
  gatsby-wordpress-migrate
</h1>

![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)
![](https://img.shields.io/npm/l/gatsby-wordpress-migrate.svg)
![](https://img.shields.io/npm/dw/gatsby-wordpress-migrate.svg)

Migrate from Wordpress without pain!

Huge community is migrating from Wordpress to Gatsby, especially developers. In order to migrate with ease and out of my pain I created this tool.

With `gatsby-wordpress-migrate` you can convert all your wordpress posts to gatsby-blog compatible in a fraction of a command.

## 🚀 Quick start

Add this code at the end of the functions.php (on wordpress, go to Appearance > Editor > functions.php) of your wordpress theme to export the `<p>` tags so we'll be able to make your text breath (otherwise they are not exported and we won't be able to say when paragraphs start/end) ;)

```php
function codelight_content_export($content) {
 return wpautop($content);
}
add_filter('the_content_export', 'codelight_content_export', 999);
```

**Install** this package globally or to your project with npm or yarn.

```sh
# Install gatsby-wordpress-migrate globally with yarn
yarn global add gatsby-wordpress-migrate
```

or

```sh
# Install gatsby-wordpress-migrate locally with yarn and make it a dev dependency
yarn add -D gatsby-wordpress-migrate
```

**Heads up**. To download all the Wordpress posts of yours, login to your Wordpress dashboard, go to `Tools > Export` and then download export file with your posts.

**Run** the CLI commands `wordpress2gatsby` and let you guided **or** run it with the following syntax.

```sh
wordpress2gatsby <XML filename> <destination folder>
# Example: wordpress2gatsby wordpressdata.xml content/blog
```

## 🧐 Example

![example](./example.gif)

## 🤟 Help it grow

You can jump in and contribute directly or file an issue in order to start exploring more opportunities/edge cases

To file the issue just follow the instructions 📃

<br/>
<br/>

---

<p align="center">
<sub><sup>Made with&nbsp&nbsp🧠 &nbsp&nbspby <a href="https://twitter.com/CostasAlexoglou">Product E:ngineer</a></sup></sub>
</p>
