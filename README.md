# Installation of compass

__os: ubuntu 14.10__

1. install ruby
sudo apt-get install ruby

        ruby version: ruby 2.1.2p95 (2014-05-08) [i386-linux-gnu]
        gem version: 2.4.8

2. install compass
problems:
- ruby official source not work well, change to taobao source use below reference:
        http://segmentfault.com/q/1010000000386278
- install compass occur error
        Building native extensions.  This could take a while...
        ERROR:  Error installing compass:
                ERROR: Failed to build gem native extension.

            /usr/bin/ruby2.1 -r ./siteconf20150913-7678-1chv6ju.rb extconf.rb
        mkmf.rb can't find header files for ruby at /usr/lib/ruby/include/ruby.h

        extconf failed, exit code 1

        Gem files will remain installed in /var/lib/gems/2.1.0/gems/ffi-1.9.10 for inspection.
        Results logged to /var/lib/gems/2.1.0/extensions/x86-linux/2.1.0/ffi-1.9.10/gem_make.out


       __solve__ :
            find solution in reference http://blog.csdn.net/cherry_sun/article/details/7743628 which suggest to
            install ruby-devel, but there is no ruby-devel lib,
            then i searched with command "apt-cache search ruby|grep dev", which find following:
                    ruby-dev - Header files for compiling extension modules for Ruby (default version)
                    ruby2.1-dev - Header files for compiling extension modules for the Ruby 2.1
            consider to the ruby version is 2.1.x, so i install ruby2.1-dev.


