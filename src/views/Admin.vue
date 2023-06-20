<template>
	<nav class="navbar">
		<ul class="navbar-nav">
			<li class="nav-item"><router-link to="/attendanceSheet" class="nav-link">Attendance Sheet</router-link></li>
			<li class="nav-item"><router-link to="/register" class="nav-link">Register Staff</router-link></li>
			<li class="nav-item"><router-link to="/" class="nav-link">Logout</router-link></li>
		</ul>
	</nav>
</template>
  
  <style>
  .navbar {
    background-color: #4F46E5;
    padding: 20px;
    display: flex;
    justify-content: center;
  }
  
  .navbar-nav {
    list-style: none;
    display: flex;
  }
  
  .nav-item {
    margin-right: 10px;
    background-color: #FAEBD7;
    padding: 10px;
  }
  
  .nav-link {
    text-decoration: none;
    color: #333;
    padding: 5px;
  }
  
  .nav-link:hover {
    color: #666;
  }
  </style>
  