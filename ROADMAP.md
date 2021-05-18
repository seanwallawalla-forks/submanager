# Roadmap


## v0.5.0 (Late March-Early April)

* Add optional regex support for replace patterns
* Refactor to modular Python package structure with ``setup.py`` and modular components
* Use consistent API to run individual manager tasks
* Improve error handling when one request/module fails
* Use Python logging module and add many more specific logging messages
* Add baseline pre-commit and CI checks
* Publish to Github and PyPI



## v0.6.0 (April?)

* Add automod-manager module to pre-process automod config
* Add ability to re/generate popup menu of threads (e.g. in removal dialog)
* Add serviceinstaller support for automatic service installation
* Add support for updating refresh tokens after PRAW adds it upstream



## v1.0.0 (May?)

* Add proper tests and CIs
* Further improve logging and error handling as needed (better logging? verbose mode?)
* Further improve documentation



## v2.0.0 (???)

* Add support for syncing between endpoints on multiple subreddits?
* Add more desired features (sticky comments, moderation tools, more automod automation...)
* Add support for running within the Brokkr framework
    * Create wrappers for plugin(s) for session, wiki sync and megathread sync
    * Create preset(s) for plugins(s)
* Create example Brokkr system config
* Add MyPy type annotations
* Add more detailed logging, optionally integrated with Brokkr