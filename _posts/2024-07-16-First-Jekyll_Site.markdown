---
layout: post
title:  "Initial Jekyll set up complete and hosted on github pages"
date:   2024-07-16 21:00:00 +0200
categories: Progress update
---
I have been able to sucessfully create an initial Jekyll site.

Step 1: Install the prerequisites
1. Ruby: Jekyll is built with Ruby, so you need to have Ruby installed. 
2. RubyGems: This is the Ruby package manager.
3. GCC and Make: These are required to build native extensions for Ruby gems.

I installed Ruby from [RubyInstaller](https://rubyinstaller.org/) and followed the installer.

Then added Ruby to my PATH

Step 2. Install Jekyll and Bundler
{% highlight shell %}
	gem install jekyll bundler
{% endhighlight %}
Step 3. Create a New Jekyll Site
{% highlight shell %}
	jekyll new my-portfolio
	cd my-portfolio
{% endhighlight %}
Step 4. Build the Site and Serve Locally
{% highlight shell %}
	jekyll new my-portfolio
	cd my-portfolio
{% endhighlight %}

Open 'http://localhost:4000' in your browser to see your new Jekyll site.

Step 5. Push changes to Github Repository for hosting.

Step 6. Deploy to GitHub Pages.
	6.1 Configure _config.yml for GitHub Pages:
{% highlight shell %}
url: "https://<username>.github.io"
baseurl: "/<repository>" 
{% endhighlight %}

	6.2 Build Your Jekyll Site
	- Before deploying, build your Jekyll site to generate the static HTML files:
{% highlight shell %}
	bundle exec jekyll build
{% endhighlight %}

	6.3 Commit and push to Github.

	6.4 Deploy to GitHub Pages.

	- Go to your GitHub repository on GitHub.com.
	- Navigate to the repository's Settings tab.
	- Scroll down to the GitHub Pages section.
	- Under "Source", select the branch where your Jekyll site is hosted (main or master typically).
	- If your Jekyll version is 4 or later, set the "Folder" option to /_site. If using an older version, leave it as root.

	6.5 Access Your Deployed Site.

Step 7. After configuring GitHub Pages, your site should be accessible at https://your-username.github.io/repository-name/. Replace "your-username" with your GitHub username and "repository-name" with your repository name.



Issues:

I had to install MSYS2 and run commands so I could install all the packages correctly.

I had issues getting the packages needed for Ruby and Jekyll installed as there was conflict in the verification of the install packages.

Once I was able to force those packages to install I was able to create and build a site without any errors.

