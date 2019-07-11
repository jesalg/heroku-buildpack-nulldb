Heroku buildpack: NullDB
=======================

Buildpack for Rails4 review apps which require [NullDB](https://github.com/nulldb/nulldb) to pre-compile assets.

Usage
-----

Example usage:

    $ heroku create --stack cedar --buildpack http://github.com/todosmodos/heroku-buildpack-nulldb.git

    $ git push heroku master
    ...
    -----> App with app.json in the root detected
    -----> exporting DATABASE_URL='nulldb://nohost'
    ...

The buildpack will export `DATABASE_URL='nulldb://nohost'` if `DATABASE_URL` is absent.
