# ACM & ACM-W at UCF Website


[![Netlify Status](https://api.netlify.com/api/v1/badges/358a3440-e9bc-4f09-815e-0d5c7e4a2b7c/deploy-status)](https://app.netlify.com/sites/acmw/deploys)

<br> 

The **ACM & ACM-W** site uses [hugo-academic](https://sourcethemes.com/academic). To get started, you'll want to clone the repo, using either:

**1.**  `git clone git@github.com:ucfacmw/site` (recommended)
1. **(a)** Once you've cloned, make sure you run  `git submodule update --init --recursive` from the root directory of the repository.

**2.**  [GitHub Desktop](https://desktop.github.com/) (only on MacOS and Windows) 

*A note about* (**1**): You'll see that there's a `:` between github.com and ucfacmw – this enforces the use of an SSH key. If you don't know what that is, or don't have one setup for GitHub – they have a [dope guide](https://help.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).

This will walk you through adding an SSH key to your personal GitHub account. We recommend using `-t ecdsa -b 384`, but their options of `-t rsa -b 4096` is also a good choice. Also, it's a good idea to set a password when prompted, but not entirely necessary.


*A note about* (**2**): This creates an SSH key for you (*we believe*), but we'd **strongly recommend** using option (**1**).

<br>

## Getting setup  with Docker and friends:

Once you have everything listed above, you'll want (**1**) Docker and (**2**) `docker-compose`.

**Using a Terminal** (*recommended*):
- **MacOS**: Use  [brew](https://brew.sh/). Then run  `brew install docker`  and  `brew install docker-compose`.
- **Linux**: Use your OS's package manager.
- **Windows**: Use [chocolatey](https://chocolatey.org/). Then run  `choco install docker`  and  `choco install docker-compose`

**GUI Installers** (MacOS / Windows):
- **MacOS**: [Docker GUI for MacOS](https://docs.docker.com/docker-for-mac/install/)
- **Windows**: [Docker GUI for Windows](https://docs.docker.com/docker-for-windows/install/)

Here are some **more resources**, since this *advice is based on mainly using MacOS and Linux*:
- Installing Docker: https://docs.docker.com/get-docker/
- Installing `docker-compose`: https://docs.docker.com/compose/install/

<br>

## Spinning up the site (hugo-academic): 

(*Make sure you follow the **NOTE** above. Also, **all commands here work on all OSes**.*)

You'll use `docker-compose` to launch the website. Make sure you're in the website repository's root directory.  (*To check, in your shell run `pwd` and you should see* `/path/to/site`.) All of these commands must be run from the root of the site.

- To **start** the container: `docker-compose up -d`.
- To **stop** the container: `docker-compose down`.
- To **view the logs**: `docker-compose logs -f hugo`. (These are helpful if the site "breaks/errors" – that is, stops compiling.)
- To **restart** the container: `docker-compose restart`. (Sometimes you'll want to clean-up the files in the container ~ e.g. say you had `localhost:6969/meetings/something` but restructured to `localhost:6969/fa20/something`, you'll find that the first URL still exists unless you restart the container. Don't bother with this unless changes are propagating and you need to see them ASAP.)

Feel free to inspect the `docker-compose.yml` and ask away. Once you've started the container, give it a few seconds to compile the site, then head over to `http://localhost:6969/` to see a live rendition of the site.

Then [personalize the site](https://sourcethemes.com/academic/docs/get-started/)!

<br>
<br>

⬇️  ⬇️ **Documentation by [George Cushen](https://georgecushen.com) can be found below!**  ⬇️ ⬇️

## Academic Kickstart: The Template for [Academic Website Builder](https://sourcethemes.com/academic/)

[**Academic**](https://github.com/gcushen/hugo-academic) makes it easy to create a beautiful website for free using Markdown, Jupyter, or RStudio. Customize anything on your site with widgets, themes, and language packs. [Check out the latest demo](https://academic-demo.netlify.com/) of what you'll get in less than 10 minutes, or [view the showcase](https://sourcethemes.com/academic/#expo).

**Academic Kickstart** provides a minimal template to kickstart your new website.

- 📚 [View the **documentation**](https://sourcethemes.com/academic/docs/)
- 💬 [Chat with the **Academic community**](https://spectrum.chat/academic) or [**Hugo community**](https://discourse.gohugo.io)
- 🐦 Twitter: [@source_themes](https://twitter.com/source_themes) [@GeorgeCushen](https://twitter.com/GeorgeCushen) [#MadeWithAcademic](https://twitter.com/search?q=%23MadeWithAcademic&src=typd)
- 💡 [Request a **feature** or report a **bug**](https://github.com/gcushen/hugo-academic/issues)
- ⬆️ **Updating?** View the [Update Guide](https://sourcethemes.com/academic/docs/update/) and [Release Notes](https://sourcethemes.com/academic/updates/)
- :heart: **Support development** of Academic:
  - ☕️ [**Donate a coffee**](https://paypal.me/cushen)
  - 💵 [Become a backer on **Patreon**](https://www.patreon.com/cushen)
  - 🖼️ [Decorate your laptop or journal with an Academic **sticker**](https://www.redbubble.com/people/neutreno/works/34387919-academic)
  - 👕 [Wear the **T-shirt**](https://academic.threadless.com/)
  - :woman_technologist: [**Contribute**](https://sourcethemes.com/academic/docs/contribute/)

[![Screenshot](https://raw.githubusercontent.com/gcushen/hugo-academic/master/academic.png)](https://github.com/gcushen/hugo-academic/)


## Ecosystem

* **[Academic Admin](https://github.com/sourcethemes/academic-admin):** An admin tool to import publications from BibTeX or import assets for an offline site
* **[Academic Scripts](https://github.com/sourcethemes/academic-scripts):** Scripts to help migrate content to new versions of Academic

## License

Copyright 2017-present [George Cushen](https://georgecushen.com).

Released under the [MIT](https://github.com/sourcethemes/academic-kickstart/blob/master/LICENSE.md) license.

[![Analytics](https://ga-beacon.appspot.com/UA-78646709-2/academic-kickstart/readme?pixel)](https://github.com/igrigorik/ga-beacon)
