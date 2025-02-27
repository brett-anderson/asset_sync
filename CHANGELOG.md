# Change Log
All notable changes to this project will be documented in this file.
This project adheres to [Semantic Versioning](http://semver.org/).


## [Unreleased]

### Added

- Nothing

### Changed

- Nothing

### Fixed

- Nothing


## [2.15.1] - 2021-11-22

### Changed

- Update dev dependency `fog-azure-rm` to become `gitlab-fog-azure-rm`

### Fixed

- Fix YAML config file parsing with Psych v4
  (https://github.com/AssetSync/asset_sync/pull/422)


## [2.15.0] - 2021-08-05

### Added

- Add support for option `aws_acl`
  (https://github.com/AssetSync/asset_sync/pull/420)


## [2.14.2] - 2021-05-31

### Added

- Add support for setting option `google_json_key_string` in YML (not new option)
  (https://github.com/AssetSync/asset_sync/pull/419)


## [2.14.1] - 2021-05-14

### Added

- Add support for setting option `log_silently` in YML (not new option)
  (https://github.com/AssetSync/asset_sync/pull/417)


## [2.14.0] - 2021-03-31

### Added

- Add support for fog option `google_json_key_string`
  (https://github.com/AssetSync/asset_sync/pull/415)


## [2.13.1] - 2021-03-01

### Fixed

- Fix "files to be uploaded list" generation for file names with dashes
  (https://github.com/AssetSync/asset_sync/pull/414)


## [2.13.0] - 2020-12-14

### Added

- Add Backblaze B2 Cloud Storage support
  (https://github.com/AssetSync/asset_sync/pull/410)


## [2.12.1] - 2020-06-17

### Fixed

- Fix initializer template in generator
  (https://github.com/AssetSync/asset_sync/pull/404)


## [2.12.0] - 2020-06-11

### Added

- Add option `aws_session_token` to support AWS Temporary Security Credentials
  (https://github.com/AssetSync/asset_sync/pull/403)


## [2.11.0] - 2020-03-13

### Added

- Add option `remote_file_list_cache_file_path` to skip scanning remote
  (https://github.com/AssetSync/asset_sync/pull/400)


## [2.10.0] - 2020-02-26

### Added

- Add option `concurrent_uploads_max_threads` to limit number of threads for uploading files
  (https://github.com/AssetSync/asset_sync/pull/398)


## [2.9.1] - 2020-02-20

### Fixed

- Fix uploading of sprockets manifest file
  (https://github.com/AssetSync/asset_sync/pull/397)


## [2.9.0] - 2020-01-15

### Added

- Add option `concurrent_uploads` to improve speed of uploading
  (https://github.com/AssetSync/asset_sync/pull/393)


## [2.8.2] - 2019-12-27

### Changed

- Use `delete_multiple_objects` when storage is `aws`
  (https://github.com/AssetSync/asset_sync/pull/392)


## [2.8.1] - 2019-07-25

### Changed

- Removed `rubyforge_project` from gemspec
  (https://github.com/AssetSync/asset_sync/pull/386)

### Fixed

- Fixed when `fog_public` set to `false`, file were still set to be public
  (https://github.com/AssetSync/asset_sync/pull/387)


## [2.8.0] - 2019-06-17

### Added

- Add option `fog_port`
  (https://github.com/AssetSync/asset_sync/pull/385)


## [2.7.0] - 2019-03-15

### Added

- Adds JSON API support when using Google Storage
  (https://github.com/AssetSync/asset_sync/pull/381)

### Changed

- Update `AssetSync::MultiMime.lookup` to always return strings (kind of internal change)
  (https://github.com/AssetSync/asset_sync/pull/380)


## [2.6.0] - 2018-12-07

### Added

- Add option `fog_public`
  (https://github.com/AssetSync/asset_sync/pull/377)


## [2.5.0] - 2018-10-25

### Added

- Add ruby only option `file_ext_to_mime_type_overrides`
  (https://github.com/AssetSync/asset_sync/pull/374)

### Changed

- Start testing against rails 5.2, stop testing against rails 4.1

### Fixed

- Only enhance rake task assets:precompile if it's defined
  (https://github.com/AssetSync/asset_sync/commit/e1eb1a16b06fd39def1759428a2d94733915bbff)
- Avoid ruby warning due to "method redefined"
  (https://github.com/AssetSync/asset_sync/pull/371)


## [2.4.0] - 2017-12-20

### Added

- Add support for Azure Blob storage
  (https://github.com/AssetSync/asset_sync/pull/363)
- Add option: `include_manifest`
  (https://github.com/AssetSync/asset_sync/pull/365)

### Changed

- Add public API method `get_asset_files_from_manifest` split from `get_local_files` for another gem
  (https://github.com/AssetSync/asset_sync/pull/366)

### Fixed

- Nothing


## [2.3.0] - 2017-12-05

### Added

- Add options: `aws_signature_version`, `fog_host`, `fog_scheme`
  (https://github.com/AssetSync/asset_sync/pull/362)

### Changed

- Change initializer template to only run when AssetSync const defined


## [2.2.0] - 2017-07-12

### Added

- Add method `add_local_file_paths` to config for uploading additional files, like webpacker
  (https://github.com/AssetSync/asset_sync/pull/347)

### Changed

- Nothing

### Fixed

- Fix too many files open when uploading local files
  (https://github.com/AssetSync/asset_sync/pull/351)


## [2.1.0] - 2017-05-19

### Added

- Allow customization of regexp of files on target bucket to be marked as 'Cacheable'  
  so that browsers when serving the content would cache them.  
  The value can be set by `cache_asset_regexps`  

### Changed

- Only support mime-type >= 2.99,  
  which is released at the end of 2015  
- Only support activemodel >= 4.1,  
  which is released in 2014  


## [2.0.0] - 2016-12-21

### Changed

- [BREAKING] require “fog-core” instead of “fog” as runtime requirement


## [1.3.0] - 2016-11-30

### Changed

- Add regex support to always_upload (https://github.com/AssetSync/asset_sync/pull/333)
- Stop failing sliently when YAML file does not contain key for rails environment (https://github.com/AssetSync/asset_sync/pull/270)
- Stop failing sliently when YAML file cannot be parsed due to syntax error


## [1.2.1] - 2016-08-19

### Fixed

- Respect value of option `log_silently` even when `ENV['RAILS_GROUPS'] == 'assets'`


## [1.2.0] - 2016-08-17

### Added

- Support for `fog_path_style` config option (AWS only) (https://github.com/AssetSync/asset_sync/pull/302)

### Changed

- Set Expires and Cache-Control headers for .gz files (https://github.com/AssetSync/asset_sync/pull/329)

### Fixed

- Add missing runtime dependency declaration for `mime-types` to gemspec (https://github.com/AssetSync/asset_sync/pull/328)
- Update outdated error message for unknown AssetSync provider (https://github.com/AssetSync/asset_sync/pull/298)
- Allow hash digest in file name with over 32 chars (for sprockets 3+) (https://github.com/AssetSync/asset_sync/pull/315)
- Fix `config.log_silently?` (https://github.com/AssetSync/asset_sync/pull/324)
- Stop using deprecated Ruby API (https://github.com/AssetSync/asset_sync/pull/276)


## v1.1.0 / 2014-08-13

Version 1.1.0 (Toby Osbourn <tosbourn@rumblelabs.com>)

Changes:

* 1 Change

    * Bumping master to 1.1.0 - preparing to update RubyGems

## v0.5.6 / 2014-08-12

Version 0.5.6 (Toby Osbourn <tosbourn@rumblelabs.com>)

Changes:

* 1 Change

    * Merged in support for optimized fog loading

## v0.5.5 / 2014-08-12

Version 0.5.5 (Toby Osbourn <tosbourn@rumblelabs.com>)

Changes:

* 2 Nominal Changes

    * Merged some spec changes to get Travis to pass the build correctly
    * Support using AWS IAM Roles

## v0.5.1 / 2012-10-22

Version 0.5.1 (David Rice <me@davidjrice.co.uk>)

Changes: 

* 5 Nominal Changes

    * Add a CHANGELOG.md (as generated by vclog -r -f markdown
    * Improve documentation on ignored_files config option
    * Allow failure of specs against ruby-head and jruby-head
    * Merge pull request #115 from demirhanaydin/patch-1
    * Merge support for always providing mime_type #93 from patdeegan/master



## v0.5.0 / 2012-08-23

Version 0.5.0 (David Rice <me@davidjrice.co.uk>)

Changes:

* 8 Nominal Changes

    * Merge branch 'sinatra' of github.com:rumblelabs/asset_sync into sinatra
    * Version 0.5.0, sinatra / rack support
    * Some refactoring to further remove dependency on Rails, add spec for railsless configuration
    * Update readme.
    * Add public_path and prefix config options so asset_sync can be used outside Rails.
    * Some refactoring to further remove dependency on Rails, add spec for railsless configuration
    * Merge branch 'ejholmes/sinatra' into sinatra
    * Version 0.4.3, removed dependency on Rails Time additions


## v0.4.3 / 2012-08-19

Version 0.4.3 (David Rice <me@davidjrice.co.uk>)

Changes:

* 21 Nominal Changes

    * Refactor cache control and expiry hearder definition to use same value of one year
    * Merge pull request #94 from karlfreeman/time
      
      Remove Rails time dependency
    * Allow failures in ruby-head
    * Merge pull request #88 from potomak/patch-1
      
      Fix defined? syntax
    * Merge pull request #95 from bbhoss/patch-1
      
      Fix syntax error in documentation
    * Describe using S3 HTTPS better
    * Fix syntax error
    * remove Rails time dependency
    * Update readme.
    * Add public_path and prefix config options so asset_sync can be used outside Rails.
    * Fix defined? syntax
    * Force build on travis
    * Get specs running under jruby and travis /cc @headius :)
    * Ignore ds_store
    * Add jruby-openssl gem to get tests passing on jruby
    * test all the things
    * Add travis config for rbx
    * Merge branch 'master' of github.com:rumblelabs/asset_sync
    * Update README for installing on heroku, labs is no-longer a plugin
    * Merge pull request #75 from mscottford/master
      
      Update asset_host configuration in README to not rely on request object
    * Version 0.4.2, allow configuration of an array of strings or regex for files to ignore uploading. #euruko


## v0.4.2 / 2012-06-02

Version 0.4.2 (David Rice <me@davidjrice.co.uk>)

Changes:

* 7 Nominal Changes

    * Remove errant puts from spec
    * Merge
    * Add option to configure ignored_files through YAML config file
    * Removes errant end in the asset_host config example.
    * Updates README to suggest a different asset_host configuration
      
      The previous version will fail in some cases because a request is not always available during asset compilation.
    * Fix Fog warnings when running specs.
    * Version 0.4.1, allow programatic disabling of AssetSync.config.enabled


## v0.4.1 / 2012-05-04

Version 0.4.1 (David Rice <me@davidjrice.co.uk>)

Changes:

* 10 Nominal Changes

    * Update docs
    * Don't default to disabled if ASSET_SYNC_ENABLED env var is not specified.
    * Add option to ignore files
    * Add support for ASSET_SYNC_ENABLED with env vars.
    * Oops, should have used the accessor
    * Add support for enabled in the yaml config.
    * Add specs for AssetSync.enabled? configured through the initializer.
    * Make it possible to turn off AssetSync...
      
      Useful when precompiling to export to a hybrid mobile app such as PhoneGap.
      Would fix issue #66.
    * How many times will I forget to update the release date? many
    * Version 0.4.0, google storage support. Allow force upload of all or selected files. Travis CI enabled


## v0.4.0 / 2012-04-26

Version 0.4.0 (David Rice <me@davidjrice.co.uk>)

Changes:

* 22 Nominal Changes

    * Add google storage options to built in initializer to allow config via ENV vars
    * Add google storage configuration to README
    * fix case on google provider in generator
    * added google storage tests
    * added google storage generators
    * add attr_accessor for google keys
    * add support for fog gems google storage option
    * Oh, travisci will build an orgs repos if you configure the webhookd. Use rumblelabs/asset_sync as build status
    * Merge branch 'master' into levent/feature/overwrite_specific_remote_files
    * Use my travis-ci build in README
    * Merge pull request #69 from levent/integrate_travis
      
      Integrate Travis CI
    * Merge branch 'integrate_travis' into feature/overwrite_specific_remote_files
    * Specs for uploading assets
    * Travis build logo
    * Setting up for Travis
    * Updated README
    * always_upload config option added
    * gitignore *.swp (for vim)
    * Add ability to ignore remote files
    * Correct name of specs
    * Allows specifying an array of assets to always upload to remote
    * Version 0.3.2, set content encoding header for .gz files


## v0.3.2 / 2012-04-18

Version 0.3.2 (David Rice <me@davidjrice.co.uk>)

Changes:

* 11 Nominal Changes

    * Remove trailing comma
    * Merge pull request #57 from nathanhumbert/master
      
      Set Content-Encoding for gzip files when config.gzip? is not true
    * Merge pull request #59 from kamui/master
      
      Use Rails.public_path and Pathname#join for path concat and string interpolation
    * Merge pull request #55 from manuelmeurer/patch-1
      
      Remove comments taken from another gem
    * Dir.chdir to path first to avoid a map call and path string slicing
    * add Rails.public_path stub and make Rails.root return Pathname class to match Rails behavior
    * Rails.root returns a Pathname, use Pathname#join instead of File.join and string interpolation
    * use Rails.public_path instead of concat Rails.root and 'public'
    * Set Content-Encoding for gzip files when config.gzip? is not true
      
      This allows a S3 bucket served via CloudFront to properly handle the
      Accept-Encoding request header.
    * Remove comments taken from another gem
    * Merge branch 'master' of github.com:rumblelabs/asset_sync


## v0.3.1 / 2012-03-07

Version 0.3.1 (David Rice <me@davidjrice.co.uk>)

Changes:

* 6 Nominal Changes

    * Version 0.3.1, improve logging of asset_sync configuration and sync events
    * Remove some debugging stuffs
    * Improve logging during asset_sync progress.
    * Separate log and warn message, should not mess up heroku precompile thread as it watches STDERR for output.
    * Improve logging, only log to STDERR if RAILS_GROUPS=assets.
    * Version 0.3.0, all configuration can be managed via env variables, improve docs on configuration


## v0.3.0 / 2012-03-07

Version 0.3.0 (David Rice <me@davidjrice.co.uk>)

Changes:

* 10 Nominal Changes

    * Merge pull request #50 from hampei/master
      
      made gzip_compression settable via ENV
    * namespaced the ENV gzip option: ASSET_SYNC_GZIP_COMPRESSION. added option to readme
    * made gzip_compression settable via ENV
    * Typo
    * Improve documentation
    * Version 0.2.12, fix the asset_sync rake task enhancement in Rails 3.2 (still supporting earlier releases)
    * Turns out this was an issue with Rails handling of the config.assets.digest parameter
    * When running rake assets:precompile this config variable is modified by Rails
    * So it therefore cannot be depended on to test wether to enhance the nondigest task or not
    * The solution is to always enhance assets:precompile:nondigest if it exists.


## v0.2.9 / 2012-01-30

Version 0.2.9 (David Rice <me@davidjrice.co.uk>)

Changes:

* 3 Nominal Changes

    * Merge pull request #42 from genuitytech/master
      
      Now correctly setting config.fog_region.
    * Now correctly setting config.fog_region.
    * Version 0.2.8, improve http headers. Add far future expires and cache control, public.


## v0.2.8 / 2012-01-27

Version 0.2.8 (David Rice <me@davidjrice.co.uk>)

Changes:

* 2 Nominal Changes

    * Add far future expires header
    * Version 0.2.7, Rails 3.2 compatibility, default Rake task improved


## v0.2.7 / 2012-01-25

Version 0.2.7 (David Rice <me@davidjrice.co.uk>)

Changes:

* 2 Nominal Changes

    * Merge branch 'rails-3-2'
    * Version 0.2.6, Rails 3.2 compatibility, default Rake task improved


## v0.2.6 / 2012-01-25

Version 0.2.6 (David Rice <me@davidjrice.co.uk>)

Changes:

* 3 Nominal Changes

    * Doc
    * Add Rails 3.2 compatible rake task
    * Fix issue #38 for when  Rails.config.assets.prefix starts with a slash.


## v0.2.5 / 2012-01-10

Version 0.2.5 (David Rice <me@davidjrice.co.uk>)

Changes:

* 1 Nominal Changes

    * Version 0.2.4, Support for Rails.config.assets.prefix


## v0.2.4 / 2012-01-06

Version 0.2.4 (David Rice <me@davidjrice.co.uk>)

Changes:

* 5 Nominal Changes

    * Merge pull request #35 from siliconsalad/config_assets_prefix
      
      Rails.config.assets.prefix used for sync
    * added test with Rails.config.assets.prefix set
    * Rails.config.assets.prefix used for sync (instead of hardcoded 'assets' value)
    * specs now use shared context to mock Rails and fixed pending tests that were failing
    * Version 0.2.3, Rackspace London support


## v0.2.3 / 2011-12-06

Version 0.2.3 (David Rice <me@davidjrice.co.uk>)

Changes:

* 3 Nominal Changes

    * Merge pull request #28 from robink/master
      
      Rackspace London support
    * Only merge racksace_auth_url to fog config if defined
    * Bump date for release


## v0.2.2 / 2011-11-29

Version 0.2.2 (David Rice <me@davidjrice.co.uk>)

Changes:

* 10 Nominal Changes

    * Version 0.2.2: add fail_silently config option to avoid heroku installing the rails31_enable_runtime_asset_compilation, fixes issues #24, #29
    * Further explanation of fail_silently option
    * Merge pull request #29 from neilmiddleton/master
      
      Allow precompile to fail quietly on heroku
    * Update README, and generator templates
    * Changes as discussed in PR#29
    * Disable pre-compilation on Heroku.
    * Updated README and generators
    * Added support for specifying rackspace_auth_url (then the possibility to use Rackspace London)
    * Fixed typo in readme
    * Updated version and release date


## v0.2.12 / 2012-03-04

Version 0.2.12 (David Rice <me@davidjrice.co.uk>)

Changes:

* 1 Nominal Changes

    * Version 0.2.11, minor fix to YAML loading and improved docs


## v0.2.11 / 2012-03-04

Version 0.2.11 (David Rice <me@davidjrice.co.uk>)

Changes:

* 7 Nominal Changes

    * Merge pull request #48 from samsoffes/patch-1
      
      Fix Heroku Labs plugin URL and add code coloring to readme.
    * Fix Heroku Labs plugin URL and add code coloring to readme.
    * Merge pull request #47 from dbalatero/dont_read_yml_file_every_time
      
      Cache the YML config to avoid multiple file reads.
    * Cache the YML config to avoid multiple file reads.
    * Fix documentation typos
    * Move old known issues about heroku ENV variables to a docs folder, write new content referencing the recommended use of user_env_compile
    * Version 0.2.10, fix handling of non standard Rails.config.assets.manifest path


## v0.2.10 / 2012-02-16

Version 0.2.10 (David Rice <me@davidjrice.co.uk>)

Changes:

* 5 Nominal Changes

    * Add an AssetSync.log method for outputing sync config failure so we can stub it out easily in tests
    * Merge pull request #44 from dbalatero/fix_nonstandard_manifest_location
      
      Fixes asset_sync to correctly read manifest.yml files.
    * Fixes asset_sync to correctly read manifest.yml files.
      
      Rails.config.assets.manifest only points to the directory that contains
      the manifest.yml file:
      
      https://github.com/rails/rails/blob/226783d1e8891a38d4a61017952528970dba903d/actionpack/lib/sprockets/railtie.rb#L36
    * Add hack, seems required for some applications on push to Heroku, not for others
    * Version 0.2.9 fix bug in internal initializer


## v0.2.1 / 2011-11-21

Version 0.2.1 (Phil <phil.mcclure@gmail.com>)

Changes:

* 4 Nominal Changes

    * Only configure with ENV vars if initializer and yml file do not exist
    * Typo in yaml, underscore need not be escaped here
    * Fix readme
    * Version 0.2.0


## v0.2.0 / 2011-11-15

Version 0.2.0 (David Rice <me@davidjrice.co.uk>)

Changes:

* 15 Nominal Changes

    * Add upgrade notice to README
    * Use fog directory
    * Merge
    * Fix readme
    * Tidy readme
    * Get AWS or Rackspace generators working correctly
    * Remove generated rake task, no need
    * Improve generators to generate AWS or Rackspace compatible initializer or yml
    * Prepare 0.2.0 for release
    * Convert readme and generators to new config options
    * Fix fog_options
    * Fix typo
    * Fix bug
    * Working on migrating the exposed config variables to reflect fog, add in a start on rackspace support. Write more specs, tidy up and document config
    * Add specs for manifest config


## v0.1.9 / 2011-11-06

Version 0.1.9 (David Rice <me@davidjrice.co.uk>)

Changes:

* 37 Nominal Changes

    * Document gzip compression
    * Add note about gzip_compression
    * Add spec to test config defaults gzip_compression to false
    * Add gzip compression info to generated asset_sync.rb or .yml. Fix .yml example with new config settings
    * Update gemspec
    * Update docs to note that rake task is no longer generated within the app.
    * Add todo
    * Add % symbol for clarity
    * Output % savings when uploading gzipped files. Only use gzipped files if the compressed version is actually smaller than the original.
    * Tidy readme
    * Get AWS or Rackspace generators working correctly
    * Remove generated rake task, no need
    * Improve generators to generate AWS or Rackspace compatible initializer or yml
    * Prepare 0.2.0 for release
    * Convert readme and generators to new config options
    * Fix fog_options
    * Fix bug
    * Fix typo
    * Working on migrating the exposed config variables to reflect fog, add in a start on rackspace support. Write more specs, tidy up and document config
    * Add spec for gzip? config method
    * Reorder logic to execute quicker if gzip? compression disabled and ignore .gz uploads correctly
    * Ignore .gz assets if we are in gzip_compression mode
    * Do not set a Vary: Accept-Encoding header, S3 does not support at all
    * Try setting vary header a different way
    * Set http header Vary: Accept-Encoding when storing gzipped assets to S3
    * Add todo
    * Refactor to computed path
    * Add path
    * Instead of overwriting the original file when processing the .gz, overwrite the original if a gz file exists to avoid any issues with whichever order files are processed in
    * Bump version (no release just yet)
    * Only handle gzip files specially if we have configured gzip_compression
    * Overwrite original files with gzipped equivalent, improve logging to show GZIP in action, make it a configurable option, config.gzip_compression that defaults to false
    * Upload GZIP compressed assets nicely to S3 with correct content type and encoding.
    * Refactor upload method to make enhancing nicer
    * Merge pull request #12 from bobbrez/master
      
      Minor correction to README for generated YAML file path.
    * Correcting location of generated yml in README
    * Comment out unnecessary logic for now


## v0.1.8 / 2011-10-17

Version 0.1.8 (David Rice <me@davidjrice.co.uk>)

Changes:

* 4 Nominal Changes

    * Don't log any debugging info v0.1.8 should add a debug mode in future
    * Fix specs, only require asset_sync engine and railtie if Rails is initialized
    * Improve docs
    * Tidy up for release of Rails 3.1.1 support.


## v0.1.7 / 2011-10-15

Version 0.1.7 (David Rice <me@davidjrice.co.uk>)

Changes:

* 6 Nominal Changes

    * Merge pull request #7 from hone/6_rails3.1.1
      
      Rails 3.1.1 Compatability
    * rails 3.1.1 support
    * fix typo
    * Update the generated yml config with a staging environment, use defaults more. Engine within asset sync doesn't appear to be ran even with :group => :assets in the definition. Add railtie to allow setting config.asset_sync configuration within a rails application.rb, this and moving the initializer style of config seems to work for Rails 3.1.1, also so does purely relying on the YAML config
    * New version of asset_sync to work around Rails 3.1.1 issues. Test if config/initializers/asset_sync.rb exists and load that, otherwise provide a default initializer that is configurable with environment variables. Then merge in settings if config/asset_sync.yml is found. Add the asset_sync.rake in to lib/tasks so it is autoloaded and don't bother generating it anymore
    * Bugfix


## v0.1.6 / 2011-09-26

Version 0.1.6 (David Rice <me@davidjrice.co.uk>)

Changes:

* 1 Nominal Changes

    * Fix gemfile


## v0.1.5 / 2011-09-26

Version 0.1.5 (David Rice <me@davidjrice.co.uk>)

Changes:

* 5 Nominal Changes

    * Should raise storage error if AWS S3 bucket is not found. Version 0.1.5
    * explain further
    * Merge branch 'master' of github.com:rumblelabs/asset_sync
    * List known issues with heroku and possible work arounds
    * Should raise error with no configuration


## v0.1.4 / 2011-08-30

Version 0.1.4 (David Rice <me@davidjrice.co.uk>)

Changes:

* 2 Nominal Changes

    * Require dependancy of active_model, add config validation, better specs, version 0.1.4
    * Tidied up read me with a DRYer use of AWS_BUCKET for asset_host.


## v0.1.3 / 2011-08-27

Version 0.1.3 (Simon Hamilton <shamilton@rumblelabs.com>)

Changes:

* 1 Nominal Changes

    * Bump version for release


## v0.1.2 / 2011-08-25

Version 0.1.2 (Simon Hamilton <shamilton@rumblelabs.com>)

Changes:

* 2 Nominal Changes

    * Removed public from cache control. May be causing a problem with uploads
    * Bump version for release


## v0.1.10 / 2011-11-15

Version 0.1.10 (David Rice <me@davidjrice.co.uk>)

Changes:

* 7 Nominal Changes

    * Improve manifest configuration by making it a boolean option only, it will automatically use the configured manifest path if different from the default. Add documentation to readme about the new option and upgrade generated configs.
    * Merge pull request #20 from agworld/e26f5ca36dee1c2196653268ed6bb38c0226e4d2
      
      Fixes issues #16, #17, #18 and #19
    * fixes https://github.com/rumblelabs/asset_sync/issues/19
    * Implements https://github.com/rumblelabs/asset_sync/issues/17
    * fixes https://github.com/rumblelabs/asset_sync/issues/18
    * fixes https://github.com/rumblelabs/asset_sync/issues/16
    * Merge branch 'gzip-compression'


## v0.1.1 / 2011-08-24

Version 0.1.1 (Simon Hamilton <shamilton@rumblelabs.com>)

Changes:

* 5 Nominal Changes

    * Merge pull request #4 from jsmestad/patch-1
      
      [BUGFIX] Add support for 'existing_remote_files' configuration in YAML fi
    * Verbose output about the delete process.
    * Condense logic on keep
    * [BUGFIX] Add support for 'existing_remote_files' configuration in YAML file.
    * Version 0.1.0 ready


## v0.1.0 / 2011-08-22

Version 0.1.0 (David Rice <me@davidjrice.co.uk>)

Changes:

* 1 Nominal Changes

    * Merge 0.0.7 from master into new refactor branch


## v0.0.7 / 2011-08-22

Version 0.0.7 (David Rice <me@davidjrice.co.uk>)

Changes:

* 9 Nominal Changes

    * Added Cache-control header (1 year, public) on uploaded files
    * Update README to reflect new configuration styles
    * Extract all file manipulation methods to a storage class, update generator templates, fix a few bugs.
    * Config class working, specs added, still @wip
    * Refactoring
    * Get config working and loading yml or the initializer
    * small additions
    * @wip working on extracting out a configuration class and allow config via an initializer alone, also support yml file usage for when that is useful
    * merge config changes


## v0.0.6 / 2011-08-06

Version 0.0.6 (Simon Hamilton <shamilton@rumblelabs.com>)

Changes:

* 1 Nominal Changes

    * Include ERB template rendering of yml. v0.0.5


## v0.0.5 / 2011-08-05

Version 0.0.5 (David Rice <me@davidjrice.co.uk>)

Changes:

* 3 Nominal Changes

    * now it parses the YAML file with ERB.
    * Set gem date for release
    * 0.0.4 Release


## v0.0.4 / 2011-08-05

Version 0.0.4 (David Rice <me@davidjrice.co.uk>)


## v0.0.3 / 2011-07-31

Version 0.0.3 (David Rice <me@davidjrice.co.uk>)

Changes:

* 1 Nominal Changes

    * Added homepage to gemspec


## v0.0.2 / 2011-07-31

Version 0.0.2 (Simon Hamilton <shamilton@rumblelabs.com>)

Changes:

* 7 Nominal Changes

    * Added a rails generator to install the rake task and the config.  Just do "rails generate asset_sync:install"
    * Updated readme
    * Getting ready to release the gem
    * Revert "remove version file"
      
      This reverts commit 7ebd853947b8d5f3b6e81f96535dfce843f2c855.
    * remove version file
    * Initial commit
    * Initial commit


## HEAD / 2012-08-27

Current Development (David Rice)

Changes:

* 2 Nominal Changes

    * Improve documentation on ignored_files config option
    * Merge branch 'sinatra'


[Unreleased]: https://github.com/AssetSync/asset_sync/compare/v2.15.1...HEAD
[2.15.1]: https://github.com/AssetSync/asset_sync/compare/v2.15.0...v2.15.1
[2.15.0]: https://github.com/AssetSync/asset_sync/compare/v2.14.2...v2.15.0
[2.14.2]: https://github.com/AssetSync/asset_sync/compare/v2.14.1...v2.14.2
[2.14.1]: https://github.com/AssetSync/asset_sync/compare/v2.14.0...v2.14.1
[2.14.0]: https://github.com/AssetSync/asset_sync/compare/v2.13.1...v2.14.0
[2.13.1]: https://github.com/AssetSync/asset_sync/compare/v2.13.0...v2.13.1
[2.13.0]: https://github.com/AssetSync/asset_sync/compare/v2.12.1...v2.13.0
[2.12.1]: https://github.com/AssetSync/asset_sync/compare/v2.12.0...v2.12.1
[2.12.0]: https://github.com/AssetSync/asset_sync/compare/v2.11.0...v2.12.0
[2.11.0]: https://github.com/AssetSync/asset_sync/compare/v2.10.0...v2.11.0
[2.10.0]: https://github.com/AssetSync/asset_sync/compare/v2.9.1...v2.10.0
[2.9.1]: https://github.com/AssetSync/asset_sync/compare/v2.9.0...v2.9.1
[2.9.0]: https://github.com/AssetSync/asset_sync/compare/v2.8.2...v2.9.0
[2.8.2]: https://github.com/AssetSync/asset_sync/compare/v2.8.1...v2.8.2
[2.8.1]: https://github.com/AssetSync/asset_sync/compare/v2.8.0...v2.8.1
[2.8.0]: https://github.com/AssetSync/asset_sync/compare/v2.7.0...v2.8.0
[2.7.0]: https://github.com/AssetSync/asset_sync/compare/v2.6.0...v2.7.0
[2.6.0]: https://github.com/AssetSync/asset_sync/compare/v2.5.0...v2.6.0
[2.5.0]: https://github.com/AssetSync/asset_sync/compare/v2.4.0...v2.5.0
[2.4.0]: https://github.com/AssetSync/asset_sync/compare/v2.3.0...v2.4.0
[2.3.0]: https://github.com/AssetSync/asset_sync/compare/v2.2.0...v2.3.0
[2.2.0]: https://github.com/AssetSync/asset_sync/compare/v2.1.0...v2.2.0
[2.1.0]: https://github.com/AssetSync/asset_sync/compare/v2.0.0...v2.1.0
[2.0.0]: https://github.com/AssetSync/asset_sync/compare/v1.3.0...v2.0.0
[1.3.0]: https://github.com/AssetSync/asset_sync/compare/v1.2.1...v1.3.0
[1.2.1]: https://github.com/AssetSync/asset_sync/compare/v1.2.0...v1.2.1
[1.2.0]: https://github.com/AssetSync/asset_sync/compare/v1.1.0...v1.2.0
