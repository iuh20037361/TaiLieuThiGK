<dependencies>
  	<!-- JSP and Servlets -->
	<!-- https://mvnrepository.com/artifact/jakarta.servlet/jakarta.servlet-api -->
	<dependency>
	    <groupId>jakarta.servlet</groupId>
	    <artifactId>jakarta.servlet-api</artifactId>
	    <version>6.0.0</version>
	    <scope>provided</scope>
	</dependency>
	
	<!-- https://mvnrepository.com/artifact/jakarta.servlet.jsp/jakarta.servlet.jsp-api -->
	<dependency>
	    <groupId>jakarta.servlet.jsp</groupId>
	    <artifactId>jakarta.servlet.jsp-api</artifactId>
	    <version>3.1.1</version>
	    <scope>provided</scope>
	</dependency>
	
	<!-- JSTL -->
	<!-- https://mvnrepository.com/artifact/jakarta.servlet.jsp.jstl/jakarta.servlet.jsp.jstl-api -->
	<dependency>
	    <groupId>jakarta.servlet.jsp.jstl</groupId>
	    <artifactId>jakarta.servlet.jsp.jstl-api</artifactId>
	    <version>3.0.0</version>
	</dependency>
	
	<!-- https://mvnrepository.com/artifact/org.glassfish.web/jakarta.servlet.jsp.jstl -->
	<dependency>
	    <groupId>org.glassfish.web</groupId>
	    <artifactId>jakarta.servlet.jsp.jstl</artifactId>
	    <version>3.0.1</version>
	</dependency>
	
	<!-- MariaDB Client Java -->
	<!-- https://mvnrepository.com/artifact/org.mariadb.jdbc/mariadb-java-client -->
	<dependency>
	    <groupId>org.mariadb.jdbc</groupId>
	    <artifactId>mariadb-java-client</artifactId>
	    <version>3.4.1</version>
	</dependency>
	
  	<dependency>
    <groupId>jakarta.platform</groupId>
    <artifactId>jakarta.jakartaee-api</artifactId>
    <version>10.0.0</version>
    <scope>provided</scope>
  	</dependency>
  </dependencies>




  <Context>
    <Resource name="jdbc/qlthuoc" auth="Container" type="javax.sql.DataSource"
              maxActive="50" maxIdle="30" maxWait="10000"
              username="root" password="sapassword"
              driverClassName="org.mariadb.jdbc.Driver"
              url="jdbc:mariadb://localhost:3307/20037361_LETHIENNGHIA"
              URIEncoding="UTF-8"/>
</Context>


<%@ taglib prefix="c" uri="jakarta.tags.core"%>



<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<%@ taglib prefix="c" uri="jakarta.tags.core"%>
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>LeThienNghia_20037361</title>
</head>
<body>
	<h2>Danh sách thuốc</h2>
    <table border="1">
        <tr>
            <th>Mã Thuốc</th>
            <th>Tên Thuốc</th>
            <th>Giá</th>
            <th>Năm sản xuất</th>
            <th>Mã Loại</th>
        </tr>
        <%-- <c:forEach var="thuoc" items="${thuocs}">
            <tr>
                <td>${thuoc.mathuoc}</td>
                <td>${thuoc.tenthuoc}</td>
                <td>${thuoc.gia}</td>
                <td>${thuoc.namsx}</td>
                <td>${thuoc.maloai}</td>
            </tr>
        </c:forEach> --%>
        <h1>${thuocs}</h1>
    </table>
    
</body>
</html>
