---
ID: 2187
post_title: custom password reset
author: krish
post_excerpt: ""
layout: page
permalink: >
  http://ecosmartecloud.com/custom-password-reset/
published: true
post_date: 2015-07-22 18:55:10
---
<?php  
/* 
Template Name: Reset Page
*/

get_header()
?>
<div class="wrapper">
	
	<?php
		global $wpdb;
		
		$error = '';
		$success = '';
		
		// check if we're in reset form
		if( isset( $_POST['action'] ) && 'reset' == $_POST['action'] ) 
		{
			$email = trim($_POST['user_login']);
			
			if( empty( $email ) ) {
				$error = 'Enter a username or e-mail address..';
			} else if( ! is_email( $email )) {
				$error = 'Invalid username or e-mail address.';
			} else if( ! email_exists( $email ) ) {
				$error = 'There is no user registered with that email address.';
			} else {
				
				$random_password = wp_generate_password( 12, false );
				$user = get_user_by( 'email', $email );
				
				$update_user = wp_update_user( array (
						'ID' => $user->ID, 
						'user_pass' => $random_password
					)
				);
				
				// if  update user return true then lets send user an email containing the new password
				if( $update_user ) {
					$to = $email;
					$subject = 'Your new password from ECOsmarteCloud';
					$sender = get_option('name');
					
					$message = 'Your new password is: '.$random_password.'<br><br> You can setup your own password under User Dashboard -> Change User Settings or Company Dashboard -> Reset Password';
					
					$headers[] = 'MIME-Version: 1.0' . "rn";
					$headers[] = 'Content-type: text/html; charset=iso-8859-1' . "rn";
					$headers[] = "X-Mailer: PHP rn";
					$headers[] = 'From: '.$sender.' < '.$email.'>' . "rn";
					
					$mail = wp_mail( $to, $subject, $message, $headers );
					if( $mail )
						$success = 'Check your email address for you new password.';
						
				} else {
					$error = 'Oops something went wrong updaing your account.';
				}
				
			}
			
			if( ! empty( $error ) )
				echo '<div class="message"><p class="error"><strong>ERROR:</strong> '. $error .'</p></div>';
			
			if( ! empty( $success ) )
				echo '<div class="error_login"><p class="success">'. $success .'</p></div>';
		}
	?>

	<!--html code-->
	<form method="post">
		<fieldset>
		    <div id="input_msg" name="input_msg">
			     <p>Please enter your username or email address. You will receive a temporary password via email.</p>
			
			<p><label for="user_login">Username or E-mail:</label>
			</div>
			
				<?php 
					if(isset($_POST['user_login']))
					{
						$user_login = $_POST['user_login'];
						echo "Success";
						
						echo '<script type="text/javascript">'
						   , 'window.location = " http://ecosmartecloud.com/rest-forget-password";'
						   , '</script>'
						;
					}
					else
					{
						$user_login = '';
					}
				?>
				<div id="input_form" name="input_form">
					<input type="text" name="user_login" id="user_login" size="35 value="<?php echo $user_login; ?>" /></p>
					<p>
						<input type="hidden" name="action" value="reset" />
						<input type="submit" value="Get New Password" class="button" id="submit" />
					</p>
				</div>
		</fieldset> 
	</form>
</div>

<?php get_footer() ?>