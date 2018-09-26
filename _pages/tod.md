---
ID: 2167
post_title: test other user
author: krish
post_excerpt: ""
layout: page
permalink: http://ecosmartecloud.com/tod/
published: true
post_date: 2015-07-16 11:54:13
---
<head>
	<meta name="viewport" content="width=device-width, initial-scale=1">
		
<link rel="stylesheet" href="http://ecosmartecloud.com/wp-admin/php/eco_res/css/bootstrap.css">
<script src="http://ecosmartecloud.com/wp-admin/php/eco_res/js/bootstrap.min.js"></script>

</head>
<center>

<h1 style="text-align: center;">Welcome to the EcoSmarte Cloud.</h1>
<p style="text-align: center;">Begin tracking pool data by adding a new customer and entering their numbers in 'My Pools'. View previous data in 'View Pool History Data'.</p>

<div class="container">
  <table class="table">
  	
  	<tr>
     <td><a title="Profile Your Pool" href="/?page_id=11">Profile Your Pool</a>
Add your new pool customers here to begin monitoring their swimming pool.
<a title="Profile Your Pool" href="/?page_id=11"><img src="http://ecosmartecloud.com/wp-content/uploads/2014/12/Pool-Profiling.png" alt="Pool-Profiling" width="524" height="303" /></a></td>
     
     <td><a title="Enter Measurement Data" href="/?page_id=416">Add Data </a>
Click here to view your registered pools and add data.
<a title="Enter Measurement Data" href="/?page_id=416"><img src="http://ecosmartecloud.com/wp-content/uploads/2014/12/Add-Data.png" alt="Add-Data" width="524" height="303" /></a>
<h3>Note: Wifi users will have automatic reporting.</h3></td>

   	</tr>        	
  	
  	<tr>
     <td><a title="View Pool History Data" href="/?page_id=508">View Pool History Data</a>
View previous data entries.
<a title="View Pool History Data" href="/?page_id=508"><img src="http://ecosmartecloud.com/wp-content/uploads/2014/12/View-Pool-History-Data.png" alt="View_History" width="524" height="140" /></a></td>

    <td><a title="Change User Settings" href="/?page_id=465">Change User Settings</a>
Update Password and Address.
<a title="Change User Settings" href="/?page_id=465"><img src="http://ecosmartecloud.com/wp-content/uploads/2014/12/Change-User-Settings-1.png" alt="new_user" width="524" height="140" /></a></td>
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
                        <a href="/?page_id=1838">Register As Water Customer</a> 
                   <?php

		}


    
}

?>