# Changelog for refinerycms-acts-as-indexed

## [4.1.1]

###Dependencies

* updated version of 'acts_as_indexed'

* remove dependency on decorators as that should be added by refinerycms
* currently depending on versions of `github/anitagraham/` forks of `decorators` and `refinerycms-i18n` as the refinery branches have not been updated.
* changed version 4.1.1

### Testing
#### Rakefile: 
Changed to `File.exist?` `File.exists?` is no longer valid Ruby.
Simplified load statement

#### Spec changes
* using page_part.body rather than page_part.content as use of attribute_aliases has been made more stringent, and neither :body nor :content are attributes of page_part.

* changed css selector for testing image search to be less strict but less ambiguous.
