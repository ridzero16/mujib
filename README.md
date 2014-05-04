mujib
=====

ridwan
<?php
include "koneksii.php"
?>
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link href="bootstrap311/dist/css/bootstrap.min.css" rel="stylesheet">
    <link href="bootstrap311/dist/css/offcanvas.css" rel="stylesheet">
    <link rel="stylesheet" type="text/css" href="bootstrap311/docs/examples/blog/blog.css"> 
    <script src="bootstrap311/dist/jquery-1.11.0.min.js"></script>
    <script src="bootstrap311/dist/js/bootstrap.min.js"></script>
    <script src="bootstrap311/dist/js/offcanvas.js"></script>
	<title>Selamat Datang Di Situs Lowongan Kerja Paling Update Tahun 2014</title>
</head>
<body>
	  <div class="navbar navbar-default navbar-fixed-top" role="navigation">
      <div class="container">
        <div class="navbar-header">
          <button type="button" class="navbar-toggle" data-toggle="collapse" data-target=".navbar-collapse">
            <span class="sr-only">Toggle navigation</span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
          </button>
          <a class="navbar-brand">Situs Informasi Loker Paling Update 2014</a>
        </div>
        <div class="collapse navbar-collapse">
          <ul class="nav navbar-nav">
            <li class="active"><a href="index.php">Beranda</a></li>
            <li><a href="blog.php">Blog</a></li>
            <li><a href="bukutamu.php">Bukutamu</a></li>
            <li class="dropdown">
              	<a href="#" class="dropdown-toggle" data-toggle="dropdown">Lainnya<b class="caret"></b></a>
  	            <ul class="dropdown-menu">
	                <li><a href="login2.php">Masuk</a></li>
	                <li><a href="daftar.php">Daftar</a></li>
	                <li><a href="tentang.php">Tentang Kami</a></li>
                </ul>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div class="container">
    	<div class="blog-header">
	    	<div class="jumbotron">
  			  <h1>Hello, world!</h1>
  			  <p>Selamat Datang di Website Info mujib</p>
  			  <p><a href="tentang.php" class="btn btn-primary btn-lg" role="button">Learn more</a></p>
			  </div>
		  </div>
  		<div class="col-sm-8">
        <?php
        $queryartikel = mysql_query("select id_artikel,judul_artikel,tgl_artikel, isi_artikel, nama_pengguna from artikel inner join pengguna where artikel.username=pengguna.username order by id_artikel desc limit 5");
        while ($row=mysql_fetch_array($queryartikel)) {
          echo "
          <div class=blog-post'>
          <div class='blog-post-title'>
            <h4 class='blog-post-title'><a href='post.php?id_artikel=$row[id_artikel]'> $row[judul_artikel]</a></h4>
            </div>
            <p class='blog-post-meta'>$row[tgl_artikel] by $row[nama_pengguna]</p>
            <p>$row[isi_artikel]</p>
          </div>
        ";
        }
        ?>
  		</div>
  		<div class="col-md-4">
  	   	<div class="sidebar-module sidebar-module-inset">
          <h4>Tentang Saya</h4>
             <p>Saya adalah mahasiswa universitas muhammadiyah jember dengan mengambil jurusan Teknik Informatika dan merupakan pembuat dari website ini</p>
  	    </div>
    	</div>
    </div>
    <div class="blog-footer">
      <p>Blog template built for <a href="http://getbootstrap.com">Bootstrap</a> edited by <a href="https://twitter.com/mdo">@mujibridwan</a>.</p>
      <p>
        <a href="#">Back to top</a>
      </p>
    </div>
</body>
