---
ID: 93
post_title: Already Logged In
author: admin
post_excerpt: ""
layout: page
permalink: http://ecosmartecloud.com/loginpg/
published: true
post_date: 2013-05-13 17:51:41
---
<center>
<?php
error_reporting(E_ERROR | E_PARSE);
if (is_user_logged_in()) {
echo 'You are already logged in. Please Log out first.';
}
else{
echo'
<h1>Login</h1>
<code>[s8-login-form hide_links="register"]</code>';
}
?>
</center>