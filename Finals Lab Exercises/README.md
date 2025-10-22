Lab Exercise 1: (Basic JSON Encoding) 

<?php
$student = array(
    "name" => "Keith Gravador",
    "age" => 20,
    "course" => "Bachelor of Science in Information Technology"
);

 
$json_data = json_encode($student);

 
echo $json_data;
?>


Lab Exercise 2: (Decoding JSON)  

<?php
 
$json_string = '{"name":"Keith","age":19,"email":"keith@example.com"}';

$phpObject = json_decode($json_string);
$phpArray = json_decode($json_string, true);

 
echo "Object: " . $phpObject->name . "<br>";
echo "Array: " . $phpArray['email'];
?>


Lab Exercise 3: (JSON Response API Simulation)

<?php
header('Content-Type: application/json');
 
$userProfile = array(
    "id" => 1,
    "name" => "Keith",
    "email" => "keith@example.com",
    "status" => "active"
);

 
echo json_encode($userProfile);
?>

Lab Exercise 4: (Handling JSON Input) 

<?php
$json = '{"username":"admin","password":"1234"}';

$data = json_decode($json, true);

echo "Username: " . $data['username'] . "<br>";
echo "Password: " . $data['password'];
?>


Lab Exercise 5: PHP + JSON + JavaScript (AJAX) 

<?php
header('Content-Type: application/json');

$json = file_get_contents('php://input');
$data = json_decode($json, true);

$username = $data['username'] ?? 'Keith';

$response = array(
    "status" => "Data received successfully!",
    "message" => "Welcome, $username!"
);

echo json_encode($response);
?>
