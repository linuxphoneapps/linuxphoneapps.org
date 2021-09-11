# linuxphoneapps.org

Working draft for a [Zola](https://getzola.org)-based (likely with the [adidoks](https://www.getzola.org/themes/adidoks/) theme) replacement for [LINMOBapps.frama.io](https://linmobapps.frama.io) - the goal is an app directory for Linux Phones like the PinePhone and Librem 5, which 
* performs well on these phones (linmobapps does not),
* allows for easier contributions for developers and users,
* provides more information and requires less maintenance.

It's up and runnning at [alpha.linuxphoneapps.org](https://alpha.linuxphoneapps.org)!

For more read this [blog post](https://linmob.net/linmobapps-additions-changes-march-april-2021/#the-future-linuxphoneapps-org).

Please join the this project and contribute!

## FAQ

### How to get this running locally to hack on it?

* [Install the latest release of Zola](https://www.getzola.org/documentation/getting-started/installation/) ([Linux Distro packaging status](https://repology.org/project/zola/versions))
* Clone this repo `git clone https://github.com/linuxphoneapps/linuxphoneapps.org.git` (or fork it first and ssh clone your fork)
* `cd linuxphoneapps.org`
* Install the adidoks theme: 
  ~~~
  `git submodule init` 
  `git submodule update`
  ~~~
* After that, running `zola serve` should get the site up and running.

### How does this roughly work?

* `content` contains subfolders for the content, e.g. apps, docs or further info on taxonomies
* `templates` contains the templates that render that content. For building templates, check out the documentation for [Zola](https://www.getzola.org/documentation/getting-started/overview/) and [Tera](https://tera.netlify.app/docs/), Zola's templating language.
* `config.toml` defines a bunch of base variables for the site,
* `themes` is not a working directory, but only the place the adidoks theme gets cloned to. 

### How to add apps? Why isn't there a template for adding apps?

Please don't add apps until the ["Prototype/First release"](https://github.com/linuxphoneapps/linuxphoneapps.org/milestone/1) milestone is completed (which will bring a template and describe how to add apps). Add them over at [LINMOBapps.frama.io](https://framagit.org/linmobapps/linmobapps.frama.io/-/blob/master/apps.csv) instead for now.

The reason for this is that until `content/apps/yourappid/index.md` is somewhat finished, adding apps does not help progress. Manually adjusting 5-10 `index.md`s is a chore, adjusting 300 is a nightmare.

### What about games? 

[There's a milestone for that](https://github.com/linuxphoneapps/linuxphoneapps.org/milestone/2). No ETA, sorry! Help is welcome!
