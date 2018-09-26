---
ID: 2182
post_title: slogin
author: krish
post_excerpt: ""
layout: page
permalink: http://ecosmartecloud.com/slogin/
published: true
post_date: 2015-07-21 22:38:41
---
<?php

    $creds = array();
    $creds['user_login'] = 'test70@gmail.com';
    $creds['user_password'] = '1234';
    $creds['remember'] = true;
    $user = wp_signon( $creds, false );
    if ( is_wp_error($user) )
        echo $user->get_error_message();

?>