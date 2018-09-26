---
ID: 2176
post_title: ecosmarte university
author: krish
post_excerpt: ""
layout: page
permalink: >
  http://ecosmartecloud.com/ecosmarte-university/
published: true
post_date: 2015-07-20 13:45:21
---
<html>
	 <link rel="stylesheet" href="http://ecosmartecloud.com/wp-admin/php/eco_res/style.css">

   <?php
  		
  		function browser(){
    $user_agent = $_SERVER['HTTP_USER_AGENT'];
    $browsers = array(
                        'Chrome' => array('Google Chrome','Chrome/(.*)s'),
                        'MSIE' => array('Internet Explorer','MSIEs([0-9.]*)'),
                        'Firefox' => array('Firefox', 'Firefox/([0-9.]*)'),
                        'Safari' => array('Safari', 'Version/([0-9.]*)'),
                        'Opera' => array('Opera', 'Version/([0-9.]*)')
                        ); 
                         
    $browser_details = array();
     
        foreach ($browsers as $browser => $browser_info){
            if (preg_match('@'.$browser.'@i', $user_agent)){
                $browser_details['name'] = $browser_info[0];
                    preg_match('@'.$browser_info[1].'@i', $user_agent, $version);
                $browser_details['version'] = $version[1];
                    break;
            } else {
                $browser_details['name'] = 'Unknown';
                $browser_details['version'] = 'Unknown';
            }
        }
     
    return $browser_details['name'];
}
 
// Example of use
$browser_name = browser();
 
   ?>

<center>
<img src="http://ecosmartecloud.com/wp-admin/php/training/Ecosmarte-Basics.png" height="300" width="1000">
<br>
<h2>Hello, and welcome to ECOsmarte University</h2>
	<h1><span style="font-size:45px; font-weight: bold;">INDEX</span></h1>
	<br>
	
	<center><a href="http://ecosmartecloud.com/wp-admin/php/training/ECOSMARTE UNIVERSITY.pdf" class="button blue">Take the Lesson</a>&nbsp;<a href=" http://ecosmartecloud.com/quiz-2/" class="button blue">Take the Test</a></center>
	
</center>

</html>