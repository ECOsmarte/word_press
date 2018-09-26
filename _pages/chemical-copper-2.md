---
ID: 1902
post_title: chemical copper 2
author: krish
post_excerpt: ""
layout: page
permalink: >
  http://ecosmartecloud.com/chemical-copper-2/
published: true
post_date: 2015-06-25 10:16:40
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


	
	<p style="font-size: 20px;"><u>The following steps detail how to test copper in the pool:</u></p>
	<ul style="font-size: 20px;">
		 <li>With a clean, dry sample tube, take a sample of water about 18" below the water - away from return jets and skimmers.</li><br>
		 <li>Add 5 drops of Copper A to the tube, cap it, and turn it upside-down to mix.</li><br>
		 <li>Add 5 drops of Copper B to the same tube, cap it, and turn it upside-down to mix.</li><br>
		 <li>Wait three minutes.</li><br>
		 <li>With the color chart on a flat surface, hold the tube about 1" above the chart. Look down through the length of the tube and compare to the color chart.</li><br>
		 <li>Record Results. The pool must have a copper level between .4 - .7ppm. On a 20,000 gallon pool, it takes, on average, 4 hours to move .1ppm and 12 hours to move .3ppm.</li>
	</ul>
	
	
	
</p>

<br><br><br>

<center><br><a href="/?page_id=1900" class="button blue">Previous</a>&nbsp;<a href="/?page_id=1905" class="button blue">Next</a>&nbsp;<a href="/?page_id=1883" class="button blue">Index</a>
</center>



</body>

</html>