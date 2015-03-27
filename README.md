Résumé for Jonathan D Hartman
=============================

This is a Middleman project for a static site containing my résumé.

It is inspired by and based in part on the
[Resume Man](https://github.com/reefab/ResumeMan) template project; but uses
[Bootstrap](http://getbootstrap.com) for its layout,
[Font Awesome](http://fontawesome.io) for its icons, and
[Haml](http://haml.info) for its templating language.

It attempts to adhere to the [hResume](http://www.microformats.org/wiki/hresume)
microformat, though some parts of the spec are more ambiguous than others.

The deploy target for hosting is GitHub Pages.

The generated résumé itself (and link for PDF export) can be found
[here](http://resume.hartman.io).

Static files generated by this project include `resume.html` (the résumé data
only), `navbar.html` (a footer with links to the project source and a PDF
version of the résumé), and `index.html` (a combo of the résumé and navbar).

Requirements
------------

In addition to the dependencies listed in the included `Gemfile`, building the
PDF artifact requires [wkhtmltopdf](http://wkhtmltopdf.org). As of this
writing (2014-02-21), the 64-bit OS X version does not render icons properly,
so the 32-bit version is required.

Usage
-----

Feel free to reuse this code for your own résumé!

1. Fork this repo
2. Install [wkhtmltopdf](http://wkhtmltopdf.org) and run `bundle install`
2. Replace the data in `data/resume.yml` with our own résumé info
3. Run `bundle exec middleman server` and verify in a browser that the web
   version looks okay
4. Run `bundle exec middleman build` and verify that the PDF artifact in
  `build/resume.pdf` looks okay
5. Replace the contents of `source/CNAME` with your own desired GitHub Pages
   site and create a CNAME in your DNS pointing that name at
   `${USERNAME}.github.io`
6. Run `bundle exec middleman deploy` to build and deploy to GitHub Pages

Known Issues
------------

* There is no additional layout intelligence for the PDF export--a longer résumé
  will likely end up with an ugly page break in the middle of a section

Contributing
------------

1. Fork this repo
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Verify things look okay with the changes (`bundle exec middleman server`)
4. Commit your changes (`git commit -am 'Add some feature'`)
5. Push your branch (`git push origin my-new-feature`)
6. Create a new Pull Request

License & Authors
-----------------

- Author: Jonathan Hartman <j@hartman.io>

Copyright 2015, Jonathan Hartman

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
