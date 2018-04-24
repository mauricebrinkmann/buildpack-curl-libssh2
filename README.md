Heroku buildpack: curl with sftp (libssh2) support
==================================================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) that replaces the Ubuntu default `curl` and `libcurl` with a latest compiled version including ssl and libssh2 packages.
Purpose for this addition is to enable using sftp with curl from PHP application via autheticating Proxy like QuotaGuard or Fixie.

Usage
-----

See Heroku's documentation on [multiple buildpacks](https://devcenter.heroku.com/articles/using-multiple-buildpacks-for-an-app).

Example usage for a PHP app:

    $ heroku buildpacks:set https://github.com/heroku/heroku-buildpack-php.git
    $ heroku buildpacks:add https://github.com/frcade/heroku-buildpack-curl-libssh2.git --index 1
    $ git push heroku master
    ...

You can verify the installation using the following command:

    $ heroku run "curl --version"
