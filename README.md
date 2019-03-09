# Customize the "New User Registration" and "Your username and password" notifications in Wordpress

When a new user is registered, WordPress sends a New User Registration notification to the admin email address in the site’s General Settings. A Your username and password email is also sent to the new user. This plugin is to be able to modify the default message sent by Wordpress.

This functionality is handled by wp_new_user_notification() located in wp-includes/pluggable.php. This is a pluggable function so it can be customized by redefining it . Unfortunately redefining it in your theme has no effect, it needs to be replaced via a plugin. It seems that plugins are loaded first, then pluggable.php, then the theme. So if your function override is in your theme, you’ll clash with the default function. 
