You will need a internet connection and a browser that supports html5 such as google chrome or microsoft edge.
For this project i used Microsoft expression web 4 as i have some experience and find it the easiest to use out of all of them. To access the webpage you will need a browser such as Chrome or Edge.
The purpose of this project is to get us fammiliar with GitHub so that for future asssignments it has become second nature.
Abstract
For this assignment we had to create a form that we can submit to mysql and fetch data from.
Intro


# Method
## Tools Used
The first tool i used was the create a server function: 
$servername = "localhost";
$username = "valley";
$password = "viking";

$conn = new mysqli($servername, $username, $password);

second i created the mysql database we woukd be reading and writing from:
$sql = "create database names";
if ($conn->querry($sql) === true) {
	echo "database created succesfully";
} else {
	echo "error creating databse" .$conn->error;
}

third i used the write function to display the entries we submitted to the database:
$query = "SELECT * from names";
echo "<b> <center>Database Output</center> </b> <br> <br>";

if ($result = $mysqli->query($query)) {

    while ($row = $result->fetch_assoc()) {
        $field1name = $row["first name"];
        $field2name = $row["last name"];
        $field3name = $row["email"];
        
        echo '<tr>
        			<td>'.$field1name.'</td>
        			<td>'.$field2name.'</td>
        			<td>'.$field3name.'</td>
        	</tr>';
    }
$result->free();
}

lastyl i created the form itself where submissions will be made:
<form action="signup.php" method="post">
first name: <input type="text" name="name"><br>
Last name: <input type="text" name="name"><br>
email: <input type="text" name="email"><br>
<input type="submit"/>

## Programming Language
The Language i used to write this was php.
## System Requirements
A system that supports html5 or above. An internet browser such as chrome or edge. 
## Environmental Requirements 
Access to the internet
## Data Used
## Purpose of the Development
# Results
![C:\xampp\htdocs\MyProj\signupsheet.php]
# Conclusion
This was a fun assignment that helped me to understand more about php and how it works.
# Future Work
For future work i think i will utilise these tools often as they are extremely useful>
# References
!