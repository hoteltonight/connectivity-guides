Testing
=======

* Avoid the `private` keyword in specs.
* Avoid checking boolean equality directly. Instead, write predicate methods and
  use appropriate matchers. [Example][predicate-example].
* Prefer `eq` to `==` in RSpec.
* Separate setup, exercise, verification, and teardown phases with newlines.
* Use RSpec's [`expect` syntax].
* Use RSpec's [`allow` syntax] for method stubs.
* Use `not_to` instead of `to_not` in RSpec expectations.

[`expect` syntax]: http://myronmars.to/n/dev-blog/2012/06/rspecs-new-expectation-syntax
[`allow` syntax]: https://github.com/rspec/rspec-mocks#method-stubs
[predicate-example]: predicate_tests_spec.rb

Acceptance Tests
----------------

[Sample](acceptance_test_spec.rb)

* Avoid scenario titles that add no information, such as "successfully."
* Avoid scenario titles that repeat the feature title.
* Use scenario titles that describe the success and failure paths.
* Use spec/features directory to store feature specs.
* Use spec/support/features for support code related to feature specs.

Factories
---------

* Order `factories.rb` contents: sequences, traits, factory definitions.
* Order factory attributes: implicit attributes, explicit attributes,
  child factory definitions. Each section's attributes are alphabetical.
* Order factory definitions alphabetically by factory name.
* Use one factories.rb file per project.

Unit Tests
----------

[Sample](unit_test_spec.rb)

* Don't prefix `it` block descriptions with `should`. Use [Imperative mood]
  instead.
* Use `subject` blocks to define objects for use in one-line specs.
  [Example][subject for one-liners example].
* Put one-liner specs at the beginning of the outer `describe` blocks.
* Use `.method` to describe class methods and `#method` to describe instance
  methods.
* Use `context` to describe testing preconditions.
* Use `describe '#method_name'` to group tests by method-under-test
* Use a single, top-level `describe ClassName` block.
* Order validation, association, and method tests in the same order that they
  appear in the class.

[Imperative mood]: http://en.wikipedia.org/wiki/Imperative_mood
[subject for one-liners example]: unit_test_spec.rb#6
