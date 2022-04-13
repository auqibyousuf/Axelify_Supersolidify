# Local setup guide

## Using ddev

1. Starting the project and installing the dependencies
Start the ddev project
  - `ddev start`

Download the dependencies 
  - `ddev composer install`

Import the Database
  - `ddev drush sqlc < db/solidify-db.sql`

Import the Configurations
  - `ddev drush cim`

Rebuild the cache
  - `ddev drush cr`

Compile the theme
  - `cd themes/custom/solidify`
  - `yarn`
  - `yarn start`

Log in as admin
  - `ddev drush uli`


Goto [https://solidify.ddev.site/](https://solidify.ddev.site/)
