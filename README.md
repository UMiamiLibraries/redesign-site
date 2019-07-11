# Redesign Blog
## To apply updates

- create a branch off of Master branch.
- create a new directory in your development environment. 
- cd into that directory and add the remote branch. 
- Use SorceTree or command line to pull that branch into the directory.
- make changes in local enviroment
- build '_site' with local config
- To build and test locally

`bundle exec jekyll build`

`bundle exec jekyll serve --incremental`

Go to: http://127.0.0.1:4000/ and verify changes.

## Build for production deployment

`bundle exec jekyll build --config=_config_prod.yml`

### Push changes up to git repo
- Add and commit files to git

### Merge branch with Master branch. 

** Make sure there are no conflicts, and there are usually conflicts!**
- Do the merge step on the git website.

## To push to production 

For Jekyll sites we SFTP the _site directory to production.

** Do not move the files to production unless you have built for production. Meaning if you did not complete this step then do it now:

`bundle exec jekyll build --config=_config_prod.yml`

SSH onto the production server and cd into /usr/local/www/redesign

Copy the _site directory over to production. Do not copy anything else over.

Verify changes online and log out of production.
