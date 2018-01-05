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
`bin/gpm install git-sync`

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
* Change the password for each customer

* Adjust fields marked as todo in
  * `user/config/site.yaml`
  * `user/config/system.yaml`
  * `user/config/plugins/email.yaml`
  * `user/config/plugins/git-sync.yaml`

* Adjust structure, text and images in `user/pages/`. 
  * The fastest way is editing the files locally and viewing the website with a webserver (e.g. Apache) on your computer. If you are finished, push the changes to the git repo configured in the git-sync plugin.
  * To get a feeling for the file and folder formats create and edit some pages with the admin interface or look in the grav documentation.

## Benutzeranleitung für Kunden
* Todo
