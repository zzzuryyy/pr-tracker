<?php
$con = mysqli_connect("localhost", "root", "", "weight_db");
$update_success = false;

if (isset($_GET['edit'])) {
    $plyr_name = $_GET['edit'];
    $query = "SELECT * FROM weight_players WHERE plyr_name='$plyr_name'";
    $result = mysqli_query($con, $query);
    $row = mysqli_fetch_array($result);
    
    $plyr_pos = $row['plyr_pos'];
    $plyr_bnch = $row['plyr_bnch'];
    $plyr_dl = $row['plyr_dl'];
    $plyr_sqt = $row['plyr_sqt'];
}

if (isset($_POST['update'])) {
    $plyr_name = $_POST['plyr_name']; // primary key
    $plyr_pos = $_POST['plyr_pos'];
    $plyr_bnch = floatval($_POST['plyr_bnch']);
    $plyr_dl = floatval($_POST['plyr_dl']);
    $plyr_sqt = floatval($_POST['plyr_sqt']);
    $plyr_total = $plyr_bnch + $plyr_dl + $plyr_sqt;

    $update_query = "UPDATE weight_players 
                     SET plyr_pos='$plyr_pos', plyr_bnch=$plyr_bnch, plyr_dl=$plyr_dl, plyr_sqt=$plyr_sqt, plyr_total=$plyr_total 
                     WHERE plyr_name='$plyr_name'";

    if (mysqli_query($con, $update_query)) {
        $update_success = true;
        header("refresh:3.5;url=view_coach.php"); // Wait 2 seconds before redirect
    }
}
?>

<html>
<head>
    <title>Edit Player Info</title>
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

        table {
            width: 600px;
            margin: 50px auto;
            background-color: white;
            border-collapse: collapse;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        th, td {
            padding: 12px;
            text-align: center;
            border-bottom: 1px solid #ddd;
        }

        th {
            background-color: #f2f2f2;
            color: #333;
        }

        tr:nth-child(even) {
            background-color: #f9f9f9;
        }

        tr:hover {
            background-color: #f1f1f1;
        }

        input[type="text"], input[type="number"], select {
            padding: 5px;
            font-size: 14px;
            margin: 5px 0;
            width: 100%;
            box-sizing: border-box;
            border-radius: 5px;
            border: 1px solid #ccc;
        }

        input[type="submit"] {
            padding: 10px 15px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            font-weight: bold;
            cursor: pointer;
        }

        input[type="submit"]:hover {
            background-color: #45a049;
        }

        .control-bar {
            background-color: rgba(0, 0, 0, 0.85);
            padding: 8px 12px;
            margin: 0 auto 20px auto;
            width: 600px;
            border-radius: 8px;
            color: white;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }

        .logout-button {
            text-align: center;
            margin-top: 30px;
        }

        .logout-button a {
            color: white;
            background-color: #ff4d4d;
            padding: 10px 15px;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
        }
    </style>
</head>
<body>

    <?php if ($update_success): ?>
        <p align='center' style='color:white; font-weight: bold;'>Player updated successfully! Redirecting...</p>
    <?php endif; ?>

    <form method="post" action="" style="width: 600px; margin: auto; background-color: white; padding: 20px; border-radius: 8px; box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);">
        <input type="hidden" name="plyr_name" value="<?php echo $plyr_name; ?>" />

        <table>
            <tr>
                <th colspan='2'>Edit Player Information: <?php echo $plyr_name; ?></th>
            </tr>

            <tr>
                <td>Position:</td>
                <td>
                    <select name="plyr_pos" required>
                        <option value="QB" <?php if ($plyr_pos == "QB") echo "selected"; ?>>QB</option>
                        <option value="RB" <?php if ($plyr_pos == "RB") echo "selected"; ?>>RB</option>
                        <option value="WR" <?php if ($plyr_pos == "WR") echo "selected"; ?>>WR</option>
                        <option value="OL" <?php if ($plyr_pos == "OL") echo "selected"; ?>>OL</option>
                        <option value="DL" <?php if ($plyr_pos == "DL") echo "selected"; ?>>DL</option>
                        <option value="LB" <?php if ($plyr_pos == "LB") echo "selected"; ?>>LB</option>
                        <option value="DB" <?php if ($plyr_pos == "DB") echo "selected"; ?>>DB</option>
                    </select>
                </td>
            </tr>

            <tr>
                <td>Bench Press:</td>
                <td><input type="number" step="0.1" name="plyr_bnch" value="<?php echo $plyr_bnch; ?>" required></td>
            </tr>

            <tr>
                <td>Deadlift:</td>
                <td><input type="number" step="0.1" name="plyr_dl" value="<?php echo $plyr_dl; ?>" required></td>
            </tr>

            <tr>
                <td>Squat:</td>
                <td><input type="number" step="0.1" name="plyr_sqt" value="<?php echo $plyr_sqt; ?>" required></td>
            </tr>

            <tr align='center'>
                <td colspan='2'><input type="submit" name="update" value="Update Player"></td>
            </tr>

            <tr align='center'>
                <td colspan='2'><a href="view_coach.php" style="color: #4CAF50; font-weight: bold; text-decoration: none; background-color: white; padding: 10px 15px; border-radius: 5px;">Back to Player Records</a></td>
            </tr>
        </table>
    </form>

</body>
</html>
