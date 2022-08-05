CF Buildpack: curl 7.59 with sftp (libssh2) support
==================================================

This is a cloud foundry buildpack that replaces the Ubuntu default `curl` and `libcurl` with a latest compiled version including ssl and libssh2 packages.
Purpose for this addition is to enable using sftp with curl from PHP application via autheticating Proxy like QuotaGuard or Fixie.
Another usecase is to make use of curl 7.59 bugfix for broken requests with huge headers that was broken in 7.58 and not upgradable with cf stack cflinuxfs3 (Ubuntu 18.04 LTS).

Usage
-----

`push my-php-app -b https://github.com/mauricebrinkmann/buildpack-curl-libssh2.git -b php_buildpack`
