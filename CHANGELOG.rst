Changelog
=========

Current
-------

- nothing yet


0.7.4 (2013-05-11)
------------------

- Preserve declaration order in StorageGlobber.glob() (Fix `issue #17 <https://github.com/noirbizarre/django.js/issues/17>`_)
- Fixes on localization on handling


0.7.3 (2013-04-30)
------------------

- Upgraded to jQuery 2.0.0
- Package both minified and unminified versions.
- Load minified versions (Django.js, jQuery and jQuery Migrate) when DEBUG=False


0.7.2 (2013-04-30)
------------------

- Fix `issue #16 <https://github.com/noirbizarre/django.js/issues/16>`_
- Declare package as Python 3 compatible on PyPI


0.7.1 (2013-04-25)
------------------

- Optionnaly include jQuery with ``{% django_js_init %}``.


0.7.0 (2013-04-25)
------------------

- Added RequireJS/AMD helpers and documentation
- Added Django Pipeline integration helpers and documentation
- Support unnamed URLs resolution.
- Support custom content types to be passed into the js/javascript script tag (thanks to Travis Jensen)
- Added ``coffee`` and ``coffescript`` template tags
- Python 3 compatibility


0.6.5 (2013-03-13)
------------------

- Make JsonView reusable
- Unescape regex characters in URLs
- Fix handling of 0 as parameter for Javasript reverse URLs


0.6.4 (2013-03-10)
------------------

- Support namespaces without app_name set.


0.6.3 (2013-03-08)
------------------

- Fix CSRF misspelling (thanks to Andy Freeland)
- Added some client side CSRF helpers (thanks to Andy Freeland)
- Upgrade to jQuery 1.9.1 and jQuery Migrate 1.1.1
- Do not clutter url parameters in ``js``, ``javascript`` and ``js_lib`` template tags.


0.6.2 (2013-02-18)
------------------

- Compatible with Django 1.5


0.6.1 (2013-02-11)
------------------

- Added ``static`` method (even if it's a unused reserved keyword)


0.6 (2013-02-09)
----------------

- Added basic user attributes access
- Added permissions support
- Added ``booleans`` context processor
- Added jQuery 1.9.0 and jQuery Migrate 1.0.0
- Upgraded QUnit to 1.11.0
- Added QUnit theme support
- Allow to specify jQuery version (1.8.3 and 1.9.0 are bundled)


0.5 (2012-12-17)
----------------

- Added namespaced URLs support
- Upgraded to Jasmine 1.3.1
- Refactor testing tools:
    - Rename ``test/js`` into ``js/test`` and reorganize test resources
    - Renamed ``runner_url*`` into ``url*`` on ``JsTestCase``
    - Handle ``url_args`` and ``url_kwargs`` on ``JsTestCase``
    - Renamed ``JasmineMixin`` into ``JasmineSuite``
    - Renamed ``QUnitMixin`` into ``QUnitSuite``
    - Extracted runners initialization into includable templates
- Added ``JsFileTestCase`` to run tests from a static html file without live server
- Added ``JsTemplateTestCase`` to run tests from a rendered template file without live server
- Added some settings to filter scope:
    - Serialized named URLs whitelist: ``settings.JS_URLS``
    - Serialized named URLs blacklist: ``settings.JS_URLS_EXCLUDE``
    - Serialized namespaces whitelist: ``settings.JS_URLS_NAMESPACES``
    - Serialized namespaces blacklist: ``settings.JS_URLS_NAMESPACES_EXCLUDE``
    - Serialized translations whitelist: ``settings.JS_I18N_APPS``
    - Serialized translations blacklist: ``settings.JS_I18N_APPS_EXCLUDE``
- Expose PhantomJS timeout with ``PhantomJsRunner.timeout`` attribute



0.4 (2012-12-04)
----------------

- Upgraded to jQuery 1.8.3
- Upgraded to Jasmine 1.3.0
- Synchronous URLs and context fetch.
- Use ``django.utils.termcolors``
- Class based javascript testing tools:
    - Factorize ``JsTestCase`` common behaviour
    - Removed ``JsTestCase.run_jasmine()`` and added ``JasmineMixin``
    - Removed ``JsTestCase.run_qunit()`` and added ``QUnitMixin``
    - Extract ``TapParser`` into ``djangojs.tap``
- Only one Django.js test suite
- Each framework is tested against its own test suite
- Make jQuery support optionnal into ``JsTestCase``
- Improved JsTestCase output
- Drop Python 2.6 support
- Added API documentation


0.3.2 (2012-11-10)
------------------

- Optionnal support for Django Absolute


0.3.1 (2012-11-03)
------------------

- Added JsTestView.django_js to optionnaly include django.js
- Added js_init block to runners to templates.


0.3 (2012-11-02)
----------------

- Improved ``ready`` event handling
- Removed runners from ``urls.py``
- Added documentation
- Added ``ContextJsonView`` and ``Django.context`` fetched from json.
- Improved error handling
- Added ``DjangoJsError`` custom error type


0.2 (2012-10-23)
----------------

- Refactor template tag initialization
- Provides Jasmine and QUnit test views with test discovery (globbing)
- Provides Jasmine and QUnit test cases
- Added ``Django.file()``
- Added ``{% javascript %}``, ``{% js %}`` and ``{% css %}`` template tags


0.1.3 (2012-10-02)
------------------

- First public release
- Provides django.js with ``url()`` method and constants
- Provides ``{% verbatim %}`` template tag
- Patch ``jQuery.ajax()`` to handle CSRF tokens
- Loads the django javascript catalog for all apps supporting it
- Loads the django javascript i18n/l10n tools in the page

