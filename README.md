# xtrlock
xtrlock mod with some additional perks.

## Source
This is a fork of Ian Jackson's screen-locking utility. The [source](http://ftp.debian.org/debian/pool/main/x/xtrlock/xtrlock_2.7.tar.gz) is taken from Debian.

## Toppings
- To restore screen brightness after unlocking the desktop on my hardware, I needed to run a command. I have added a patch to do the same.

## Install
To compile, run:

    $ make CFLAGS="${CFLAGS} -DSHADOW_PWD" LDLIBS="-lX11 -lcrypt" xtrlock

To install, run:

    $ sudo make install

## Usage
The new option added is `-c` (for *Command*). To start `xtrlock` in screen blanking mode and set monitor backlight level to 20 after unlocking the screen, run:

    $ xtrlock -c "xbacklight -set 20" -b
