# Masoom Document

# Install Druapl by Lando

Follow the URL: https://docs.lando.dev/drupal/getting-started.html

Create a directory: $mkdir lando-site

run the command:

lando init \
    --source remote \
    --remote-url https://www.drupal.org/download-latest/tar.gz \
    --remote-options="--strip-components 1" \
    --recipe drupal9 \
    --webroot . \
    --name my-first-drupal9-app
  
# Start it up
 $lando start

# Install a site local drush
 $lando composer require drush/drush

# Install drupal
 $lando drush site:install --db-url=mysql://drupal9:drupal9@database/drupal9 -y

# List information about this app
 $lando info
 
# One time login URL
 $lando drush uli
