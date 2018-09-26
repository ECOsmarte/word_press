---
ID: 1894
post_title: chemical pH 2
author: krish
post_excerpt: ""
layout: page
permalink: http://ecosmartecloud.com/chemical-ph-2/
published: true
post_date: 2015-06-25 03:05:56
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
<center><img src="http://ecosmartecloud.com/wp-admin/php/eco_res/round_button_ph.png" alt=""></center><br><br></center>

<p style="font-size: 20px;">
	
	<p style="font-size: 20px;"><u> The following steps detail how to test pH in the pool: </u></p>
	<ul style="font-size: 20px;">
		 <li>Make sure the plastic sample tube is clean and dry. </li><br>
		 <li>Take a sample of water from about 18" below the surface of the water, away from the return jets and skimmers. </li><br>
		 <li>Add 5 drops of phenol red to the water sample. </li><br>
		 <li>Put the cap on the sample tube and turn the tube over to mix. </li><br>
		 <li>Hold the sample out at arm’s length and compare side by side to the pH color samples. </li><br>
		 <li>Record the results. </li>
	</ul>
	
</p>

<br><br><br>
</body>


<center><br><a href="/?page_id=1888" class="button blue">Previous</a>&nbsp;<a href="/?page_id=1897" class="button blue">Next</a>&nbsp;<a href="/?page_id=1886" class="button blue">Index</a>
</center>





</html>