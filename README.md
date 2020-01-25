# beautiful-saber

A rather poor imitation of beautiful-jekyll theme for Saber.land.

## What it is?

This is a starter project/theme for [saber.land](https://saber.land/).

If you haven't checked out Saber yet, you should. It's a wonderful project that has the potential to solve world hunger (or something). To be more specific: Saber enables you to create static sites using VueJS.

## Installation

Don't have Saber? Head over to its [quick introduction](https://saber.land/docs) and get back here.

As is the case with all themes (?), start by installing this theme in your existing saber install.

```
yarn add saber-theme-beautiful-saber
```

This theme also uses a few plugins and this is a good time to install them.

```
yarn add saber-plugin-query-posts saber-plugin-feed
```

### Configuration

In your `saber-config.yml` in the root directory, include the following lines -

```
theme: beautiful-saber

plugins:
  - resolve: saber-plugin-query-posts
  - resolve: saber-plugin-feed
    options:
      atomFeed: true
```

As already evident, these lines indicate the theme and the plugins to build out the features.

## Back story (_every project needs one_)

I loved [beautiful-jekyll](https://deanattali.com/beautiful-jekyll/) back in the day. I had blogs (plural) using that theme, and will remain ever thankful for the author's effort.

Now that I am in a position to spare effort to do something, what better way could there be to get that design to newer heights? So then, I created beautiful-saber, a poorer cousin to the original Jekyll theme but with all the advantages of a modern toolset in Saber and VueJS. Of course, I could not do this without egoist showing us cool stuff in [Minima](https://github.com/saberland/saber-theme-minima) theme.

## Credits

This template design is directly inspired by Beautiful Jekyll, a theme for Jekyll by [Dean Attali](https://github.com/daattali).

However, there are many changes made to the underlying code/structure to bring that to the amazing Saber platform.

## License

MIT.
