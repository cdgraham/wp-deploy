# Deploy Scripts for WordPress Plugins and Themes

These scripts expect the following directory structure where `your-plugin-slug` is 
the slug of your plugin in the WordPress plugin repository:

	your-plugin-slug
	 |
	 +-- git (your Git repo)
	 |   |
	 |   +-- .git
	 |   +-- readme.md
	 |   +-- your-plugin-slug.php
	 |   +-- ...
	 |
	 +-- svn (your SVN repo)
	 |   |
	 |   +-- assets
	 |   +-- trunk
	 |   +-- tags
	 |   +-- ...
	 |   
	 +-- wp-deploy (this repo)
	 |   |
	 |   +-- .git
	 |   +-- deploy.sh
	 |   +-- tag.sh
	 |   +-- ...

## Components
* assets.sh
* deploy.sh
* pot.sh
* README.md - this file
* setup-bash.sh - Checks git repo setup, there are no uncommited changes, and checks out wordpress.org plugin source if not done already
* tag.sh

## Setup
1. Create your plugin slug directory `mkdir <your-plugin-slug>`.
2. In your plugin slug directory clone the wp-deploy repo. `git clone https://github.com/cdgraham/wp-deploy.git`
3. Set up your plugin repo in the git directory.
4. Go to the wp-deploy directory and run the `setup-bash.sh` script. This will checkout the wordpress.org plugin with the `<your-plugin-slug>`.

### Credits

Based on ["Deploying from git to svn" by Scribu](http://scribu.net/blog/deploying-from-git-to-svn.html)

