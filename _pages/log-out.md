---
ID: 460
post_title: Log Out
author: admin
post_excerpt: ""
layout: page
permalink: http://ecosmartecloud.com/log-out/
published: true
post_date: 2014-05-27 11:02:51
---
<script language=javascript>
//When body loads, this function will be called. It logs the user out and redirects them to home page.
function redirect(){
  window.location.href = " <?php echo wp_logout_url( home_url() ); ?>";
}
</script>

<body onload="redirect()">

</body>