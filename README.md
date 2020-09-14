<p align="center">
 <h1 align="center">Code Time & 100 Days of Code Readme Stats</h2>
 <p align="center">Get dynamically generated coding time stats on your readmes powered by <a href="https://www.software.com">Software.com</a>!</p>
</p>

  <p align="center">
    <a href="https://github.com/kylepeeler/codetime-readme-stats/actions">
      <img alt="Tests Passing" src="https://github.com/kylepeeler/codetime-readme-stats/workflows/Test/badge.svg" />
    </a>
    <a href="https://codecov.io/gh/kylepeeler/codetime-readme-stats">
      <img src="https://codecov.io/gh/kylepeeler/codetime-readme-stats/branch/master/graph/badge.svg" />
    </a>
    <a href="https://github.com/kylepeeler/codetime-readme-stats/issues">
      <img alt="Issues" src="https://img.shields.io/github/issues/kylepeeler/codetime-readme-stats?color=0088ff" />
    </a>
    <a href="https://github.com/kylepeeler/codetime-readme-stats/pulls">
      <img alt="GitHub pull requests" src="https://img.shields.io/github/issues-pr/kylepeeler/codetime-readme-stats?color=0088ff" />
    </a>
  </p>

  <p align="center">
    <a href="#demo">View Demo</a>
    ·
    <a href="https://github.com/kylepeeler/codetime-readme-stats/issues/new/choose">Report Bug</a>
    ·
    <a href="https://github.com/kylepeeler/codetime-readme-stats/issues/new/choose">Request Feature</a>
  </p>

  <!-- <p align="center">
    <a href="/docs/readme_fr.md">Français </a>
    ·
    <a href="/docs/readme_cn.md">简体中文</a>
    ·
    <a href="/docs/readme_es.md">Español</a>
    ·
    <a href="/docs/readme_de.md">Deutsch</a>
    ·
    <a href="/docs/readme_ja.md">日本語</a>
    ·
    <a href="/docs/readme_pt-BR.md">Português Brasileiro</a>
    ·
    <a href="/docs/readme_it.md">Italiano</a>
    ·
    <a href="/docs/readme_kr.md">한국어</a>
  </p> -->
</p>
<p align="center">Loved the project? Please consider <a href="https://www.paypal.me/kylepeeler">donating</a> to help it improve!

## Features

