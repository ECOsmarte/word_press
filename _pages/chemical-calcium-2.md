---
ID: 1915
post_title: Chemical calcium 2
author: krish
post_excerpt: ""
layout: page
permalink: >
  http://ecosmartecloud.com/chemical-calcium-2/
published: true
post_date: 2015-06-29 14:02:52
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


<p style="font-size: 20px;"><u>The following detail how to correct for an imbalance of calcium:</u></p>

	<ul style="font-size: 20px;">
		 <li style="list-style-type:square"><b>If calcium is too Low</b>
		 <ul><br>
		 	<li>Put a little calcium at a time in a leaf skimmer. Swish it around toward the middle of the pool until it dissolves. Repeat this process to add 50 - 100 lbs of calcium.</li><br />
		 	<li>Wait a couple days before testing the water again to make sure the calcium is thoroughly mixed into the pool water.</li><br>
		 	<li>Retest the water.</li><br>
		 	<li>Repeat this process until the calcium level is at least above 400ppm.</li>
		 </ul></li>

	</ul>
<br><br><br>

<center><br><a href="/?page_id=1913" class="button blue">Previous</a>&nbsp;<a href="/?page_id=1922" class="button blue">Next</a>&nbsp;<a href="/?page_id=1883" class="button blue">Index</a>
</center>

</body>

</html>