---
ID: 1669
post_title: Cerrar sesión
author: admin
post_excerpt: ""
layout: page
permalink: http://ecosmartecloud.com/cerrar-sesion/
published: true
post_date: 2015-01-08 11:47:49
---
<script language=javascript>
//When body loads, this function will be called. It logs the user out and redirects them to home page.
function redirect(){
  window.location.href = " <?php echo wp_logout_url( home_url() ); ?>";
}
</script>

<body onload="redirect()">

</body>