<!-- - [GitHub Stats Card](##github-stats-card)
- [GitHub Extra Pins](##github-extra-pins)
- [Top Languages Card](##top-languages-card) -->

- [Themes](##themes)
- [Customization](#customization)
- [Deploy Yourself](#deploy-on-your-own-vercel-instance)

## GitHub Stats Card

Copy paste this into your markdown content, and that's it. Simple!

Change the `?username=` value to your GitHub's username.

```md
[![Kyle Peeler's Code Time Stats](https://codetime-readme-stats.vercel.app/api?username=kylepeeler](https://github.com/kylepeeler/github-readme-stats)
```

_Note: Ranks are calculated based on user's stats, see [src/calculateRank.js](./src/calculateRank.js)_

### Hiding individual stats

To hide any specific stats, you can pass a query parameter `?hide=` with comma separated values.

> Options: `&hide=stars,commits,prs,issues,contribs`

```md
![Kyle Peeler's github stats](https://codetime-readme-stats.vercel.app/api?username=kylepeelerhide=contribs,prs)
```

### Adding private contributions count to total commits count

You can add the count of all your private contributions to the total commits count by using the query parameter `?count_private=true`.

_Note: If you are deploying this project yourself, the private contributions will be counted by default otherwise you need to chose to share your private contribution counts._

> Options: `&count_private=true`

```md
![Kyle Peeler's github stats](https://codetime-readme-stats.vercel.app/api?username=kylepeelercount_private=true)
```

### Showing icons

To enable icons, you can pass `show_icons=true` in the query param, like so:

```md
![Kyle Peeler's github stats](https://codetime-readme-stats.vercel.app/api?username=kylepeelershow_icons=true)
```

### Themes

With inbuilt themes you can customize the look of the card without doing any [manual customization](#customization).

Use `?theme=THEME_NAME` parameter like so :-

```md
![Kyle Peeler's github stats](https://codetime-readme-stats.vercel.app/api?username=kylepeelershow_icons=true&theme=radical)
```

#### All inbuilt themes :-

dark, radical, merko, gruvbox, tokyonight, onedark, cobalt, synthwave, highcontrast, dracula

<img src="https://res.cloudinary.com/kylepeelerimage/upload/v1595174536/grs-themes_l4ynja.png" alt="GitHub Readme Stat Themes" width="600px"/>

You can look at a preview for [all available themes](./themes/README.md) or checkout the [theme config file](./themes/index.js) & **you can also contribute new themes** if you like :D

### Customization

You can customize the appearance of your `Stats Card` or `Repo Card` however you want with URL params.

#### Common Options

- `title_color` - Card's title color _(hex color)_
- `text_color` - Body text color _(hex color)_
- `icon_color` - Icons color if available _(hex color)_
- `bg_color` - Card's background color _(hex color)_ **or** a gradient in the form of _angle,start,end_
- `theme` - name of the theme, choose from [all available themes](./themes/README.md)
- `cache_seconds` - set the cache header manually _(min: 1800, max: 86400)_

##### Gradient in bg_color

You can provide multiple comma separated values in bg_color option to render a gradient, the format of the gradient is :-

```
&bg_color=DEG,COLOR1,COLOR2,COLOR3...COLOR10
```

> Note on cache: Repo cards have default cache of 4hours (14400 seconds) if the fork count & star count is less than 1k otherwise it's 2hours (7200). Also note that cache is clamped to a minimum of 2hours and maximum of 24hours

#### Stats Card Exclusive Options

- `hide` - Hides the specified items from stats _(Comma seperated values)_
- `hide_title` - _(boolean)_
- `hide_rank` - _(boolean)_
- `show_icons` - _(boolean)_
- `include_all_commits` - Count total commits instead of just the current year commits _(boolean)_
- `count_private` - Count private commits _(boolean)_
- `line_height` - Sets the line-height between text _(number)_

#### Repo Card Exclusive Options

- `show_owner` - Show the owner name of the repo _(boolean)_

#### Language Card Exclusive Options

- `hide` - Hide the languages specified from the card _(Comma separated values)_
- `hide_title` - _(boolean)_
- `layout` - Switch between two available layouts `default` & `compact`
- `card_width` - Set the card's width manually _(number)_
- `langs_count` - Show more languages on the card, between 1-10, defaults to 5 _(number)_

> :warning: **Important:**
> Language names should be uri-escaped, as specified in [Percent Encoding](https://en.wikipedia.org/wiki/Percent-encoding)
> (i.e: `c++` should become `c%2B%2B`, `jupyter notebook` should become `jupyter%20notebook`, etc.)

---

# GitHub Extra Pins

GitHub extra pins allow you to pin more than 6 repositories in your profile using a GitHub readme profile.

Yey! You are no longer limited to 6 pinned repositories.

### Usage

Copy-paste this code into your readme and change the links.

Endpoint: `api/pin?username=kylepeeler&repo=codetime-readme-stats`

```md
[![ReadMe Card](https://codetime-readme-stats.vercel.app/api/pin/?username=kylepeeler&repo=codetime-readme-stats)](https://github.com/kylepeeler/codetime-readme-stats)
```

### Demo

[![ReadMe Card](https://codetime-readme-stats.vercel.app/api/pin/?username=kylepeeler&repo=codetime-readme-stats)](https://github.com/kylepeeler/codetime-readme-stats)

Use [show_owner](#customization) variable to include the repo's owner username

[![ReadMe Card](https://codetime-readme-stats.vercel.app/api/pin/?username=kylepeeler&repo=codetime-readme-stats&show_owner=true)](https://github.com/kylepeeler/codetime-readme-stats)

# Top Languages Card

Top languages card shows github user's top languages which have been mostly used.

_NOTE: Top languages does not indicate my skill level or something like that, it's a github metric of which languages have the most code on github, it's a new feature of codetime-readme-stats_

### Usage

Copy-paste this code into your readme and change the links.

Endpoint: `api/top-langs?username=kylepeeler

```md
[![Top Langs](https://codetime-readme-stats.vercel.app/api/top-langs/?username=kylepeeler](https://github.com/kylepeeler/codetime-readme-stats)
```

### Hide individual languages

You can use `?hide=language1,language2` parameter to hide individual languages.

```md
[![Top Langs](https://codetime-readme-stats.vercel.app/api/top-langs/?username=kylepeeler&hide=javascript,html)](https://github.com/kylepeeler/codetime-readme-stats)
```

### Show more languages

You can use the `&langs_count=` option to increase or decrease the number of languages shown on the card. Valid values are integers between 1 and 10 (inclusive), and the default is 5.

```md
[![Top Langs](https://codetime-readme-stats.vercel.app/api/top-langs/?username=kylepeelerlangs_count=8)](https://github.com/kylepeeler/codetime-readme-stats)
```

### Compact Language Card Layout

You can use the `&layout=compact` option to change the card design.

```md
[![Top Langs](https://codetime-readme-stats.vercel.app/api/top-langs/?username=kylepeelerlayout=compact)](https://github.com/kylepeeler/codetime-readme-stats)
```

### Demo

[![Top Langs](https://codetime-readme-stats.vercel.app/api/top-langs/?username=kylepeeler](https://github.com/kylepeeler/codetime-readme-stats)

- Compact layout

[![Top Langs](https://codetime-readme-stats.vercel.app/api/top-langs/?username=kylepeelerlayout=compact)](https://github.com/kylepeeler/codetime-readme-stats)

---

### All Demos

- Default

![Kyle Peeler's github stats](<https://codetime-readme-stats.vercel.app/api?username=kylepeeler>

- Hiding specific stats

![Kyle Peeler's github stats](https://codetime-readme-stats.vercel.app/api?username=kylepeeler&hide=contribs,issues)

- Showing icons

![Kyle Peeler's github stats](https://codetime-readme-stats.vercel.app/api?username=kylepeeler&hide=issues&show_icons=true)

- Include All Commits

![Kyle Peeler's github stats](https://codetime-readme-stats.vercel.app/api?username=kylepeeler&include_all_commits=true)

- Themes

Choose from any of the [default themes](#themes)

![Kyle Peeler's github stats](https://codetime-readme-stats.vercel.app/api?username=kylepeeler&show_icons=true&theme=radical)

- Gradient

![Kyle Peeler's github stats](https://codetime-readme-stats.vercel.app/api?username=kylepeeler&bg_color=30,e96443,904e95&title_color=fff&text_color=fff)

- Customizing stats card

![Kyle Peeler's github stats](https://codetime-readme-stats.vercel.app/api/?username=kylepeeler&show_icons=true&title_color=fff&icon_color=79ff97&text_color=9f9f9f&bg_color=151515)

- Customizing repo card

![Customized Card](https://codetime-readme-stats.vercel.app/api/pin?username=kylepeeler&repo=codetime-readme-stats&title_color=fff&icon_color=f9f9f9&text_color=9f9f9f&bg_color=151515)

- Top languages

[![Top Langs](https://codetime-readme-stats.vercel.app/api/top-langs/?username=kylepeeler](https://github.com/kylepeeler/codetime-readme-stats)

---

### Quick Tip (Align The Repo Cards)

You usually won't be able to layout the images side by side. To do that you can use this approach:

```md
<a href="https://github.com/kylepeeler/codetime-readme-stats">
  <img align="center" src="https://codetime-readme-stats.vercel.app/api/pin/?username=kylepeeler&repo=codetime-readme-stats" />
</a>
<a href="https://github.com/kylepeeler/codetime-readme-stats">
  <img align="center" src="https://codetime-readme-stats.vercel.app/api/pin/?username=kylepeeler&repo=codetime-readme-stats" />
</a>
```

## Deploy on your own Vercel instance

### [Check Out Step By Step Video Tutorial By @codeSTACKr](https://youtu.be/n6d4KHSKqGk?t=107)

Since the GitHub API only allows 5k requests per hour, it is possible that my `https://codetime-readme-stats.vercel.app/api` could hit the rate limiter. If you host it on your own Vercel server, then you don't have to worry about anything. Click on the deploy button to get started!

[![Deploy to Vercel](https://vercel.com/button)](https://vercel.com/import/project?template=https://github.com/kylepeeler/codetime-readme-stats)

<details>
 <summary><b> Guide on setting up Vercel  🔨 </b></summary>

1. Go to [vercel.com](https://vercel.com/)
1. Click on `Log in`
   ![](https://files.catbox.moe/tct1wg.png)
1. Sign in with GitHub by pressing `Continue with GitHub`
   ![](https://files.catbox.moe/btd78j.jpeg)
1. Sign into GitHub and allow access to all repositories, if prompted
1. Fork this repo
1. Go back to your [Vercel dashboard](https://vercel.com/dashboard)
1. Select `Import Project`
   ![](https://files.catbox.moe/qckos0.png)
1. Select `Import Git Repository`
   ![](https://files.catbox.moe/pqub9q.png)
1. Select root and keep everything as is, just add your environment variable named PAT_1 (as shown), which will contain a personal access token (PAT), which you can easily create [here](https://github.com/settings/tokens/new) (leave everything as is, just name it something, it can be anything you want)
   ![](https://files.catbox.moe/0ez4g7.png)
1. Click deploy, and you're good to go. See your domains to use the API!

</details>

## :sparkling_heart: Support the project

I open-source almost everything I can, and I try to reply to everyone needing help using these projects. Obviously,
this takes time. You can use this service for free.

However, if you are using this project and happy with it or just want to encourage me to continue creating stuff, there are few ways you can do it :-

- Giving proper credit when you use codetime-readme-stats on your readme, linking back to it :D
- Starring and sharing the project :rocket:
- [![paypal.me/kylepeeler](https://ionicabizau.github.io/badges/paypal.svg)](https://www.paypal.me/kylepeeler) you can make one-time donations via PayPal.
  - I'll probably buy a coffee. :coffee:

Thanks! :heart:

---

![https://vercel.com](https://res.cloudinary.com/kylepeelerimage/upload/v1597827714/powered-by-vercel_1_ug4uro.svg)

Contributions are welcome! <3

Inspired by many others awesome developers who created other Github Actions Cards. Special shout out to [github-readme-stats](https://github.com/anuraghazra/github-readme-stats) & [others listed here](/).

Made with :heart: and JavaScript.
