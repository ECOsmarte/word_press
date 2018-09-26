---
ID: 987
post_title: Editing Help Screen
author: admin
post_excerpt: ""
layout: page
permalink: >
  http://ecosmartecloud.com/editing-help-screen/
published: true
post_date: 2014-07-09 08:35:41
---
<center>
<?php

if (is_user_logged_in())  {
echo '[php snippet=24]';
}
else{
echo '<h1>Please log in first</h1> <code>[s8-login-form hide_links="register"]</code>';
}
?>
</center>