#[TypePlate](https://typeplate.com)

##About
Frameworks make decisions for you about how to organize, structure and design a site. Pattern libraries don't separate styling and markup, making them tough to use in a truly modular fashion. We weren't satisfied, so we made a thing that doesn’t do that.
**TypePlate** is a "typographic starter kit". We don’t make aesthetic design choices, but define **proper markup with extensible styling** for common typographic patterns. A stripped-down Sass library concerned with the appropriate technical implementation of design patterns—not how they look.

##Local Development and Contributing

###Ensuring Latest Ruby Install for RVM Users
**``.rvmc``**

Since things like Compass, Sass are Ruby Gems you'll need to have Ruby installed. Ruby is just a language and the Gems are little packages containing applications. RVM is a ruby version manager that allows users to independently manage Gems and Gemsets via the bash command ``rvm use gemset $GEM_NAME``. When navigating into the ``yeoman`` directory of this project you'll see the ``.rvmc`` file at work with this message &ndash;Have no fear and just make sure to follow the directions and type 'y' to proceed or you may type 'v' as seen below to view the contents. Bottom line&hellip;we just wanna make sure you're using the latest version of Ruby.

    ==============================================================================
    = NOTICE                                                                     =
    ==============================================================================
    = RVM has encountered a new or modified .rvmrc file in the current directory =
    = This is a shell script and therefore may contain any shell commands.       =
    =                                                                            =
    = Examine the contents of this file carefully to be sure the contents are    =
    = safe before trusting it! ( Choose v[iew] below to view the contents )      =
    ==============================================================================
    Do you wish to trust this .rvmrc file? (/Users/GrayGhost/Sites/TypePlate/yeoman/.rvmrc)
    y[es], n[o], v[iew], c[ancel]> v


    ==============================================================================
    = The contents of the .rvmrc file will now be displayed.                     =
    = After reading the file, you will be prompted again for 'yes or no' to set  =
    = the trust level for this particular version of the file.                   =
    =                                                                            =
    = Note: You will be re-prompted each time the .rvmrc file's contents change  =
    = changes, and may change the trust setting manually at any time.            =
    ==============================================================================
    (( press a key to review the .rvmrc file ))
    # Guarantee correct Ruby compatibility, for RVM users.
    rvm use 1.9.3

    ==============================================================================
    = Viewing of /Users/GrayGhost/Sites/TypePlate/yeoman/.rvmrc complete.        =
    ==============================================================================
    = Trusting an .rvmrc file means that whenever you cd into this directory,    =
    = RVM will run this .rvmrc shell script.                                     =
    = Note that if the contents of the file change, you will be re-prompted to   =
    = review the file and adjust its trust settings. You may also change the     =
    = trust settings manually at any time with the 'rvm rvmrc' command.          =
    ==============================================================================

    Do you wish to trust this .rvmrc file? (/Users/GrayGhost/Sites/TypePlate/yeoman/.rvmrc)
    y[es], n[o], v[iew], c[ancel]> y
    Using /Users/GrayGhost/.rvm/gems/ruby-1.9.3-p362

###Yeoman
We use Yeoman for this project. If you don't know what Yeoman is then you're gonna have to learn a little bit about it. We suggest [yeoman.io](http://yeoman.io) to read up on what it is and a little how to use it or feel free to check out [Yeoman on github](https://github.com/yeoman/yeoman). You can install Yeoman by running the audit script to see what you need in place:

    curl -L get.yeoman.io | bash

###Dependencies
**Stylesheets** : Sass &amp; Compass

These dependencies can be installed by executing the following bash command

    gem install compass

you can always check if they're installed by running the bash command ``gem list`` which should list all your gems installed.

###Local Server
You must run the command ``yeoman server`` from ``yeoman > app`` directory of TypePlate or else you'll see a pretty message like this.

    <FATAL> Unable to find Gruntfile. Do you need any --help? </FATAL>

###Production Build
When you're ready to build the produciton version of TypePlate's codebase you'll need to run the following command from your ``app`` directory mentioned previously.

    yeoman build

Yeoman will now place your production built ready files into a temp directory called ``dist`` and will now be viewable by running the following command from your terminal.

    yeoman server:dist

If you feel the build files from your ``yeoman:dist`` preview are satisfactory it's time to make one final adjustment to move our production ready site into the root directory of TypePlate. ``cd`` back into the root directory of TypePlate and use our custom ``rake`` build command.

    rake build

This command will copy the contents of the ``dist`` directory and place all our production site files within the root of this project. Bingo bango, easy peezy, 123. Now go drink a beer and file a pull request for your awesome changes.



###©credits
TypePlate &copy;2013 &bull; A [@grayghostvisuals](https://github.com/grayghostvisuals) and [@zakkain](https://twitter.com/zakkain) Joint™
Logo Crafting by [@TommyCreenan](https://twitter.com/TommyCreenan). Additional contributions by [@andyunleashed](https://github.com/andyunleashed) and [@chrisjeane](https://github.com/chrisjeane)