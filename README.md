# Mercer's Openwrt source
The original codes built by OpenWrt project,\
other core codes comes from coolsnowwolf,\
for this, I am pay tribute to them.

## Notes:
To build your firmware, you need to have installed necessary packages.\
running\
`sudo apt-get update`\
then\
`sudo apt-get -y install build-essential asciidoc binutils bzip2 gawk gettext git libncurses5-dev libz-dev patch unzip zlib1g-dev lib32gcc1 libc6-dev-i386 subversion flex uglifyjs git-core gcc-multilib p7zip p7zip-full msmtp libssl-dev texinfo libglib2.0-dev xmlto qemu-utils upx libelf-dev autoconf automake libtool autopoint`

Run `./scripts/feeds update -a` to get all the latest package definitions\
defined in feeds.conf / feeds.conf.default respectively\
and `./scripts/feeds install -a` to install symlinks of all of them into\
package/feeds/.

Use `make menuconfig` to configure your image.

Simply running `make -j1 V=s` will build your firmware.\
It will download all sources, build the cross-compile toolchain, \
the kernel and all choosen applications.

To build your own firmware you need to have access to a Linux, BSD or MacOSX system\
(case-sensitive filesystem required). Cygwin will not be supported because of\
the lack of case sensitiveness in the file system.