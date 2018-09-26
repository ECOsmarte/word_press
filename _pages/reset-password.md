---
ID: 692
post_title: Reset Password
author: admin
post_excerpt: ""
layout: page
permalink: >
  http://ecosmartecloud.com/reset-password/
published: true
post_date: 2014-06-05 11:39:08
---
<center>
<div id="content" style="display:inline">
<h2>Enter your new password.<br><br><strong>Make sure it is at least 6 characters long for safety.</strong></h2>
</div>

<div id="password" style="display:inline">
	<form name="pass_change" method="post" enctype="multipart/form-data" action="">
	<table border='1'>
				
		<tr>
		<th><center>New Password</center></th>
		</tr>
		
		<tr>
		<td><input id="new_pass" name="new_pass" type="password"></td>
		</tr>
		
		<tr>
		<th><center>Re-Enter New Password</center></th>
		</tr>
		
		<tr>
		<td><input id="new2_pass" name="new2_pass" type="password"></td>
		</tr>
		
		<tr>
		<td><input type="submit" name="Submit" value="Change Password"></td>
		</tr>
	</table>
	</form>
</div>
</center>

<?php
	error_reporting(E_ERROR | E_PARSE);
	session_start();
	$current_user = wp_get_current_user();
	$user_id = $current_user->ID;
	
	$con = mysqli_connect("eco1312908274943.db.11054119.hostedresource.com", "eco1312908274943", "ECOcloudDB3!", "eco1312908274943");
	// Check connection
	if (mysqli_connect_errno()) {
	  echo "Failed to connect to MySQL: " . mysqli_connect_error();
	}

	if(isset($_POST['Submit'])) {
		$new_pass = $_POST["new_pass"];
		$new2_pass = $_POST["new2_pass"];
		
		if ($new_pass != $new2_pass) {
			echo'<script>alert("The New Passwords Do Not Match. Please retype the new passwords.");</script>';
		}
		
		else {
			$result = mysqli_query($con, "UPDATE wp_users SET user_pass = MD5('$new_pass')  WHERE ID = '$user_id'");
			if ($result) {
				
				echo '<script>document.getElementById("content").innerHTML="<center><h2>Password Has Been Changed</h2></center>";</script>';
				echo '<script>document.getElementById("password").innerHTML="Password Has Been Changed";</script>';
			}
			
			else{
				echo"<script>alert('Password change did not work. Please contact Pool Help or try again.');</script>";
			}
		}
	}
	

?>