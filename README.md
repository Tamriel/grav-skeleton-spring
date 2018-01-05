## Setup
* Install Grav with the Admin Plugin
`wget https://getgrav.org/download/core/grav-admin/latest`<br>
`unzip latest`<br>
`rm latest`<br>
`mv grav-admin/* grav-admin/.* .`<br>
`rmdir grav-admin`<br>

* Install needed plugins for the theme
`bin/gpm install featherlight lightslider`

* Install optional plugins
`bin/gpm install git-sync`

* Install Skeleton files
`git clone https://github.com/Tamriel/spring.git user/themes/spring`

* Install the Spring Theme
`git clone https://github.com/Tamriel/spring.git user/themes/spring`<br>
`cd user/themes/spring`
`scss --load-path ../antimatter/scss --watch scss:css-compiled`

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


* Adjust structure, text and images in `user/pages/`

## Benutzeranleitung
