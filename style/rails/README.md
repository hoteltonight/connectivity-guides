Rails
=====

* Avoid `member` and `collection` routes.
* Use private instead of protected when defining controller methods.
* Name date columns with `_on` suffixes.
* Name datetime columns with `_at` suffixes.
* Name time columns (referring to a time of day with no date) with `_time`
  suffixes.
* Order ActiveRecord associations alphabetically by association type, then
  attribute name. [Example][order-associations].
* Order ActiveRecord validations alphabetically by attribute name.
* Order ActiveRecord associations above ActiveRecord validations.
* Order controller contents: filters, public methods, private methods.
* Order i18n translations alphabetically by key name.
* Order model contents: constants, macros, public methods, private methods.
* Put application-wide partials in the [`app/views/application`] directory.
* Use the default `render 'partial'` syntax over `render partial: 'partial'`.
* Use `link_to` for GET requests, and `button_to` for other HTTP verbs.
* Use new-style `validates :name, presence: true` validations, and put all
  validations for a given column together. [Example][validations].

[order-associations]: /style/rails/sample.rb#L2-L4
[validations]: /style/rails/sample.rb#L6
[`app/views/application`]: http://railscasts.com/episodes/269-template-inheritance

Migrations
----------

[Sample](migration.rb)

* Set an empty string as the default constraint for non-required string and text
  fields. [Example][default example].
* Set an explicit [`on_delete` behavior for foreign keys][add_foreign_key].

[default example]: migration.rb#L6
[add_foreign_key]: http://api.rubyonrails.org/classes/ActiveRecord/ConnectionAdapters/SchemaStatements.html#method-i-add_foreign_key

Routes
------

* Avoid the `:except` option in routes.
* Order resourceful routes alphabetically by name.
* Use the `:only` option to explicitly state exposed routes.
