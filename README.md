# Template site for Community DAOs

Template site for community decentralised autonomous organisations. Use this template to set up your own website for your area. You view a demo of the site [here](https://247f12.github.io/DAOs/). The idea with this template site is to facilitate a uniform online identity for each community website, as well as to make it easy for anyone to set up. 

## How do I make my own site?
- Click the green button at the top of the repository that says "Use this template".
- Follow the instructions to create a new repository using the template.
- Once you have made the repository go to settings and allow github pages to serve from the master branch
	- GitHub pages is GitHub's hosting service for personal and project sites (its free) you can find out more [here](https://pages.github.com/)
- If you have a custom domain you want to serve from, you can do so also in the settings.
	- Simply add this domain under custom domain in the GitHub Pages section of your repositories settings.
	- You will then have to configure your domain provider to point to your new github pages site.

## Making it your own
- All the code is yours to edit however there are some key things that you may want to change first.

### Home page
- You can edit this through **index.md** in the **root** directory.

### Manifesto
- The manifesto page is stored in the manifesto folder, edit the **index.md** file within this folder to edit this page.

### Blog/Updates posts
- You can add blog posts by simply adding mardown files (.md) files into the **\_posts** folder.
- File names for blog posts should be date followed by the title so that they appear in the right order, eg. **2020-07-03-nameofpost.md**.
- Posts should always start with:
	
	\---

	layout: post

	title: Example Post Title

	date: 2020-07-03

	\---

- You then write your post in [markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#links)


- Blogging is powered by [jekyll](https://jekyllrb.com/), more information about that on their site.

### Resources
- The resources page is stored in the resources folder, edit the **index.md** file within this folder to edit this page.

## Create your own pages

- Create a folder in the root directory with the name of your page eg mypage.
- Create a index.md file inside your new folder, with the following in it.

	\---

	layout: page

	title: Example Page

	\---

- Any content you want on this page can be added below this header.

- Next to add our new page to the navigation bar, go to the **header.html** within _\_includes_ folder.

```html
<li class="nav-item">
  <a class="nav-link" href="{{ "/manifesto" | relative_url}}">Manifesto</a>
</li>
<li class="nav-item">
  <a class="nav-link" href="{{ "/blog" | relative_url }}">Updates</a>
</li>
<li class="nav-item">
  <a class="nav-link" href="{{ "/resources" | relative_url }}">Resources</a>
</li>
<li class="nav-item">
  <a class="nav-link" href="{{ site.github.repository_url }}">Template</a>
</li>
```

- Above is the html for the navigation bar. to add your new page simply add another in the format
```
<li class="nav-item">
	<a class="nav-link" href="{{ "/example" | relative_url }}">Template</a>
</li>
```

- Replace **example** with the name of your new page (the name of the folder you created earlier)

