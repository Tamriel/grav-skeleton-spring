## Setup
* Install Grav with the Admin Plugin<br>
`wget https://getgrav.org/download/core/grav-admin/latest`<br>
`unzip latest`<br>
`rm latest`<br>
`mv grav-admin/* grav-admin/.* .`<br>
`rmdir grav-admin`<br>

* Install needed plugins for the theme<br>
`bin/gpm install featherlight lightslider`

* Install optional plugins<br>
`bin/gpm install git-sync resize-images auto-date langswitcher`

* Install Skeleton files<br>
`git clone https://github.com/Tamriel/grav-skeleton-spring.git`<br>
`rm -rf user/pages user/config user/accounts`<br>
`mv grav-skeleton-spring/pages/ grav-skeleton-spring/config/ grav-skeleton-spring/accounts/ user/`<br>
`rm -rf grav-skeleton-spring`<br>

* Install the Spring Theme<br>
`git clone https://github.com/Tamriel/grav-theme-spring.git user/themes/spring`

* Test if the website works

* Login to the admin Interface at yoursite.de/admin with:
  * Benutzer: admin
  * Passwort: Aa1admin
* Change the username and the password

* Adjust fields marked as todo in
  * `user/config/site.yaml`
  * `user/config/plugins/email.yaml`
  
* Setup the git sync plugin in the admin interface with Bitbucket.

* Adjust structure, text and images in `user/pages/`. 
  * The fastest way is editing the files locally and viewing the website with a webserver (e.g. Apache) on your computer. If you are finished, push the changes to the git repo configured in the git-sync plugin.
  * To get a feeling for the file and folder formats create and edit some pages with the admin interface or look in the grav documentation.
  
* When using multiple languages:
  * On small devices, the total width of the menu items plus the language list is too much.
  * Therefore set in `user/themes/spring/css-compiled/template.css` in the row `@media (max-width: 1100px)` the width, at which menu items and language list become two rows. The language list will be hidden when below that width.

## Comments
* [Install](https://blog.amuehlbeier.de/isso-auf-u7/) Isso on your server
* Enable Twig processing in the Grav settings
* ` bin/gpm install jscomments`
* In the plugins settings add your ISSO Url and disable voting
* Add `{{ jscomments()|raw }}` below the text of a page
