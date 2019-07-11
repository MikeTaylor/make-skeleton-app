# make-skeleton-app

This code generates skeleton apps for the ReShare project. Each app to be generated is described by a short file of [m4](https://en.wikipedia.org/wiki/M4_(computer_language)) macros in [the `macros` directory](macros). App generation consists of copying [the `template` directory](template) to the app directory, with each occurrece of a macro replaced using m4. This can be done by running `./generate-app _appName_` and leaves the generated app directory inside the `output` directory. You can generate all the apps by running `./generate-app -a`.

Supported macros are:

* `__NAME__`: machine-readable name of the app, e.g. "shipping"
* `__TITLE__`: human-readable title of the app, e.g. "Shipping"
* `__DESCRIPTION__`: short description of the app, e.g. "Ship loaned items to borrowing library"

This allows us to quickly generate the seven new skeleton apps required by [PR-179](https://openlibraryenvironment.atlassian.net/browse/PR-179).
