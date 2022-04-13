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
  - `ddev drush cr`

themes/custom/solidify
yarn
yarn start



1. quick checks:
   - check if composer is working properly
      `ddev composer`
   - check if drush is working properly
      `ddev drush`
   - check if node is working properly
      `ddev exec node --version`

2. Goto [https://solidify.ddev.site/](https://solidify.ddev.site/)

3. Theme build tasks
   - Install all the dependecies
   ddev exec -d /var/www/html/web/themes/custom/drupalastic yarn
   - Start the development server and watch assets for changes to compile
    ddev exec -d /var/www/html/web/themes/custom/drupalastic yarn start
   - Build assets for production
    ddev exec -d /var/www/html/web/themes/custom/drupalastic yarn build
   - Lint assets
   ddev exec -d /var/www/html/web/themes/custom/drupalastic yarn lint
