When messing with the routes file don't forget to reset the router cache:
	drush ev '\Drupal::service("router.builder")->rebuild();'
	drush cache-rebuild
