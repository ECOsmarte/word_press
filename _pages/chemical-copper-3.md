---
ID: 1905
post_title: chemical copper 3
author: krish
post_excerpt: ""
layout: page
permalink: >
  http://ecosmartecloud.com/chemical-copper-3/
published: true
post_date: 2015-06-25 15:32:39
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

<p style="font-size: 20px;"><u>The following details how to correct for an imbalance of copper:</u></p>
	<ul style="font-size: 20px;">
		 <li style="list-style-type:square;><p style="font-size: 20px;"><b>If copper is too Low</b></p>
		 <ul style="font-size: 20px;">
		 	<li><p style="font-size: 20px;">Set Controller mode to ION until Copper levels register at least 0.4 ppm.</p></li>
		 </ul></li>
		 
		 <li style="list-style-type:square; font-size: 20px;"><p style="font-size: 20px;"><b>If copper is too High</b></p>
		 <ul style="font-size: 20px;">
		 	
			<li style="list-style-type:circle; font-size: 20px;"><p style="font-size: 20px;">Method 1</p>
            <ul style="font-size: 20px;">
            	<li><p style="font-size: 20px;">Drain 2 feet of water from the pool and refill.</p></li>
            	<li><p style="font-size: 20px;">Retest the copper.</p></li>
            	<li><p style="font-size: 20px;">If the copper level is still above .7ppm, drain another 2 feet and refill.</p></li>
            </ul></li>
		 </ul>

		 <ul style="list-style-type:circle; font-size: 20px;">
			<li><p style="font-size: 20px;">Method 2</p>
            <ul style="font-size: 20px;">
            	<li><p style="font-size: 20px;">Place 4 Ferre Tabs (from a local pool store or online at ecosmarteonlinestore.com) into the skimmers.</p></li>
            </ul></li>
            
		 </ul></li>

	</ul>

<br><br><br>

<center><br><br><a href="/?page_id=1902" class="button blue">Previous</a>&nbsp;<a href="/?page_id=1913" class="button blue">Next</a>&nbsp;<a href="/?page_id=1883" class="button blue">Index</a>
</center>



</body>

</html>