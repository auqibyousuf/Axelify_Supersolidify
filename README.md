# Local setup guide

## Using ddev

1. Starting the project and installing the dependencies
  - `ddev start`
  - `ddev composer install`
  - `ddev drush si`

2. quick checks:
   - check if composer is working properly
      `ddev composer`
   - check if drush is working properly
      `ddev drush`
   - check if node is working properly
      `ddev exec node --version`

3. Goto [https://axelify.ddev.site/](https://axelify.ddev.site/)

4. Theme build tasks
   - Install all the dependecies
   ddev exec -d /var/www/html/web/themes/custom/drupalastic yarn
   - Start the development server and watch assets for changes to compile
    ddev exec -d /var/www/html/web/themes/custom/drupalastic yarn start
   - Build assets for production
    ddev exec -d /var/www/html/web/themes/custom/drupalastic yarn build
   - Lint assets
   ddev exec -d /var/www/html/web/themes/custom/drupalastic yarn lint
