---
ID: 1924
post_title: Chemical phosphates 2
author: krish
post_excerpt: ""
layout: page
permalink: >
  http://ecosmartecloud.com/chemical-phosphates-2/
published: true
post_date: 2015-06-29 14:27:03
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
<center><img src="http://ecosmartecloud.com/wp-admin/php/eco_res/round_button_phos.png" alt=""></center><br><br></center>

<p style="font-size: 20px;"><u> The following steps detail how to test phosphates in the pool:</u></p>
	<ul style="font-size: 20px;">
		 <li>With a clean, dry sample tube, take a 10 mL sample of water from about 18″ below the surface of the water, away from the return jets and skimmers. </li><br>
		 <li>Gently bend a phosphate test strip in half (do not fold), with pads facing inward. Place the strip inside the test tube cap.</li><br>
		 <li>Cap the test tube and invert the tube slowly 5 times, allowing the air bubble to go from the top to bottom and bottom to top.</li><br>
		 <li>Remove the cap and test strip.</li><br>
		 <li>Place the bottom of the test tube on the white boxed area of the color chart on the phosphate test container. Look down through the top of the OPEN test tube and compare it to the color chart.</li><br>
		 <li>Read results as ppb and record. </li>
	</ul>


<br><br><br>

<center><a href="/?page_id=1922" class="button blue">Previous</a>&nbsp;<a href="/?page_id=2004" class="button blue">Next</a>&nbsp;<a href="/?page_id=1883" class="button blue">Index</a>
</center>

</body>

</html>