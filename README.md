# RSI-Signals<br>
Just play the code<br>
u0sama007@gmail.com

<!DOCTYPE html>
<html>
<body>

<?php
$servername = "92.205.3.240";
$username = "py";
$password = "py123";
$dbname = "PY";

// Create connection
$conn = new mysqli($servername, $username, $password, $dbname);
// Check connection
if ($conn->connect_error) {
    die("Connection failed: " . $conn->connect_error);
}

$sql = "SELECT ID, 'Loop', Trades FROM Traider;";
$result = $conn->query($sql);

if ($result->num_rows > 0) {
    // output data of each row
    while($row = $result->fetch_assoc()) {
        echo "<br> id: ". $row["ID"]. " - Name: ". $row["Loop"]. " " . $row["Trades"] . "<br>";
    }
} else {
    echo "0 results";
}

$conn->close();
?>



</body>
</html>

