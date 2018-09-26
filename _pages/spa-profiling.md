---
ID: 1291
post_title: Spa Profiling
author: admin
post_excerpt: ""
layout: page
permalink: http://ecosmartecloud.com/spa-profiling/
published: true
post_date: 2014-08-06 13:36:05
---
<?php 
error_reporting(E_ERROR | E_PARSE);
if (is_user_logged_in()) {
echo '<center>
[php snippet=27]
</center>';
}

else {
echo '<center>
<h1>Please log in first</h1>
<code>[s8-login-form hide_links="register"]</code>
</center>';
}?>