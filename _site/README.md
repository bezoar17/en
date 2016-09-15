This is just a customary file to populate the master branch. THis repo will serve as 
a dummy for publishing work done by me on Github using JEkyll.

BASIC FOLLOWING 
https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/


THis is for running jekyll on windows itself. This is only for setting it up , for configuring the 
repos and understanding what exactly Jekyll does there are other resources.

http://daverupert.com/2016/04/jekyll-on-windows-with-bash/
Hi. I'm having the exact same issue with Windows 10 fast release using the Linux subsystem for Windows.

As a workaround, I added the "sticky bit" to the Bundler tmp directory like this:

chmod +t -R ~/.bundle/cache

Now it works. The reason for this is that on a Windows drive, directories always have mode 777 per default.

However, this issue is caused by the Ruby tmpdir.rb trying to make sense of a world-writable directory which is not sticky.


rm gemoji and run again 
rm -r nokogiri , could not install again(1.6.8)
http://daverupert.com/2016/06/ruby-on-rails-on-bash-on-ubuntu-on-windows/ insall dependencies and then use system libraries flag.
DONE 

JEkyll website was built.
on serving the files

bezoar17@ELDER:/mnt/d/work/Github/en$ bundle exec jekyll serve
Configuration file: /mnt/d/work/Github/en/_config.yml
jekyll 3.2.1 | Error:  Could not find a JavaScript runtime. See https://github.com/rails/execjs for a list of available runtimes.
gem install execjs and reestablish the website and serve

jekyll 3.2.1 | Error:  Invalid argument - Failed to watch "/mnt/d/work/Github/en/.git/hooks": the given event mask contains no legal events; or fd is not an inotify file descriptor.

http://www.codemunki.es/2016/09/07/jekyll-on-windows-subsystem-for-linux/

bundle exec jekyll serve -w --force_polling
