---
ID: 1900
post_title: chemical copper
author: krish
post_excerpt: ""
layout: page
permalink: >
  http://ecosmartecloud.com/chemical-copper/
published: true
post_date: 2015-06-25 10:09:57
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
<body>
	
<h1><center>The 4 Chemical Levels of ECOsmarte and their Constraints</center></h1><br><br>
<center><img src="http://ecosmartecloud.com/wp-admin/php/eco_res/round_button_copper.png" alt=""></center><br><br></center>
<br>
<p style="font-size: 20px;">The second level is copper. Copper is the active ingredient in the pool that acts as both an antimicrobial and algaecide. The correct level for copper is between 0.4-0.7 ppm. If copper is too low, it can cause copper to be rendered ineffective. Copper kills bacteria at 0.1 ppm and algae at 0.3 ppm, if below those levels it will be rendered ineffective accordingly. If copper is too high, it can cause copper staining.</p>

<br><br><br>
</body>
<br>
<center><a href="/?page_id=1897" class="button blue">Previous</a>&nbsp;<a href="/?page_id=1902" class="button blue">Next</a>&nbsp;<a href="/?page_id=1883" class="button blue">Index</a>
</center>





</html>