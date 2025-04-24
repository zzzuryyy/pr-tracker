<?php
$con = mysqli_connect("localhost", "root", "", "weight_db");

if (!$con) {
    die("Connection failed: " . mysqli_connect_error());
}

$login_id = $_GET['login_id'] ?? '';

if ($_SERVER['REQUEST_METHOD'] === 'POST') {
    $new_id = $_POST['login_id'];
    $new_pw = $_POST['login_pw'];
    $new_rank = $_POST['login_rank'];

    // If a new password is provided, hash it
    if (!empty($new_pw)) {
        $hashed_pw = password_hash($new_pw, PASSWORD_DEFAULT);
        $stmt = $con->prepare("UPDATE weight_login SET login_id = ?, login_pw = ?, login_rank = ? WHERE login_id = ?");
        $stmt->bind_param("ssss", $new_id, $hashed_pw, $new_rank, $login_id);
    } else {
        $stmt = $con->prepare("UPDATE weight_login SET login_id = ?, login_rank = ? WHERE login_id = ?");
        $stmt->bind_param("sss", $new_id, $new_rank, $login_id);
    }
    $stmt->execute();
    $stmt->close();
    
    header("Location: view_admin.php");
    exit;
}

$user = mysqli_fetch_assoc(mysqli_query($con, "SELECT * FROM weight_login WHERE login_id = '$login_id'"));
?>

<html>
<head>
    <title>Edit User</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
    <style>
        body {
            margin: 0;
            padding: 0;
            background-image: url('gymvibe.jpg');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            background-repeat: no-repeat;
            font-family: Arial, sans-serif;
        }

        .container {
            margin: 80px auto;
            width: 500px;
        }

        table {
            width: 100%;
            background-color: white;
            border-collapse: collapse;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
        }

        th, td {
            padding: 12px;
            text-align: center;
        }

        th {
            background-color: #f2f2f2;
            color: #333;
        }

        input, select {
            padding: 8px;
            width: 90%;
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        .btn {
            background-color: #e74c3c;
            color: white;
            padding: 10px 15px;
            text-decoration: none;
            border-radius: 5px;
            border: none;
            font-weight: bold;
            cursor: pointer;
        }

        .btn:hover {
            background-color: #c0392b;
        }

        .btn-back {
            display: inline-block;
            margin-top: 15px;
        }

        h2 {
            text-align: center;
            color: white;
            text-shadow: 2px 2px 4px #000;
            margin-bottom: 20px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Edit User - <?php echo htmlspecialchars($user['login_id']); ?></h2>
        <form method="post">
            <table>
                <tr>
                    <th colspan="2">Edit Login Information</th>
                </tr>
                <tr>
                    <td>Login ID</td>
                    <td><input type="text" name="login_id" value="<?php echo htmlspecialchars($user['login_id']); ?>" required></td>
                </tr>
                <tr>
                    <td>Password:</td>
                    <td>
                        <input 
                            type="password" 
                            name="login_pw" 
                            placeholder="Enter new password"
                            oncopy="return false;" 
                            oncut="return false;" 
                            onfocus="this.value='';" 
                        >
                    </td>
                </tr>

                <tr>
                    <td>Rank</td>
                    <td>
                        <select name="login_rank" required>
                            <option value="player" <?php if ($user['login_rank'] == 'player') echo 'selected'; ?>>Player</option>
                            <option value="coach" <?php if ($user['login_rank'] == 'coach') echo 'selected'; ?>>Coach</option>
                            <option value="admin" <?php if ($user['login_rank'] == 'admin') echo 'selected'; ?>>Admin</option>
                        </select>
                    </td>
                </tr>
                <tr>
                    <td colspan="2"><input type="submit" class="btn" value="Save Changes"></td>
                </tr>
            </table>
        </form>

        <div style="text-align: center;">
            <a href="view_admin.php" class="btn btn-back"><i class="fas fa-arrow-left"></i> Back to Admin Panel</a>
        </div>
    </div>
</body>
</html>
<?php mysqli_close($con); ?>
