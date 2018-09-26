---
ID: 1933
post_title: Back wash
author: krish
post_excerpt: ""
layout: page
permalink: http://ecosmartecloud.com/back-wash/
published: true
post_date: 2015-06-29 15:00:25
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
	
<h1><center>When to backwash your filter</center></h1>
<center><h2>Now we will explain what backwashing is, when to do it, and what happens it is done too frequently or not enough.</h2></center><br><br></center>

<br>
<p style="font-size: 20px;">Backwashing is a way to clear any stuck debris off of the filter. It is effective and does not require opening the filter. As debris from the pool flows through the filter, it is caught by the media so it does not flow back into the pool. As more and more debris is caught, it gets continually harder and harder to push water through, increasing the pressure of the filter. As the pressure increases, the filter can collect finer and finer particles. However if the pressure gets too high, circulation in the pool will slow down and eventually stop, and the pump may be overworked and burn out.</p>

<br><br><br>

<center><br><a href="/?page_id=2004" class="button blue">Previous</a>&nbsp;<a href="/?page_id=1936" class="button blue">Next</a>&nbsp;<a href="/?page_id=1883" class="button blue">Index</a>	
	
</center>



</body>

</html>