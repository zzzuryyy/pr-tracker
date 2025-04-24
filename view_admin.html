<?php
$con = mysqli_connect("localhost", "root", "", "weight_db");

if (!$con) {
    die("Connection failed: " . mysqli_connect_error());
}

$result = mysqli_query($con, "SELECT login_id, login_rank FROM weight_login");

// Delete user if requested
if (isset($_GET['delete'])) {
    $del_id = $_GET['delete'];
    $del_query = "DELETE FROM weight_login WHERE login_id = '$del_id'";
    mysqli_query($con, $del_query);
    header("Location: view_admin.php");
    exit;
}
?>

<html>
<head>
    <title>Admin View</title>
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
            width: 700px;
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
            border-bottom: 1px solid #ddd;
        }

        th {
            background-color: #f2f2f2;
            color: #333;
        }

        .btn-container {
            margin-top: 20px;
            text-align: center;
        }

        .btn {
            display: inline-block;
            margin: 0 10px;
            padding: 10px 15px;
            background-color: #e74c3c;
            color: white;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            transition: background-color 0.3s ease;
        }

        .btn:hover {
            background-color: #c0392b;
        }

        .icon-link {
            text-decoration: none;
            color: black;  /* Changed color to black */
            font-size: 18px;
            margin: 0 6px;
        }

        .icon-link:hover {
            color: #c0392b;
            transform: scale(1.1);
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

        h2 {
            text-align: center;
            color: white;
            text-shadow: 2px 2px 4px #000;
            margin-bottom: 20px;
        }
    </style>

    <script>
        function confirmDelete(userId) {
            if (confirm("Are you sure you want to delete user: " + userId + "?")) {
                window.location.href = "view_admin.php?delete=" + userId;
            }
        }
    </script>
</head>
<body>

    <div class="container">
        <h2>Admin Panel - User List</h2>
        <table>
            <tr>
                <th>Login ID</th>
                <th>Rank</th>
                <th><i class="fas fa-wrench"></i></th>
            </tr>
            <?php while ($row = mysqli_fetch_assoc($result)) : ?>
                <tr>
                    <td><?php echo htmlspecialchars($row['login_id']); ?></td>
                    <td><?php echo htmlspecialchars($row['login_rank']); ?></td>
                    <td>
                        <a href="edit_user.php?login_id=<?php echo $row['login_id']; ?>" class="icon-link" title="Edit"><i class="fas fa-edit"></i></a>
                        <a href="javascript:void(0);" onclick="confirmDelete('<?php echo $row['login_id']; ?>')" class="icon-link" title="Delete"><i class="fas fa-trash-alt"></i></a>
                    </td>
                    
                </tr>
            <?php endwhile; ?>
        </table>

        <div class="btn-container">
            <a href="reg_new.php" class="btn"><i class="fas fa-user-plus"></i> New User</a>
            <a class="btn" href="logout.php"><i class="fas fa-sign-out-alt"></i> Logout </a>
        </div>
    </div>

</body>
</html>

<?php
mysqli_close($con);
?>
