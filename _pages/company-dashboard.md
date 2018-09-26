---
ID: 1463
post_title: Company Dashboard
author: admin
post_excerpt: ""
layout: page
permalink: >
  http://ecosmartecloud.com/company-dashboard/
published: true
post_date: 2014-12-19 13:39:18
---
<head>
	<meta name="viewport" content="width=device-width, initial-scale=1">

</head>
<center>

<h2>Start setting up your pools with Pool Profiling.</h2><br><br>

<strong>Note: Each user is allowed to add up to three pools to their profile. Email Pool Help if you need to add more than three pools.</strong></h3><br><br>

<div class="container">
  <table class="table">
  	
  	<tr>
     <td><a href="http://ecosmartecloud.com/pool-profiling/" >Add A New Customer</h1></a>Add your new pool customers here to begin monitoring their swimming pool.<br><a href="/?page_id=412"><img src="http://ecosmartecloud.com/wp-content/uploads/2014/12/Add-A-New-Customer.png" alt="Profiling_pool" width="524" height="140"/></a></td>
     <td><a href="/?page_id=416" >Add Data</h1></a>Enter measurements for profiled pools.<br><a href="/?page_id=416"><img src="http://ecosmartecloud.com/wp-content/uploads/2014/12/Add-Data.png" alt="View_setting" width="524" height="140"/></a>
<h3>Note: Wifi users will have automatic reporting.</h3></td>
   	</tr>        	
  	
  	<tr>
     <td><a href="http://ecosmartecloud.com/view-data/" >View Pool History Data</h1></a>View previous data entries.<br><br><a href="/?page_id=508"><img src="http://ecosmartecloud.com/wp-content/uploads/2014/12/View-Pool-History-Data.png" alt="View_History" width="524" height="140"/></a></td>
    <td><a href="/?page_id=465" >Change User Settings</h1></a>Update Password and Address.<br><br><a href="/?page_id=465"><img src="http://ecosmartecloud.com/wp-content/uploads/2014/12/Change-User-Settings-1.png" alt="new_user" width="524" height="140" /></a></td>
   	</tr> 
  	
  	 </table>
</div>
<?php

$con = mysqli_connect("eco1312908274943.db.11054119.hostedresource.com", "eco1312908274943", "ECOcloudDB3!", "eco1312908274943");
// Check connection
if (mysqli_connect_errno()) {
  echo "Failed to connect to MySQL: " . mysqli_connect_error();
}

$current_user = wp_get_current_user();
$user_email = $current_user->user_email;
$user_id = $current_user->ID;
$user_roles = $current_user->roles;
$user_role = array_shift($user_roles);

//Look if the user is in the water profile

$results = mysqli_query($con,"SELECT ID FROM cstm_water_profile WHERE email='$user_email'");
		
		$id_exist = mysqli_num_rows($results); //total records
		
if($user_role==='pc' || $user_role==='su')
{

                 if($id_exist) 
		{
		    ?>
                        <a href="/?page_id=1829">Visit Water Customer Dashboard</a> 
                   <?php
		}
		else
		{
                    ?>
                        <a href="/?page_id=1838">Add non-salt, non chemical whole house water system service log</a> 
                   <?php

		}


    
}

?>