Ruby on PHP (PHP extension)
=============

PHP extension for running Ruby in PHP. Eventually, this will be able to run
full rails apps. That's the goal, anyway.


Introduction
-----------
Currently, there is only ruby_eval function to be executed by receiving a code of ruby as a string.

Originally developed by github user do_aki on Scientific Linux release 6 (x86_64). Forked
by bparks and continued on ubuntu (64-bit).

ruby 1.9 or newer required (according to original README).

###sample code

    <?php
    ruby_eval(
    <<<'EOC'
      def hello
        "HELLO Ruby on PHP!!"
      end
    EOC
    );
 
    echo ruby_eval('hello()'); // say HELLO Ruby on PHP!!

### Slide (Tokyu Ruby Kaigi 04)
http://www.slideshare.net/do_aki/20111029-rubyon-php


Installation
-----------
    phpize
    ./configure
    make test
    sudo make install

and add following line to php.ini

    extension=ruby.so

