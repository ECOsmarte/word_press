---
ID: 1743
post_title: Recolocar la contraseña
author: admin
post_excerpt: ""
layout: page
permalink: >
  http://ecosmartecloud.com/recolocar-la-contrasena/
published: true
post_date: 2015-01-08 15:47:25
---

<div id="content">
<h2>Introduzca su contraseña nueva.

<strong>Asegúrese que es por lo menos 6 símbolos de largo para seguridad.</strong></h2>
</div>
<div id="password"><form action="" enctype="multipart/form-data" method="post" name="pass_change">
<table border="1">
<tbody>
<tr>
<th>Contraseña nueva</th>
</tr>
<tr>
<td></td>
</tr>
<tr>
<th>Confirme su contraseña nueva</th>
</tr>
<tr>
<td></td>
</tr>
<tr>
<td></td>
</tr>
</tbody>
</table>
</form></div>
<!--?php 
	error_reporting(E_ERROR | E_PARSE);
	session_start();
	$current_user = wp_get_current_user();
	$user_id = $current_user-->ID; $con = mysqli_connect("eco1312908274943.db.11054119.hostedresource.com", "eco1312908274943", "ECOcloudDB3!", "eco1312908274943"); // Check connection if (mysqli_connect_errno()) { echo "Failed to connect to MySQL: " . mysqli_connect_error(); } if(isset($_POST['Submit'])) { $new_pass = $_POST["new_pass"]; $new2_pass = $_POST["new2_pass"]; if ($new_pass != $new2_pass) { echo'// '; } else { $result = mysqli_query($con, "UPDATE wp_users SET user_pass = MD5('$new_pass') WHERE ID = '$user_id'"); if ($result) { echo '// &lt;![CDATA[
document.getElementById(&quot;content&quot;).innerHTML=&quot;
<h2>Password Has Been Changed</h2>
";
// ]]&gt;'; echo '// '; } else{ echo"// "; } } } ?&gt;