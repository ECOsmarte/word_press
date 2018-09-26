---
ID: 1940
post_title: Setting Controller
author: krish
post_excerpt: ""
layout: page
permalink: >
  http://ecosmartecloud.com/setting-controller/
published: true
post_date: 2015-06-29 17:33:56
---
<html>

    <link rel="stylesheet" href="buttons.css">
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
<body link="blue">
	
<h1><center>What setting to set your controller to and when</center></h1>
<center><h2>Next we will discuss the controller settings. This lesson will only cover the turbo system, if you want to learn more about the programmable system, please see the ECOsmarte University.</h2></center><br><br></center><br><br>


<p style="font-size: 20px; position: relative; top: 50px;">The turbo has two switches, an ion/oxy switch and a high/low switch. The ion/oxy switch determine whether the system is releasing copper or oxygen into the water respectively. Copper should only ever be released into the pool by setting the switch to ionize if after a copper test you determine that the copper is lower than 0.4 ppm. Otherwise, the switch should be set to oxidize by default. The high/low switch should always be set to high unless the pool is located in a desert in which case the switch may be set to low.</p>

<br><br><br>

<div style="position: relative; top: 70px;"><center><br><a href="/?page_id=1936" class="button blue">Previous</a>&nbsp;<a href="/?page_id=1948" class="button blue">Next</a>&nbsp;<a href="/?page_id=1883" class="button blue">Index</a>	
	
</center>
</div>


</body>

</html>