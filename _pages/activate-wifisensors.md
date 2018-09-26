---
ID: 1097
post_title: Activate Wifi/Sensors
author: admin
post_excerpt: ""
layout: page
permalink: >
  http://ecosmartecloud.com/activate-wifisensors/
published: true
post_date: 2014-07-21 09:30:09
---
<center>
<?php //Error reporting removed to get rid of annoying header already sent error.
error_reporting(E_ERROR | E_PARSE);
ob_start();
session_start();
if (is_user_logged_in()) {
echo '[php snippet=25]
';
}
else{
echo '
<h2>To enable Email and Cell Phone notifications of urgent pool information,please become a Beta Site Member.<br><br> For details on becoming a beta site member,<a href="http://ecosmartecloud.com/wp-content/uploads/2014/07/WifiBetaSite-2.pdf" target="_blank"> Click Here.</a><br><br>If you are already a Beta Site member, please <a href="http://ecosmartecloud.com/wp-login.php">Log In</a> below.</h2>
<br><br>
<a href="http://ecosmartecloud.com/register">Click Here to Register</a>
';
}?>
</center>