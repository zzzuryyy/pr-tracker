<html>
    <head>
        <title>Login</title>
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

            table {
                width: 400px;
                margin: 100px auto;
                background-color: white;
                border-collapse: collapse;
                border-radius: 8px;
                overflow: hidden;
                box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            }

            th {
                background-color: #f2f2f2;
                padding: 15px;
                color: #333;
                font-size: 18px;
                text-align: center;
                border-top-left-radius: 8px;
                border-top-right-radius: 8px;
            }

            td {
                padding: 12px;
                text-align: left;
                border-bottom: 1px solid #ddd;
            }

            td input[type="text"], td input[type="password"] {
                padding: 8px;
                font-size: 14px;
                width: 100%;
                box-sizing: border-box;
                border-radius: 5px;
                border: 1px solid #ccc;
            }

            td input[type="submit"] {
                padding: 10px 15px;
                background-color: #4CAF50;
                color: white;
                border: none;
                border-radius: 5px;
                font-weight: bold;
                cursor: pointer;
            }

            td input[type="submit"]:hover {
                background-color: #45a049;
            }

            .alert {
                text-align: center;
                color: red;
                font-weight: bold;
            }
        </style>
    </head>
    <body>
        <form action="login.php" method="post">
            <table>
                <tr>
                    <th colspan="2">PR Tracker Login</th>
                </tr>
                <tr>
                    <td>Username:</td>
                    <td><input type="text" name="login_id" required></td>
                </tr>
                <tr>
                    <td>Password:</td>
                    <td><input type="password" name="login_pw" required></td>
                </tr>
                <tr>
                    <td colspan="2" style="text-align: center;">
                        <input type="submit" name="login" value="Login">
                    </td>
                </tr>
            </table>
        </form>

        <?php
            if (isset($_POST['login'])) {
                $login_id = $_POST['login_id'] ?? null;
                $login_pw = $_POST['login_pw'] ?? null;

                if (!$login_id || !$login_pw) {
                    echo "<div class='alert'>Please enter both Login ID and Password.</div>";
                    exit;
                }

                $con = mysqli_connect("localhost", "root", "", "weight_db");

                if (!$con) {
                    die("Connection failed: " . mysqli_connect_error());
                }

                // Secure query using prepared statements to fetch the hashed password
                $stmt = mysqli_prepare($con, "SELECT login_pw, login_rank FROM weight_login WHERE login_id = ?");
                mysqli_stmt_bind_param($stmt, "s", $login_id);
                mysqli_stmt_execute($stmt);
                mysqli_stmt_bind_result($stmt, $hashed_pw, $login_rank);
                mysqli_stmt_fetch($stmt);

                // Debugging: check what is being returned for password hash and login rank
                echo "<div class='alert'>Wrong login information</div>"; // Debugging line

                if ($login_rank && password_verify($login_pw, $hashed_pw)) {
                    // Password is correct, redirect based on login_rank
                    switch (strtolower($login_rank)) {
                        case 'coach':
                            header("Location: view_coach.php");
                            break;
                        case 'player':
                            header("Location: view_plyr.php");
                            break;
                        case 'admin':
                            header("Location: view_admin.php");
                            break;
                        default:
                            echo "<script>alert('Unknown user rank. Please contact support.')</script>";
                            break;
                    }
                    exit;
                } else {
                    echo "<div class='alert'>Invalid username or password.</div>";
                }

                mysqli_stmt_close($stmt);
                mysqli_close($con);
            }
            ?>


        ?>
    </body>
</html>
