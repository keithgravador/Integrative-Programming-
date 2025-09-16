<!DOCTYPE html>
<html>
<head>
    <title>GET Method </title>
</head>
<body>
    <h2>PHP GET Method </h2>
    <form action="process2.php" method="get">
        <label for="name">Enter your name:</label>
        <input type="text" name="name" id="name" required>
        <br><br>
        
        <label for="age">Enter your age:</label>
        <input type="number" name="age" id="age" required>
        <br><br>

        <label for="course">Enter your course:</label>
        <input type="text" name="course" id="name" required>
        <br><br>
        
        <input type="submit" value="Submit">
    </form>
</body>
</html>



<!DOCTYPE html>
<html>
<head>
    <title>Process GET</title>
</head>
<body>
    <?php
        if (isset($_GET['name']) && isset($_GET['age']) && isset($_GET['course'])) {
            $name = htmlspecialchars($_GET['name']);
            $age = htmlspecialchars($_GET['age']);
            $course = htmlspecialchars($_GET['course']); 

            echo "Your name is: " . $name . "<br>";
            echo "Your age is: " . $age . "<br>";
            echo "Your course is: " . $course . "<br>";
        } else {
            echo "No data received.";
        }
    ?>
</body>
</html>
