[Blog](/blog/) / [Engineering](/blog/categories/engineering/)

[tutorial](/blog/tags.html#tutorial)

# Publishing Obsidian.md notes with GitLab Pages

[Scott Hampton](/company/team/#shampton) ·

Mar 15, 2022 · 16 min read

[![Scott Hampton GitLab profile](https://about.gitlab.com/blog/2022/03/15/publishing-obsidian-notes-with-gitlab-pages//images/team/scotthampton-crop.jpg)](/company/team/#shampton)

---

[Obsidian.md](https://obsidian.md) is a "knowledge base" application that uses plain text Markdown files stored in a local folder to organize your notes. The product has been growing in popularity, partly because of how extensible it is. There are a lot of community built plugins to help users configure the application to support their specific workflow. There are many people that use Obsidian to write their blog posts. [Obsidian offers a paid service to publish your notes directly](https://obsidian.md/publish) and is completely compatible with features Obsidian offers. I suggest you support the Obsidian developers if their product works for you. If you are looking for an alternative way to publish, this blog post provides a tutorial for how to publish your notes using GitLab Pages.

You can find an Obsidian.md example in [this demonstration project](https://gitlab.com/gitlab-org/frontend/playground/obsidian-and-gitlab-pages-demo) which deploys [a GitLab Pages site](https://gitlab-org.gitlab.io/frontend/playground/obsidian-and-gitlab-pages-demo/).

## What is Obsidian markdown?[](#what-is-obsidian-markdown)

Obsidian is markdown-based system, which means it incorporates tags, plugins and backlinks to create an easy-to-use system. It makes it possible for you to use symbols inside the text that are interpreted as text formatting. This [link](https://www.markdownguide.org/cheat-sheet/) is a cheat sheet of all the mardown syntax elements.

### Benefits of Obsidian.md[](#benefits-of-obsidianmd)

Perhaps the most significant benefit of Obsidian markdown (md) is its simple, straightforward design and the excellent support provided. It is also extensible, with plenty of community plugins available.

There is no proprietary formatting, encoding. This gives you greater control over how you backup files and manage change tracking.

Obsidian doesn't support git right out the box, it requires a community plugin called Obsidian Git. However, one the plugin is installed, “you end up with the greatest change tracking/archiving tool at your disposal,” one user [raves](https://www.faesel.com/blog/why-every-developer-needs-to-use-obsidian).

### How is Obsidian.md different from other markdown languages?[](#how-is-obsidianmd-different-from-other-markdown-languages)

Obsidian markdown [differs from other markdown editors](https://cylab.be/blog/149/what-is-obsidianmd-and-why-you-should-use-it) in that it uses the “Linked Thought” feature, which refers to a group of note-taking applications that allow you to link thoughts and notes together seamlessly. Because it is based on the [Markdown language](https://en.wikipedia.org/wiki/Markdown), it is light-weight. The tool expands on the markdown language with additional functionality, such as creating links between files, offering "hover over preview" of links and easy inclusion and management of sources.

For example, Obsidian lets you hover over any links added to a document and see a small preview of what the links refers to. You just need to position your mouse over the "Format your notes" link.

### Some notable features of Obsidian.md[](#some-notable-features-of-obsidianmd)

There’s a visually-striking graph view that’s acts as a map of all your files stored in Obsidian. There is also a markdown format importer that can find and replace certain Markdown syntax elements in your files, and support for [math and diagram](https://publish.obsidian.md/help/How+to/Format+your+notes) syntax.

Also noteworthy is that Obsidian makes it easy to publish notes online and it stores all of your files in plaintext markdown files.

Obsidian supports CommonMark and GitHub Flavored Markdown (GFM) so you can embed notes and other files. It stores data in folders of markdown files so you can access your notes with other text editors or markdown apps. Obsidian also lets you open existing folders of markdown files.

## Is Obsidian good for notes?[](#is-obsidian-good-for-notes)

Obsidian is a very capable, free note-taking app (with advanced, paid tiers available as well). It touts itself as a [“second brain”](https://obsidian.md/) that is good for creating a knowledge base, markdown file editor and linking notes together. It is designed to take notes quickly and is easy to use, making it an ideal app. You just open the app, create a new note and start typing.

It works across multiple platforms, including Windows, iOS, Android and Linux.

Obsidian has been called the [“most advanced note-taking app.”](https://deskoflawyer.com/secure-note-taking-apps/)

## Setting up Obsidian notes[](#setting-up-obsidian-notes)

Once you download the app, you will see the main Obsidian window, which has the different options on the left, then the folder/files panel and the composition area where you an create and edit your notes.

There are four icons on the left side: collapse panel, open quick switcher, open graph view, and open markdown importer. The collapse panel shows (or hides) the left panel.When you tap the open quick switcher button, it brings up a text box where you can begin to type. The open graph view shows a graph listing the connections each page has. The open markdown importer lets you import markdown files into Obsidian from other applications.

You’ll also see three buttons:

1. Open another vault
2. Help
3. Settings

The vault refers to a collection of notes that you can open or create.

You have the option of either creating a note directly or creating a note via a link. In the former instance, in the folder panel, click on the “new note” button or use the keyboard shortcut for Windows: Control N, or for Mac: Command N. Now you’ve created a new note.

An interesting time-saving feature is that you can create a note via a link and assign a name to that new note. You have to click on the link to actually create it.

You can find a helpful guide [here](https://www.sitepoint.com/obsidian-beginner-guide/).

## Organizing an Obsidian note using folders[](#organizing-an-obsidian-note-using-folders)

When you begin using Obsidian you have to designate where you want to keep your notes. If you already have your notes in markdown format in a folder, you would choose the “open folder as vault” option. Otherwise, you can create a new vault and choose a location to store your notes.

You can drag and drop notes to move them around. There are three icons at the top pane that allow you to create a new note, make a new folder, or change the sorting order.

Obsidian has a powerful search feature that checks the content of your notes and returns all results very quickly. Access it by clicking on the magnifying glass icon at the top to begin a search of your notes.

You’ll already be in editor mode by default when you open Obsidian and you can edit your notes or write new ones. All markdown syntax is visible in this mode. Press Ctrl + E to switch to preview mode, and the syntax will disappear and the note will appear formatted.

If you type a hashtag before a word, Obsidian will detect it and assign it to the note, regardless of where it is in your text.

## Get going with Obsidian.md[](#get-going-with-obsidianmd)

[Obsidan.md](https://obsidian.md), at it's core, is an application that helps manage your markdown files. You can download the application via their site and create a "workspace" folder when you first start the application. When using the application, all of your notes will be created in the folder you choose as your "workspace".

![Obsidian application](https://about.gitlab.com/blog/2022/03/15/publishing-obsidian-notes-with-gitlab-pages//images/blogimages/obsidian_md.png)

### Workspace file structure[](#workspace-file-structure)

Inside your Obsidian workspace, you can have any number of folders and markdown files. When you open a folder in Obsidian as your "workspace", Obsidian will automatically add a folder `.obsidian`, which contains your workspace configuration such as application styles and plugins. A basic workspace file structure could look something like this:

```
.
├── workspace_folder/
│   └── Other pages/
│   │   └── Another page.md
│   └── .obsidian
│   └── index.md
```

`index.md`

```
# Home

This is a basic home page, and a link to another page in my documents.

See [[Another page]] - note that this link uses wikilinks which Obsidian uses to help you easily link to other notes in your workspace.
```

`Other pages/Another page.md`

```
# Another page

This is another page besides the home page.
```

## Generating a static site to host your notes[](#generating-a-static-site-to-host-your-notes)

In order to publish your notes to GitLab Pages, you need to create a static site to show and navigate your notes. There are several open source tools that generate static sites from Markdown documents. After experimenting with a few, I found [MkDocs](https://www.mkdocs.org/) to be the easiest and most compatible with Obsidian.

If you would like to use MkDocs locally, you can install it with `pip install mkdocs` (Python and [pip as package manager](https://pypi.org/project/pip/) are required). This is not necessary, because in this tutorial we'll utilize GitLab CI pipelines to install MkDocs and build our site.

There are two small steps you need to make in order to get your existing Obsidian notes working with MkDocs.

### File structure[](#file-structure)

All files that are not your workspace notes will be created outside of your workspace folder. The following folder structure is how this final demo project is going to look.

```
.
├── wiki/
│   └── .obsidian
│   └── index.md
├── .gitlab-ci.yml
├── mkdocs.yml
└── requirements.txt
```

- `wiki/` - this is your Obsidian workspace folder
- `.obsidian` - the application configuration folder Obsidian uses for your workspace. This will not affect the site.
- `index.md` - MkDocs looks for `index.md` in your workspace folder to use as your site's home page.
- `.gitlab-ci.yml` - the GitLab CI configuration file used to deploy your site.
- `mkdocs.yml` - the MkDocs configuration file use to build and customize your site.
- `requirements.txt` - this file defines the Python package dependencies for MkDocs.

### Basic MkDocs Configuration[](#basic-mkdocs-configuration)

You'll need to create a configuration file `mkdocs.yml` for MkDocs to know how you would like your site to look. Here are the first four lines we need to configure our notes.

```
site_name: My Obsidian Notes
site_url: https://group-name.gitlab.io/repo-name
site_dir: public
docs_dir: ./wiki
```

- `site_name` - is what will be used as the main title for the web site.
- `site_url` - is used as the "canonical URL" of the site. You will need to use [the default URL provided by GitLab Pages](https://docs.gitlab.com/ee/user/project/pages/getting_started_part_one.html#gitlab-pages-default-domain-names) or your custom domain here.
- `site_dir` - GitLab Pages requires HTML source code to be contained in a `public` folder. This setting tells MkDocs to put the generated files in the `public` folder.
- `docs_dir` - this is the relative path to your workspace folder. I like to name mine `wiki` because it's my personal wikipedia. You can name this folder whatever you want.

We'll come back to this configuration file later to add more custom styles to your site.

## Configuring GitLab CI[](#configuring-gitlab-ci)

We need to configure a GitLab CI job to install MkDocs and build the web site based on our Obsidian notes. The following `.gitlab-ci.yml` file has the basic setup for this:

```
image: python:3.8-slim

pages:
  stage: deploy
  script:
    # Install all of the python packages for mkdocs
    - pip install -r requirements.txt
    # Build the site using mkdocs
    # --strict aborts the build on any warnings
    # --verbose enables verbose output so that it's easier to see what mkdocs is doing
    # neither --strict nor --verbose are necessary if you choose not to use them
    - mkdocs build --strict --verbose
  artifacts:
    paths:
      - public
  only:
    - main
```

This job will only run when a change is made to the default branch (`main` in this case).

### Python Packages[](#python-packages)

Note the line `pip install -r requirements.txt` in the above `.gitlab-ci.yml` file. This line is installing MkDocs and any additional plugins you use to customize your site. You'll need to create a `requirements.txt` file for this script to work:

```
# Documentation static site generator & deployment tool
mkdocs>=1.1.2
```

We'll come back to this `requirements.txt` file to add a couple more packages to customize our site later.

## Customizing your site[](#customizing-your-site)

One of the benefits of using MkDocs is that it has a lot of extensions you can add on to customize your site. You can change the theme of the site, which adjusts the colors and layout. You can also add extensions that improve how your markdown notes are displayed and interacted with on the site.

### Theme[](#theme)

MkDocs includes two built-in themes (`mkdocs` and `readthedocs`), [as documented on their website](https://www.mkdocs.org/user-guide/choosing-your-theme/). There are also a lot of [community built themes](https://github.com/mkdocs/mkdocs/wiki/MkDocs-Themes) you can search through and choose to use. My current favorite theme is [Material](https://github.com/mkdocs/mkdocs/wiki/MkDocs-Themes#material-for-mkdocs-). You can install it by adding it our `requirements.txt` and choosing it as your theme in the `mkdocs.yml` configuration file, or if you are installing it locally you can install it with `pip install mkdocs-material`.

`requirements.txt`

```
# Material theme
mkdocs-material>=8.1.7
```

`mkdocs.yml`

```
theme:
  name: material
  palette:
    scheme: slate
```

I have chosen the `slate` scheme for the material theme which makes it darker. You can choose more configuration options based on [their website documentation](https://squidfunk.github.io/mkdocs-material/setup/changing-the-colors/).

### Extensions[](#extensions)

MkDocs includes [built-in extensions](https://www.mkdocs.org/user-guide/configuration/#markdown_extensions) that you can add to your `mkdocs.yml` configuration file. The [Material](https://github.com/mkdocs/mkdocs/wiki/MkDocs-Themes#material-for-mkdocs-) theme package also comes with many more extensions that we can use. Below are some of my favorite for working with Obsidian:

```
# Extensions
markdown_extensions:
  - footnotes
  - attr_list
  - pymdownx.highlight
  - pymdownx.superfences
  - pymdownx.details
  - pymdownx.magiclink
  - pymdownx.tasklist
  - pymdownx.emoji
  - admonition
  - toc:
    permalink: true
```

- `footnotes` - adds the ability to define inline footnotes, whech are then rendered below all Markdown content of a document. [See documentation here](https://squidfunk.github.io/mkdocs-material/reference/footnotes/).
- `attr_list` - allows you to add HTML attributes and CSS classes to almost every Markdown inline and block-level element with special syntax. [See documentation here](https://squidfunk.github.io/mkdocs-material/setup/extensions/python-markdown/#attribute-lists).
- `pymdownx.highlight` - adds support for syntax highlighting of code blocks. [See documentation here](https://facelessuser.github.io/pymdown-extensions/extensions/highlight/).
- `pymdownx.superfences` - allows for arbitrary nesting of code and content blocks inside each other. [See documentation here](https://facelessuser.github.io/pymdown-extensions/extensions/superfences/).
- `pymdownx.details` - allows for creating collapsible content blocks. [See documentation here](https://facelessuser.github.io/pymdown-extensions/extensions/details/).
- `pymdownx.magiclink` - provides a number of useful link related features such as auto-link HTML and emails. [See documentation here](https://facelessuser.github.io/pymdown-extensions/extensions/magiclink/).
- `pymdownx.tasklist` - adds support for tasklist syntax. [See documentation here](https://facelessuser.github.io/pymdown-extensions/extensions/tasklist/).
- `pymdownx.emoji` - adds support for inserting emoji via simple short names enclosed within colons (`:short_name:`). [See documentation here](https://facelessuser.github.io/pymdown-extensions/extensions/emoji/).
- `admonition` - allows you to create "callouts" in your documentation. [See documentation here](https://squidfunk.github.io/mkdocs-material/reference/admonitions/).
- `toc:permalink` - adds a table of contents to your page based on your markdown document, and ensures each link is a permanent link that can be reused. [See documentation here](https://python-markdown.github.io/extensions/toc/).

### Plugins[](#plugins)

MkDocs also has a community of plugins that add more features when building your site. MkDocs includes some plugins by default that you can use in the configuration file, but in order to use community plugins you have to add them to the `requirements.txt` file to be installed as packages. The following two plugins are ones that I've found useful, but you can look at [the list of community plugins here](https://github.com/mkdocs/mkdocs/wiki/MkDocs-Plugins):

```
plugins:
  - search
  - roamlinks
```

- `search` - provides a search bar at the top of your site to easily search your documents. [See documentation here](https://www.mkdocs.org/user-guide/configuration/#search).
- `roamlinks` - adds support for Obsidian's wikilinks feature. [See documentation here](https://github.com/Jackiexiao/mkdocs-roamlinks-plugin).

`requirements.txt`

```
# Wikilinks support
mkdocs-roamlinks-plugin>=0.1.3
```

If installing locally, you can install roamlinks with `pip install mkdocs-roamlinks-plugin`.

## Combining it all together[](#combining-it-all-together)

After all of the above work is done, you should have a file structure that looks like this:

```
.
├── wiki/
│   └── .obsidian
│   └── index.md
├── .gitlab-ci.yml
├── mkdocs.yml
└── requirements.txt
```

Here are the contents of the three main files that you've been editing:

`.gitlab-ci.yml`

```
image: python:3.8-slim

pages:
  stage: deploy
  script:
    - pip install -r requirements.txt
    - mkdocs build --strict --verbose
  artifacts:
    paths:
      - public
  only:
    - main
```

`mkdocs.yml`

```
site_name: My Obsidian Notes
site_url: https://group-name.gitlab.io/repo-name
site_dir: public

theme:
  name: material
  palette:
    scheme: slate

# Extensions
markdown_extensions:
  - footnotes
  - attr_list
  - pymdownx.highlight
  - pymdownx.superfences
  - pymdownx.details
  - pymdownx.magiclink
  - pymdownx.tasklist
  - pymdownx.emoji
  - admonition
  - toc:
    permalink: true

plugins:
  - search
  - roamlinks
```

`requirements.txt`

```
# Documentation static site generator & deployment tool
mkdocs>=1.1.2

# Material theme
mkdocs-material>=8.1.7

# Wikilinks support
mkdocs-roamlinks-plugin>=0.1.3
```

Now that your files are all finished, the last step is to push your changes to your GitLab repository and wait for your pipeline to finish. Once finished, you can go to [your default domain provided by GitLab](https://docs.gitlab.com/ee/user/project/pages/getting_started_part_one.html#gitlab-pages-default-domain-names) or you can [configure GitLab Pages to use a custom domain](https://docs.gitlab.com/ee/administration/pages/index.html).

Here's a screenshot of the demonstration site created in this tutorial:

![Obsidian application](https://about.gitlab.com/blog/2022/03/15/publishing-obsidian-notes-with-gitlab-pages//images/blogimages/obsidian_mkdocs_site.png)

## Is the Obsidian note-taking secure?[](#is-the-obsidian-note-taking-secure)

Users overall believe Obsidian is safe to use. One user said you [maintain full control](https://becomeawritertoday.com/obsidian-review/) over your notes and it provides the ability to encrypt your vault.

[This lawyer](https://deskoflawyer.com/secure-note-taking-apps/) maintains that Obsidian is the most-secure note-taking app available. Others claim there are [no security threats](https://thebusinessblocks.com/is-obsidian-one-of-the-most-secure-and-best-notetaking-apps/) with Obsidian and users don’t have to worry about data being lost or transferred to third parties.

Because your files are stored on your own computer, this keeps your data safe and private according to another [user](https://www.online-tech-tips.com/computer-tips/how-to-use-obsidian-as-a-personal-wiki-on-your-computer/).

### Where to find more information on Obsidian markdown[](#where-to-find-more-information-on-obsidian-markdown)

You can find more information in this [Obsidian markdown guide](https://www.markdownguide.org/tools/obsidian/). An Obsidian roadmap is available [here](https://trello.com/b/Psqfqp7I/obsidian-roadmap). Of course, you can also go to the [Obsidan website](https://obsidian.md/).

Share your Obsidian.md deployments in the comments.

[Share on Facebook](http://www.facebook.com/sharer.php?u=https://about.gitlab.com/blog/2022/03/15/publishing-obsidian-notes-with-gitlab-pages/) [Share on Twitter](http://twitter.com/share?url=https://about.gitlab.com/blog/2022/03/15/publishing-obsidian-notes-with-gitlab-pages/&text=Publishing Obsidian.md notes with GitLab Pages) [Share on LinkedIn](https://www.linkedin.com/shareArticle?mini=true&url=https://about.gitlab.com/blog/2022/03/15/publishing-obsidian-notes-with-gitlab-pages/&title=Publishing Obsidian.md notes with GitLab Pages&summary=&source=) [Share on Hacker News](https://news.ycombinator.com/submitlink?u=https://about.gitlab.com/blog/2022/03/15/publishing-obsidian-notes-with-gitlab-pages/&t=Publishing Obsidian.md notes with GitLab Pages)

[](https://www.facebook.com/gitlab "GitLab on Facebook")[](https://twitter.com/gitlab "GitLab on Twitter")[](https://www.linkedin.com/company/gitlab-com "GitLab on LinkedIn")[](https://www.youtube.com/channel/UCnMGQ8QHMAnVIsI3xJrihhg "GitLab on YouTube")

Sign up for GitLab's monthly newsletter

*

Enter your email address

By subscribing to this newsletter, I consent to GitLab sending me monthly blog emails in accordance with [GitLab's Privacy Statement](https://about.gitlab.com/privacy/). I may opt-out at anytime by clicking "unsubscribe" in the email footer or by visiting our [Communications Preference Center](https://about.gitlab.com/company/preference-center/).

Subscribe

Having trouble viewing or submitting this form? You may need to update your Cookie Preferences to allow all cookies. You might also need to allow us on your adblocker, firewall, or browser privacy settings.

Thanks for subscribing!

---

Tags: [tutorial](/blog/tags.html#tutorial)

## More to explore

[

engineering

## How to host VueJS apps using GitLab Pages



](/blog/2023/09/13/hosting-vuejs-apps-using-gitlab-pages/)[

engineering

## How to adopt a cascading merge request strategy with GitLab Flow

![Madou Coulibaly GitLab profile](https://about.gitlab.com/blog/2022/03/15/publishing-obsidian-notes-with-gitlab-pages//images/team/mcoulibaly-crop.jpg) Madou Coulibaly



](/blog/2023/08/31/cascading-merge-requests-with-gitlab-flow/)[

engineering

## How to facilitate remote design sprints

![Emily Bauman GitLab profile](https://about.gitlab.com/blog/2022/03/15/publishing-obsidian-notes-with-gitlab-pages//images/team/emilybauman-crop.jpg) Emily Bauman



](/blog/2023/08/23/remote-design-sprints/)

[All Blog Posts](/blog/)

### We want to hear from you

Enjoyed reading this blog post or have questions or feedback? Share your thoughts by creating a new topic in the GitLab community forum.

[Share your feedback](https://forum.gitlab.com/new-topic?title=Publishing Obsidian.md notes with GitLab Pages&body=&tags=blog-feedback)

## Take GitLab for a spin

See what your team could do with The DevSecOps Platform.

[Get free trial](https://gitlab.com/-/trials/new?glm_content=default-saas-trial&glm_source=about.gitlab.com)

![](https://about.gitlab.com/blog/2022/03/15/publishing-obsidian-notes-with-gitlab-pages//images/cta/gitlab-enterprise-team-member-photos.png)

Have a question? We're here to help.

[Talk to an expert](https://about.gitlab.com/sales/)

[Edit this page](https://gitlab.com/-/ide/project/gitlab-com/www-gitlab-com/edit/master/-/sites/uncategorized/source/blog/blog-posts/2022-03-15-publishing-obsidian-notes-with-gitlab-pages.html.md.erb) [View source](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/sites/uncategorized/source/blog/blog-posts/2022-03-15-publishing-obsidian-notes-with-gitlab-pages.html.md.erb)

®

### Platform

- [DevSecOps platform](/platform/)

### Pricing

- [View plans](/pricing/)
- [Why Premium?](/pricing/premium/)
- [Why Ultimate?](/pricing/ultimate/)

### Solutions

- [Digital transformation](/solutions/digital-transformation/)
- [Security & Compliance](/solutions/security-compliance/)
- [Automated software delivery](/solutions/delivery-automation/)
- [Agile development](/solutions/agile-delivery/)
- [Cloud transformation](/solutions/cloud-native/)
- [SCM](/solutions/source-code-management/)
- [CI/CD](/features/continuous-integration/)
- [Value stream management](/solutions/value-stream-management/)
- [GitOps](/solutions/gitops/)
- [Enterprise](/enterprise/)
- [Small business](/small-business/)
- [Public sector](/solutions/public-sector/)
- [Education](/solutions/education/)
- [Financial services](/solutions/finance/)

### Resources

- [Install](/install/)
- [Quick setup checklists](/get-started/)
- [Learn](/learn/)
- [Docs](https://docs.gitlab.com/)
- [Blog](/blog/)
- [Customer success stories](/customers/)
- [Remote](/company/culture/all-remote/)
- [TeamOps](/teamops/)
- [Community](/community/)
- [Forum](https://forum.gitlab.com/)
- [Events](/events/)
- [Partners](/partners/)

### Company

- [About](/company/)
- [Jobs](/jobs/)
- [Leadership](/company/team/e-group/)
- [Team](/company/team/)
- [Handbook](/handbook/)
- [Investor relations](https://ir.gitlab.com)
- [Environmental, social and governance (ESG)](/environmental-social-governance/)
- [Diversity, inclusion and belonging (DIB)](/diversity-inclusion-belonging/)
- [Trust Center](/security/)
- [Newsletter](/company/contact/)
- [Press](/press/)

### Contact us

- [Contact an expert](/sales/)
- [Get help](/support/)
- [Customer portal](https://customers.gitlab.com/customers/sign_in/)
- [Status](https://status.gitlab.com/)
- [Terms of use](/terms/)
- [Privacy statement](/privacy/)
- Cookie Preferences

- [](https://twitter.com/gitlab)
- [](https://www.facebook.com/gitlab)
- [](https://www.youtube.com/channel/UCnMGQ8QHMAnVIsI3xJrihhg)
- [](https://www.linkedin.com/company/gitlab-com)

Git is a trademark of Software Freedom Conservancy and our use of 'GitLab' is under license

View page source — Edit this page — please [contribute](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/CONTRIBUTING.md).

© 2023 GitLab B.V.

 

![Company Logo](https://cdn.cookielaw.org/logos/aa14a5c8-79e3-442a-8177-464ad850b19d/e46c1d0d-1f66-481f-bc06-5427671431da/253e6fee-c4c0-4b60-bc35-79cdae5dda32/gitlab-logo-100.png)

## Privacy Preference Center

- ### Your Privacy
    
- ### Strictly Necessary Cookies
    
- ### Functionality Cookies
    
- ### Performance and Analytics Cookies
    
- ### Targeting and Advertising Cookies
    

#### Your Privacy

When you visit any website, it may store or retrieve information on your browser, mostly in the form of cookies. This information might be about you, your preferences or your device and is mostly used to make the site work as you expect it to. The information does not usually directly identify you, but it can give you a more personalized web experience. Because we respect your right to privacy, you can choose not to allow some types of cookies. Click on the different category headings to find out more and change our default settings. However, blocking some types of cookies may impact your experience of the site and the services we are able to offer.  
[Cookie Policy](https://about.gitlab.com/privacy/cookies/)

User ID: 0beccec0-f6b6-4423-9222-3604cf7cd3b0

This User ID will be used as a unique identifier while storing and accessing your preferences for future.

Timestamp: --

#### Strictly Necessary Cookies

Always Active

These cookies are necessary for the website to function and cannot be switched off in our systems. They are usually only set in response to actions made by you which amount to a request for services, such as setting your privacy preferences, enabling you to securely log into the site, filling in forms, or using the customer checkout. GitLab processes any personal data collected through these cookies on the basis of our legitimate interest.

Cookies Details‎

#### Functionality Cookies

 Functionality Cookies

These cookies enable helpful but non-essential website functions that improve your website experience. By recognizing you when you return to our website, they may, for example, allow us to personalize our content for you or remember your preferences. If you do not allow these cookies then some or all of these services may not function properly. GitLab processes any personal data collected through these cookies on the basis of your consent

Cookies Details‎

#### Performance and Analytics Cookies

 Performance and Analytics Cookies

These cookies allow us and our third-party service providers to recognize and count the number of visitors on our websites and to see how visitors move around our websites when they are using it. This helps us improve our products and ensures that users can easily find what they need on our websites. These cookies usually generate aggregate statistics that are not associated with an individual. To the extent any personal data is collected through these cookies, GitLab processes that data on the basis of your consent.

Cookies Details‎

#### Targeting and Advertising Cookies

 Targeting and Advertising Cookies

These cookies enable different advertising related functions. They may allow us to record information about your visit to our websites, such as pages visited, links followed, and videos viewed so we can make our websites and the advertising displayed on it more relevant to your interests. They may be set through our website by our advertising partners. They may be used by those companies to build a profile of your interests and show you relevant advertisements on other websites. GitLab processes any personal data collected through these cookies on the basis of your consent.

Cookies Details‎

### Cookie List

Consent Leg.Interest

 checkbox label label

 checkbox label label

 checkbox label label

Clear

 checkbox label label

Apply Cancel

Confirm My Choices

Allow All

[![Powered by Onetrust](https://cdn.cookielaw.org/logos/static/powered_by_logo.svg "Powered by OneTrust Opens in a new Tab")](https://www.onetrust.com/products/cookie-consent/)

![](https://www.facebook.com/tr?id=1689559637958103&ev=PageView&noscript=1) ![](https://www.facebook.com/tr?id=707037893090842&ev=PageView&noscript=1) ![](https://www.facebook.com/tr?id=2212789108844434&ev=PageView&noscript=1)

Close

suggested results

![](https://bat.bing.com/action/0?ti=26083336&tm=gtm002&Ver=2&mid=7cc8c182-9f62-46f2-bfea-2c01c2e05e5e&sid=1cd294c0526c11eeb8f253079e9d2bbd&vid=1cd2ba00526c11ee9c940d6a84d9b63d&vids=1&msclkid=N&pi=918639831&lg=en-US&sw=1920&sh=1080&sc=24&tl=Publishing%20Obsidian.md%20notes%20with%20GitLab%20Pages%20%7C%20GitLab&p=https%3A%2F%2Fabout.gitlab.com%2Fblog%2F2022%2F03%2F15%2Fpublishing-obsidian-notes-with-gitlab-pages%2F&r=&lt=4500&evt=pageLoad&sv=1&rn=368458)

![](https://cdn.bizible.com/m/ipv?_biz_r=&_biz_h=802059049&_biz_u=b7a33b8f883b4c04de7ba23c935b1dd2&_biz_s=8097ae&_biz_l=https%3A%2F%2Fabout.gitlab.com%2Fblog%2F2022%2F03%2F15%2Fpublishing-obsidian-notes-with-gitlab-pages%2F&_biz_t=1694633478864&_biz_i=%0APublishing%20Obsidian.md%20notes%20with%20GitLab%20Pages%0A%7C%0AGitLab%0A&_biz_n=0&rnd=210002&cdn_o=a&_biz_z=1694633478865)![](https://cdn.bizibly.com/u?_biz_u=b7a33b8f883b4c04de7ba23c935b1dd2&_biz_s=8097ae&_biz_l=https%3A%2F%2Fabout.gitlab.com%2Fblog%2F2022%2F03%2F15%2Fpublishing-obsidian-notes-with-gitlab-pages%2F&_biz_t=1694633478868&_biz_i=%0APublishing%20Obsidian.md%20notes%20with%20GitLab%20Pages%0A%7C%0AGitLab%0A&rnd=215220&cdn_o=a&_biz_z=1694633478868)![](https://cdn.bizible.com/m/u?mapType=mkto&mapValue=id%3A194-VVC-221%26token%3A_mch-gitlab.com-1694633477213-60106&_biz_u=b7a33b8f883b4c04de7ba23c935b1dd2&_biz_s=8097ae&_biz_l=https%3A%2F%2Fabout.gitlab.com%2Fblog%2F2022%2F03%2F15%2Fpublishing-obsidian-notes-with-gitlab-pages%2F&_biz_t=1694633478868&_biz_i=%0APublishing%20Obsidian.md%20notes%20with%20GitLab%20Pages%0A%7C%0AGitLab%0A&_biz_n=1&rnd=374606&cdn_o=a&_biz_z=1694633478969)