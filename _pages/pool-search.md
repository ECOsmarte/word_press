---
ID: 256
post_title: Pool Search By Username
author: Zhongyu He
post_excerpt: ""
layout: page
permalink: http://ecosmartecloud.com/pool-search/
published: true
post_date: 2013-09-30 20:29:18
---
<center>
<?php
error_reporting(E_ERROR | E_PARSE);
ob_start();
session_start();
	if( (is_user_logged_in()) && (current_user_can('manage_options')) ) {
		echo '
		<h1>Pool Search <br><br></h1><h2>Enter Username or Email of person to search for their pools </h2>
		[php snippet=14]
		';
	}
	elseif ((is_user_logged_in()) && (!current_user_can('manage_options')) ) {
		echo '
		<h1>Only Admins have access to this page. If you are an admin. Please email by using the pool help button.</h1>
		';
	}
	else{
		echo '
		<h1>Only Admins have access to this page. Please log in first if you are an admin.</h1>
		<code>[s8-login-form]</code>
		';
	}
?>
	<br>
	<hr>
	<h3>Please join our <a href="http://www.facebook.com/pages/ECOsmarte/260208241509?fref=ts " target="_blank">Facebook Group </a><br>
	Also, follow us on<a href="https://twitter.com/Ecosmarte2" target="_blank"> Twitter </a></h3>
	</center>