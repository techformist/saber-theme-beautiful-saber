# beautiful-saber

A rather poor imitation of beautiful-jekyll theme for Saber.land.

## What it is?

This is a starter project/theme for [saber.land](https://saber.land/).

If you haven't checked out Saber yet, you should. It's a wonderful project that has the potential to solve world hunger (or something). To be more specific: Saber enables you to create static sites using VueJS.

## Demo

See https://beautiful-saber.netlify.com.

## Installation

Don't know Saber? Head over to its [quick introduction](https://saber.land/docs) and get back here.

### Get started the easy way

Clone the starter project for this starter theme and you will get started in ~10 seconds.

```
git clone https://github.com/techformist/beautiful-saber-example-site.git
cd beautiful-saber-example-site
yarn install
yarn dev
```

Go to https://localhost:3000 to view your brand new site.

### Arguably better way

Install saber.

```
mkdir my-awesome-site
cd my-awesome-site

yarn init -y
yarn add saber

```

Create directories for your content - `pages`, `pages\_posts`, `theme` directories - see [project structure](https://saber.land/docs/project-structure.html) for more details.

Next, install `saber-theme-beautiful-saber` theme and required plugins.

```
yarn add saber-theme-beautiful-saber saber-plugin-query-posts saber-plugin-feed
```

In `scripts` section of your `package.json`, include two lines -

```json
  "scripts": {
    // ...
    "dev": "saber",
    "build": "saber build"
    // ...
  }
```

Create `saber-config.yml` file in the saber root folder as described [here](https://saber.land/docs/saber-config.html#theme).

```yml
theme: beautiful-saber
```

You are now ready to run your site.

```
yarn dev
```

You will not see anything when you go to https://localhost:3000 because there isn't anything right now.

- Create `index.md` under `pages` directory and add some content
- Create a post under `pages/_posts` directory to see the post on home page

Have fun with your new site.

## Configuration

Configure your site using `saber-config.yml`. Below parameters are self explanatory.

```yml
theme: beautiful-saber

siteConfig:
  title: An Awesome Blog
  url: https://beautiful-saber.saberjs.org
  author: Marcus Aurelius
  email: marcus@iam.stoic
  description: I would have loved a description here, but I am happy as it is.

themeConfig:
  nav:
    - text: Home
      link: /
    - text: About
      link: /about.html
  social:
    twitter: techformist
    github: techformist
    rss: true
  disqus: techformist

plugins:
  - resolve: saber-plugin-query-posts
  - resolve: saber-plugin-feed
    options:
      atomFeed: true
```

As already evident, these lines indicate the theme and the plugins to build out the features.

You can add new plugins to enhance your site's features -

## Deployment

When you are ready, [build your site](https://saber.land/docs/deployment.html) with -

```
yarn saber build
```

You can deploy the `public` directory to GitHub, Netlify, S3, etc. to start hosting your website.

## Back story

(stuff that no one asked for)

I loved [beautiful-jekyll](https://deanattali.com/beautiful-jekyll/) back in the day. I had blogs (plural) using that theme, and will remain ever thankful for the author's effort.

Now that I am in a position to spare effort to do something, what better way could there be to get that design to newer heights? So then, I created `beautiful-saber`, a poorer cousin to the original Jekyll theme but with all the advantages of a modern toolset in Saber and VueJS. Of course, I could not do this without [Kevin Titor / egoist](http://github.com/egoist) showing us how cool stuff can happen in Saber using [Minima](https://github.com/saberland/saber-theme-minima) theme.

## Credits

This template design is directly inspired by Beautiful Jekyll, a theme for Jekyll by [Dean Attali](https://github.com/daattali).

Of course, this theme wouldn't exist without [Saber.land](https://saber.land).

## License

MIT.
