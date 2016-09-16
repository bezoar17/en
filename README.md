http://philguo.com/blog/2016/hexo-on-github-pages/ 

GOOD ONE FOR GITHUB PAGES .

This is just a customary file to populate the master branch. THis repo will serve as 
a dummy for publishing work done by me on Github using JEkyll.

BASIC FOLLOWING and Jekyll understanding
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

Version 1607 (OS BUild 14393.105) destroyed boot loader.
http://www.omgubuntu.co.uk/2016/08/windows-10-anniversary-update-delete-partition reports of deleted os also, mine did not show that
also bluetooth stopped working after this update just wasn't showing but then download driver atheros(win 10 latest) after multiple restarts.
>>== Windows has stopped this device because it has reported problems. (Code 43). -- uninstalled the module , it went away.

We can fix it from http://windowsreport.com/anniversary-update-destroys-boot-loader-dual-boot-config/

gh-pages is never merged with master for JEkyll usage.



<<<===================================================================================================>>>

Try heko , install git scm on windows and node js on ubuntu bash .. Try out the fix for ubuntu boot loader, Pracstising on typingclub.com
Try out expii also 

NODE AND NPM ON UBUNTU BASH 

To install Node.js, type the following command in your terminal:

1
sudo apt-get install nodejs
Then install the Node package manager, npm:

1
sudo apt-get install npm
Create a symbolic link for node, as many Node.js tools use this name to execute.

1
sudo ln -s /usr/bin/nodejs /usr/bin/node



<<<<<<<<<<<			Hexo			>>>>>>>
Hexo is JS based while Jekyll is ruby based . 

Hexo can be used with node and git . jekyll needed ruby and rails.
TO publish to a repo just make the folder in the repo.
Other than that , you can use it elseware and try it out locally.
http://jdpaton.github.io/2012/11/05/setup-hexo/ This tells us that along with the documentation at hexo.io

Hexo :(First of all read the docs at hexo website to understand what it is.)
https://hexo.io/docs/ common thingsa are starting , deploy , generate , server and plugins,themes etc.

http://blog.giacomocerquone.com/jekyll-vs-hexo/

Pre req: node and git

hexo trial locally ---->>
ubuntu-bash/hexo/trial

npm install hexo-cli -g :installing hexo cli
hexo init trial
cd trial
: creates a trial dir for hexo
npm install hexo-server --save :   to install server
npm install hexo --save
install everything in 
https://github.com/hexojs/hexo/wiki/Migrating-from-2.x-to-3.0
hexo server : does not work in win 10 bash 
but hexo server -s does work. https://github.com/gulpjs/gulp/issues/660



http://philguo.com/blog/2016/hexo-on-github-pages/

<GITHUB PAGES WITH HEXO>


<HEXO ON WINDOWS _ ANS GIT >
MIght have to try out hexo in windows itself.

FOllowing this.
http://www.bravo-kernel.com/2015/10/setting-up-hexo-on-windows/
Install git-scm , not directly in cmd but present in github's git shell.
RUn any and everything from git-bash or from cmd directly.
instead of /mnt/d ....
use /d/work/ in git bash.
node and npm are already installed.
hexo is installed as mentioned in the website.
server serves all files. hexo serve-s serves only files in public.
which is created when generate is called.

SO in review.
Hexo requires git,node and npm to be installed.
in ubuntu bash and windows ensure that.
now for ubuntu env use bash and windows use cmd.
hexo's website is basically a folder.
which if kept in gh-pages branch of a project will be served on the net.
now 
we can use hexo in both of the bash and cmd.
now when we add a page or blog in hexo , server will update the website with latest update,
this requires to constantly check the files which is not implemented correctly in bash emulation in windows.
So it works fine in cmd.
OR we can run generate command which converts it to static pages and keep it in public folder.
This can be server using hexo serve - s which runs on both cmd and bash for windows.
But only the pages which have been generated will show up , latest changes without generate command won't;

NOw , first of all , if we want to deploy the website in git repo (remote) the deploy command should run generate also without it , it does not work.

So to publish the website code , deploy is only used(the initial settings of the repo is configured at the beginning.)

Now to locally develop the changes and test. --->
we can add a page, blog whatever , and if hexo server is running we will se the change directly on localhost:4000 as the server keeps 
track of the change. THIS IS ONLY POSSIBLE CURRENTLY FOR CMD(native windows.)

to use bash in same effect. We have to run hexo generate && hexo serve -s every time a change is done and then we see the changes in the 
localhost:4000.
