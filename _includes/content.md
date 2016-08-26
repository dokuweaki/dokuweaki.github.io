# Table of contents

- [About](#about)
- [Usage](#usage)
- [Install](#install)

---

# About

DokuWeaki is a bundle of plugins for DokuWiki especially targeted for agile teams, supporting agile documentation and following the philosophy of weakly typed wikis, aka as Weaki.

## Bundled plugins

- ### Comments

Enables users to add inline comments in page contents.

- ### GitHub Content Assist

This plugin lets users specify a GitHub *repository*, or a DokuWiki *page*. The contents of this repository or page will then be used to feed an autocomplete feature. While the user is typing, the suggestions mechanism of the feature will try to autocomplete the word.

- ### GitHub Integration

This plugin allows to automatically *push*, *pull* and *delete* files from GitHub when editing DokuWiki pages.

- ### JavaScript Code Transclusion

This plugin allows users to include a code snippet from GitHub in a DokuWiki page with a simple tag.

The snippet can either be an *entire file*, or a *single function* from that file.

<p style="text-align: right;"><sup><sub>* The inclusion of a complete file works for most programming languages. However, in order to include a single function the file must be a JavaScript file.</sub></sup></p>

- ### Templating

This plugin enables users to create a new DokuWiki page with one of multiple skeleton templates. There is no need to create more pages from scratch.

It is also possible to add new starting templates for future use.

---

# Usage

### Comments

Following is an example of how to use the Comments plugin. One can either use the comment interface buttons on the Wiki page, or can add/edit/delete comments manually through the page editor.

<video controls src="{{ site.baseurl }}/assets/usage-comments.mp4" width="100%">
	Sorry, your browser doesn't support embedded videos, but don't worry, you can <a href="{{ site.baseurl }}/assets/usage-comments.mp4">download it</a> and watch it with your favorite video player!
</video>

### GitHub Content Assist

To enable the content assist on a certain page click the button in the editor, fill in the dialog with the repository details you want to use. Press <kbd>CTRL</kbd> + <kbd>Space</kbd> while writing to use the plugin autocomplete feature.

<video controls src="{{ site.baseurl }}/assets/usage-content-assist.mp4" width="100%">
	Sorry, your browser doesn't support embedded videos, but don't worry, you can <a href="{{ site.baseurl }}/assets/usage-content-assist.mp4">download it</a> and watch it with your favorite video player!
</video>

### GitHub Integration

To integrate a Wiki with a GitHub repository, one needs to create a [GitHub token](https://github.com/settings/tokens) with ***repo* and *user* scopes**.

After the token is created, its details must be added to the DokuWiki settings in:

> **Admin > Configuration Settings > WeakiGithubIntegration section**

![WeakiGithubIntegration settings]({{ site.baseurl }}/assets/install-github-integration.png)

<p style="margin-top: -15px; text-align: right;"><sup><sub>* The token in the picture is not available.</sub></sup></p>

Below is a demo of a working configuration.

<video controls src="{{ site.baseurl }}/assets/usage-github-integration.mp4" width="100%">
	Sorry, your browser doesn't support embedded videos, but don't worry, you can <a href="{{ site.baseurl }}/assets/usage-github-integration.mp4">download it</a> and watch it with your favorite video player!
</video>

### JavaScript Code Transclusion

To embed code in a page from a file available at GitHub, just use one of the following tags:

```
<js-code src="{ link to GitHub file }">

<js-code src="{ link to GitHub file }@{ method name }">
```

<video controls src="{{ site.baseurl }}/assets/usage-js-code-transclusion.mp4" width="100%">
	Sorry, your browser doesn't support embedded videos, but don't worry, you can <a href="{{ site.baseurl }}/assets/usage-js-code-transclusion.mp4">download it</a> and watch it with your favorite video player!
</video>

### Templating

To create a page using a *template*, start editing the page. Edit the **url** by appending an extension to the page name. The extension must be exactly like the name of an existing template.

For example, if you want to create a page with a FAQ template:

`https://.../doku.php?id=start&do=edit`

`https://.../doku.php?id=start.faq&do=edit` - *notice the '**.faq**'*

<video controls src="{{ site.baseurl }}/assets/usage-templating.mp4" width="100%">
	Sorry, your browser doesn't support embedded videos, but don't worry, you can <a href="{{ site.baseurl }}/assets/usage-templating.mp4">download it</a> and watch it with your favorite video player!
</video>

---

# Install

## Use the right template

The DokuWeaki Plugins have been developed with the [Writr](https://www.dokuwiki.org/template:writr) template in mind.

Install it and select it in the **Configuration Settings** page.

## How to install the bundle

- [Download]({{ site.bundle-download-link }}) the bundle .zip file
- Login as **Administrator**
- Browse to the **Extension Manager**
- Select the **Manual Install** tab
- Upload the bundle .zip
- Click the **Install** button
