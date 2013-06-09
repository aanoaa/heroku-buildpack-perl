Heroku buildpack: Perl
======================

This is a Heroku buildpack that runs `Perl/p5-hubot` application.

Usage
-----

Example usage:

    $ cpanm Hubot
    $ hubot --create /path/to/hubot
    $ cd /path/to/hubot
    $ git init ; git add . ; git commit -m "init commit"

    $ heroku create --stack cedar --buildpack https://github.com/aanoaa/heroku-buildpack-perl.git
    $ git push heroku master

    $ heroku config:add HEROKU_URL=http://your-herokuapp.herokuapp.com
    $ heroku config:add HUBOT_IRC_ROOMS='#perl-kr,#aanoaa'
    $ heroku config:add HUBOT_IRC_SERVER='irc.freenode.net'

want to use more `Hubot::Scripts::*`? describe it to `cpanfile` and
`hubot-scripts.json`

many softwares built by @miyagawa, including `cpanm` and `cpanfile`
are great. thanks. :+1:

Libraries
---------

Dependencies can be declared using `cpanfile` (recommended) or more traditional `Makefile.PL`, `Build.PL` and `META.json` (whichever you can install with `cpanm --installdeps`), and the buildpack will install these dependencies using [cpanm](http://cpanmin.us) into `./local` directory.

