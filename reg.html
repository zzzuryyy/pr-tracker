<?php
$con = mysqli_connect("localhost", "root", "", "weight_db");

if (!$con) {
    die("Connection failed: " . mysqli_connect_error());
}

$register_success = false;

if (isset($_POST['submit'])) {
    $plyr_name = $_POST['plyr_name'];
    $plyr_pos = $_POST['plyr_pos'];
    $plyr_bnch = floatval($_POST['plyr_bnch']);
    $plyr_dl = floatval($_POST['plyr_dl']);
    $plyr_sqt = floatval($_POST['plyr_sqt']);
    $plyr_total = $plyr_bnch + $plyr_dl + $plyr_sqt;

    $query = "INSERT INTO weight_players (plyr_name, plyr_pos, plyr_bnch, plyr_dl, plyr_sqt, plyr_total) 
              VALUES ('$plyr_name', '$plyr_pos', $plyr_bnch, $plyr_dl, $plyr_sqt, $plyr_total)";

    if (mysqli_query($con, $query)) {
        $register_success = true;
        header("refresh:3.5;url=view_coach.php"); // Wait 3.5 seconds before redirect
    }
}
?>

<!DOCTYPE html>
<html>
<head>
    <title>Register Player</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
    <style>
        body {
            background-image: url('gymvibe.jpg');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            background-repeat: no-repeat;
            margin-top: 50px;
            font-family: Arial, sans-serif;
            color: #333;
        }

        .form-container {
            width: 1000px;
            margin: auto;
            padding: 20px;
            background-color: rgba(240, 240, 240, 0.9);
            border-radius: 10px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.2);
        }

        table {
            width: 100%;
            background-color: #f2f2f2;
            border-collapse: collapse;
        }

        th, td {
            padding: 12px;
            text-align: center;
            border: 1px solid #ccc;
        }

        th {
            background-color: #ddd;
        }

        input[type="text"], input[type="number"], select, input[type="submit"] {
            padding: 6px 10px;
            font-size: 14px;
            margin: 0 3px;
            border-radius: 6px;
            border: 1px solid #aaa;
        }

        .highlight {
            background-color: yellow;
            font-weight: bold;
        }

        .success-message {
            text-align: center;
            color: green;
            font-weight: bold;
        }

        .links {
            text-align: center;
            margin-top: 20px;
        }

        a {
            text-decoration: none;
        }

        .red-button {
            background-color: #d9534f;
            color: white;
            padding: 8px 16px;
            border-radius: 8px;
            text-decoration: none;
            margin: 0 5px;
            display: inline-block;
            transition: background-color 0.3s ease;
            font-weight: bold;
        }

        .red-button i {
            margin-right: 6px;
        }

        .red-button:hover {
            background-color: #c9302c;
        }
    </style>
</head>
<body>

    <div class="form-container">
        <?php if ($register_success): ?>
            <p class="success-message">Player registered successfully! Redirecting...</p>
        <?php endif; ?>

        <form method="post" action="">
            <table>
                <tr>
                    <th colspan="2">Register New Player</th>
                </tr>
                <tr>
                    <td>Name:</td>
                    <td><input type="text" name="plyr_name" required></td>
                </tr>
                <tr>
                    <td>Position:</td>
                    <td>
                        <select name="plyr_pos" required>
                            <option value="QB">QB</option>
                            <option value="RB">RB</option>
                            <option value="WR">WR</option>
                            <option value="OL">OL</option>
                            <option value="DL">DL</option>
                            <option value="LB">LB</option>
                            <option value="DB">DB</option>
                        </select>
                    </td>
                </tr>
                <tr>
                    <td>Bench Press:</td>
                    <td><input type="number" step="0.1" name="plyr_bnch" required></td>
                </tr>
                <tr>
                    <td>Deadlift:</td>
                    <td><input type="number" step="0.1" name="plyr_dl" required></td>
                </tr>
                <tr>
                    <td>Squat:</td>
                    <td><input type="number" step="0.1" name="plyr_sqt" required></td>
                </tr>
                <tr>
                    <td colspan="2" style="text-align: center;">
                        <input type="submit" name="submit" value="Register Player">
                    </td>
                </tr>
            </table>
        </form>
    </div>

    <div class="links">
        <a class="red-button" href="view_coach.php">
            <i class="fas fa-arrow-left"></i> Back to Player Records
        </a>
    </div>

</body>
</html>

<?php mysqli_close($con); ?>
