# Password-Validation

<html>  
<head>  
<title> Validate the Password </title>  
</head>  
<script>  
function validateForm() {  
    //collect form data in JavaScript variables  
    var pw1 = document.getElementById("pswd1").value;  
    var pw2 = document.getElementById("pswd2").value;  
    var name1 = document.getElementById("fname").value;  
    var name2 = document.getElementById("lname").value;  
      
    //check empty first name field  
    if(name1 == "") {  
      document.getElementById("blankMsg").innerHTML = "**Fill the first name";  
      return false;  
    }  
      
    //character data validation  
    if(!isNaN(name1)){  
      document.getElementById("blankMsg").innerHTML = "**Only characters are allowed";  
      return false;  
    }  
  
   //character data validation  
    if(!isNaN(name2)){  
      document.getElementById("charMsg").innerHTML = "**Only characters are allowed";  
      return false;  
    }   
    
    //check empty password field  
    if(pw1 == "") {  
      document.getElementById("message1").innerHTML = "**Fill the password please!";  
      return false;  
    }  
    
    //check empty confirm password field  
    if(pw2 == "") {  
      document.getElementById("message2").innerHTML = "**Enter the password please!";  
      return false;  
    }   
     
    //minimum password length validation  
    if(pw1.length < 8) {  
      document.getElementById("message1").innerHTML = "**Password length must be atleast 8 characters";  
      return false;  
    }  
  
    //maximum length of password validation  
    if(pw1.length > 15) {  
      document.getElementById("message1").innerHTML = "**Password length must not exceed 15 characters";  
      return false;  
    }  
    
    if(pw1 != pw2) {  
      document.getElementById("message2").innerHTML = "**Passwords are not same";  
      return false;  
    } else {  
      alert ("Your password created successfully");  
      document.write("JavaScript form has been submitted successfully");  
    }  
 }  
</script>  
  
<body>  
<h1 style="color:green">Javatpoint</h1>  
<h3> Verify valid password Example </h3>  
  
<form onsubmit ="return validateForm()">  
  
<!-- Enter first name -->  
<td> Full Name* </td>  
<input type = "text" id = "fname" value = "">   
<span id = "blankMsg" style="color:red"> </span> <br><br>  
  
<!-- Enter last name -->  
<td> Last Name </td>  
<input type = "text" id = "lname" value = "">   
<span id = "charMsg" style="color:red"> </span> <br><br>  
  
<!-- Create a new password -->  
<td> Create Password* </td>  
<input type = "password" id = "pswd1" value = "">   
<span id = "message1" style="color:red"> </span> <br><br>  
  
<!?Enter confirm password -->  
<td> Confirm Password* </td>  
<input type = "password" id = "pswd2" value = "">   
<span id = "message2" style="color:red"> </span> <br><br>  
  
<!-- Click to verify valid password -->  
<input type = "submit" value = "Submit">  
  
<!-- Click to reset fields -->  
<button type = "reset" value = "Reset" >Reset</button>  
</form>  
</body>  
</html>  
