# NationBuilder API PHP Library
A PHP interface for the NationBuilder API

# Requirements
Requires the OAuth2 PHP Library: https://github.com/adoy/PHP-OAuth2

# Examples
## Get an authorization code
'''php
$operation = new NationBuilderAPI( NATION_SLUG, CLIENT_ID, CLIENT_SECRET, REDIRECT_URI, null, null );
'''

## Get an authorization token
'''php
$operation = new NationBuilderAPI( NATION_SLUG, CLIENT_ID, CLIENT_SECRET, REDIRECT_URI, null, AUTH_CODE );
'''

##  Search for a user
$operation = new NationBuilderAPI( $_SESSION['slug'], CLIENT_ID, CLIENT_SECRET, REDIRECT_URI, TOKEN, 'people' );

$result = $operation->match( array( 'email' => 'example@example.com' ) );