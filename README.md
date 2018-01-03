libcurl for iOS
=================
Build libcurl for iOS development.  
This script will generate static library for armv7 armv7s arm64 i386 and x86_64.  
Bitcode support.  
OpenSSL and Darwin native ssl support.  
  
Script only, please download libcurl from here: http://curl.haxx.se/download.html  
Tested Xcode 9.2 on macOS 10.12.6(Sierra) 
Tested curl 7.56.1 

Usage
=================
```
curl -O https://curl.haxx.se/download/curl-7.56.1.tar.gz
tar xf curl-7.56.1.tar.gz
cd curl-7.56.1
curl https://raw.githubusercontent.com/matsurowa25/build-libcurl-ios/master/build_libcurl_dist.sh |bash
......
```
Find the result libcurl-ios-dist on your desktop.


OpenSSL
=================
The script link with native ssl by default (--with-darwinssl).  
To use OpenSSL, use https://github.com/sinofool/build-openssl-ios/ to build OpenSSL for iOS first, in curl source directory run:

```bash
curl https://raw.githubusercontent.com/sinofool/build-libcurl-ios/master/build_libcurl_dist.sh openssl |bash
```

Binary (Not updated yet)
=================
Following binary is curl-7.47.1, I will release 7.54.0 binaries after a longer test.

You can find a prebuild binary (with OpenSSL) here: https://sinofool.net/dl/libcurl-ios-dist.tar.bz2

Double check the binary file before use:

```
SHA1:
993c9bb75d798a886749e7801d5f54c494dbf6fb  libcurl-ios-dist.tar.bz2

GnuPG: (My Key ID: 9BE18853)
https://sinofool.net/dl/libcurl-ios-dist.tar.bz2.sig
```
