# 0.0.2

## Bugfix with key conflict

i19 would throw a very cryptic error when there is a conflict of keys.
For example if you this translation in your html file:

    = t("books")

and in your yml file:

    es:
      books: 'Libros'

And you later on try to add

    t("books.unread", default:"Sin leer")

i19 would just throw an NoMethodError fetch for String. Now i19 is capable of detecting this case and informs the user with a nice verbose output

# 0.0.1

Initial release of the gem
