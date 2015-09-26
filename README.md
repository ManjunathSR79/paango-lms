# paango-lms
<%@ page language="java" contentType="text/html; charset=ISO-8859-1"
    pageEncoding="ISO-8859-1"%>
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=ISO-8859-1">
<title>Insert title here</title>
 
</head>
<body >

<form method="post" action="addcourse.jsp">
<input 	type="submit" value="Add Course">
</form>
 


 <script type="text/javascript" src="http://localhost:8080/lms/Courses"> 
 function getCourses()
 {
	 var xhr= new XMLHttpRequest();
	 xhr.onreadystatechange=function (){
	 if(xhr.readyState==4)
		 {
		 var res=xhr.responseText;
		 var place=res.split(', ');
		 document.getElementById("cname").value=place[0];}
	 }
	 var req= new HttpServletRequest();
	 var res= new HttpServletResponse();
	 
	 xhr.open("GET",doGet(req ,res),true);
		 xhr.send(null);
		 
	 
	 

 }
 
