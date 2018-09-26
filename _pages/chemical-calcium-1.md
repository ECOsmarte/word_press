---
ID: 1913
post_title: Chemical calcium 1
author: krish
post_excerpt: ""
layout: page
permalink: >
  http://ecosmartecloud.com/chemical-calcium-1/
published: true
post_date: 2015-06-29 14:02:29
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
<center><img src="http://ecosmartecloud.com/wp-admin/php/eco_res/round_button_cal.png" alt=""></center><br><br></center>
<br>
<p style="font-size: 20px;">The third level is calcium. Calcium’s main job is to acts as a pH buffer and stabilizes pH in the water. Calcium also adds conductivity to the water so that the electrodes can send electricity through the copper anodes and release copper ions into the water. The correct level for calcium is 400 ppm minimum. If calcium is too low, pH can drift high and copper ions will not be released into the water efficiently.</p>
<br /><br />

<p style="font-size: 20px;"><u>The following steps detail how to test calcium in the pool:</u></p>
	<ul style="font-size: 20px;">
		 <li>Dip one paper calcium test strip into the water for 3 seconds and then remove.</li><br>
		 <li>Immediately match to the closest color on the color chart.</li><br>
		 <li>Read results as ppm and record.</li><br>
	</ul>

<br><br><br>

<center><br><a href="/?page_id=1905" class="button blue">Previous</a>&nbsp;<a href="/?page_id=1915" class="button blue">Next</a>&nbsp;<a href="/?page_id=1883" class="button blue">Index</a>
</center>

</body>

</html>