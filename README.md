
# linuxphoneapps.org

## Join the [discussion on how to build LinuxPhoneApps](https://framagit.org/linmobapps/linmobapps.frama.io/-/issues/10)

## What is this?

Abandoned working draft for a [Zola](https://getzola.org)-based (likely with the [adidoks](https://www.getzola.org/themes/adidoks/) theme) replacement for [LINMOBapps.frama.io](https://linmobapps.frama.io) - the goal is an app directory for Linux Phones like the PinePhone and Librem 5, which 
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

### What's the Roadmap?

#### 1. Getting a rough Zola site to work ([milestone 1](https://github.com/linuxphoneapps/linuxphoneapps.org/milestone/1))

The spec for apps needs to get to a somewhat viaable form first before moving the apps over. The open issues should clarify what's still missing and needs clarification. [This template]() should resemble the current draft of an app entry.

##### 1.1 Overhaul current dataset of [LINMOBapps](https://linmobapps.frama.io)

See the corresponding [Milestone over at LINMOBapps](https://framagit.org/linmobapps/linmobapps.frama.io/-/issues?milestone_title=%5Bapps.csv%5D+Overhaul+Q3+2021).

##### 1.2 Optional goal: Include games ([milestone](https://github.com/linuxphoneapps/linuxphoneapps.org/milestone/2))

The above under 1.0 and 1.1 applies to the game section, too. Feel free to add issues to the milestome, any help is welcome.

#### 1.3 Work on a converter from apps.csv (optionally also games.csv) to individual app

To reach this goal I've already [started a project](https://github.com/linuxphoneapps/appscsv2toml).

#### 2. Launch properly on LinuxPhoneApps.org with all apps brought over

No milestone for this yet. It will be added (along with issues), once 1. and 1.1 are finished, as these are blockers for this milestone.

##### 2.5. "Semi-Automatic metadata based updates"

Using [AppStream Metadata](https://www.freedesktop.org/software/appstream/docs/chap-Metadata.html) it should be possible to add more information, such as release notes or upstream screenshots with relatively little work.
For this, an "AppStream to LPA-TOML" converter will have to be created, and likely some diff'ing logic that either analyses the metainfo.xml/appdata.xml files or their converted counterparts.

We also might need a seperate, modular "updating" logic, as a key goal is to augment upstream information by information our contributors collect/provide.

In theory work on this Milestone can be started right now, as the current template is likely to not change too much (it might be extended, but that's all). It would definitely be helpful to also have a definitive list of the (relevant) kinds of extra information [appstream metadata](https://www.freedesktop.org/software/appstream/docs/chap-Metadata.html) can contain that we don't currently collect/list on [alpha.linuxphoneapps.org](https://alpha.linuxphoneapps.org/apps/)/[LINMOBapps](https://linmobapps.frama.io) as early as possible.

#### 3. Pie in the Sky

* Web app for Linux Phones
* package repositories
* ...
