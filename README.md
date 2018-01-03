libcurl for iOS
=================
Build libcurl for iOS development.  
This script will generate static library for armv7 armv7s arm64 and x86_64.  
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
Find the result libcurl-ios-dist on your home.


OpenSSL
=================
The script link with native ssl by default (--with-darwinssl).  
To use OpenSSL, use https://github.com/sinofool/build-openssl-ios/ to build OpenSSL for iOS first, in curl source directory run:

```bash
curl https://raw.githubusercontent.com/sinofool/build-libcurl-ios/master/build_libcurl_dist.sh openssl |bash
```
