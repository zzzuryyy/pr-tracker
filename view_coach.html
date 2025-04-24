<?php
$con = mysqli_connect("localhost", "root", "", "weight_db");

if (!$con) {
    die("Connection failed: " . mysqli_connect_error());
}

$sort_column = isset($_GET['sort']) ? $_GET['sort'] : 'plyr_name';
$sort_order = isset($_GET['order']) ? $_GET['order'] : 'ASC';

$search_query = "";
if (isset($_GET['search']) && !empty($_GET['search'])) {
    $search = mysqli_real_escape_string($con, $_GET['search']);
    $search_query = " WHERE plyr_name LIKE '%$search%'";
}

$query = "SELECT * FROM weight_players" . $search_query . " ORDER BY $sort_column $sort_order";
$result = mysqli_query($con, $query);

if (!$result) {
    die("Query failed: " . mysqli_error($con));
}
?>

<!DOCTYPE html>
<html>
<head>
    <title>Player Weight Records</title>
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

        table {
            width: 1000px;
            margin: auto;
            background-color: #f2f2f2;
            border-collapse: collapse;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.2);
            border-radius: 10px;
            overflow: hidden;
        }

        th, td {
            padding: 12px;
            text-align: center;
            border: 1px solid #ccc;
        }

        th {
            background-color: #ddd;
        }

        .controls {
            width: 1000px;
            margin: 0 auto 20px auto;
            padding: 10px;
            background-color: rgba(240, 240, 240, 0.9);
            border-radius: 10px;
            text-align: center;
        }

        .links {
            text-align: center;
            margin-top: 20px;
        }

        a {
            text-decoration: none;
        }

        .icon {
            font-size: 16px;
            margin: 0 5px;
            color: #333;
        }

        .icon:hover {
            color: #d9534f;
        }

        select, input[type="submit"], input[type="text"] {
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

        #playerTable tbody tr {
            display: table-row;
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

    <div class="controls">
        <form method="get" action="">
            <label for="search">Search:</label>
            <input type="text" name="search" id="liveSearch" placeholder="Type to search...">

            <label for="sort">Sort by:</label>
            <select name="sort" id="sort">
                <option value="plyr_name" <?= $sort_column == 'plyr_name' ? 'selected' : '' ?>>Name</option>
                <option value="plyr_bnch" <?= $sort_column == 'plyr_bnch' ? 'selected' : '' ?>>Bench Press</option>
                <option value="plyr_dl" <?= $sort_column == 'plyr_dl' ? 'selected' : '' ?>>Deadlift</option>
                <option value="plyr_sqt" <?= $sort_column == 'plyr_sqt' ? 'selected' : '' ?>>Squat</option>
                <option value="plyr_total" <?= $sort_column == 'plyr_total' ? 'selected' : '' ?>>Total</option>
            </select>

            <select name="order" id="order">
                <option value="ASC" <?= $sort_order == 'ASC' ? 'selected' : '' ?>>A-Z / Lowest First</option>
                <option value="DESC" <?= $sort_order == 'DESC' ? 'selected' : '' ?>>Z-A / Highest First</option>
            </select>

            <input type="submit" value="Apply">
        </form>
    </div>

    <table id="playerTable">
        <thead>
            <tr>
                <th colspan='8'>Players' Weight Records</th>
            </tr>
            <tr>
                <th>Name</th>
                <th>Position</th>
                <th>Bench Press [lbs]</th>
                <th>Deadlift [lbs]</th>
                <th>Squat [lbs]</th>
                <th>Total [lbs]</th>
                <th><i class="fas fa-wrench"></i></th>
            </tr>
        </thead>
        <tbody>
            <?php while ($row = mysqli_fetch_assoc($result)): ?>
                <tr>
                    <td><?= htmlspecialchars($row['plyr_name']) ?></td>
                    <td><?= htmlspecialchars($row['plyr_pos']) ?></td>
                    <td><?= $row['plyr_bnch'] ?></td>
                    <td><?= $row['plyr_dl'] ?></td>
                    <td><?= $row['plyr_sqt'] ?></td>
                    <td><?= $row['plyr_total'] ?></td>
                    <td>
                        <a class="icon" href="edit.php?edit=<?= urlencode($row['plyr_name']) ?>" title="Edit">
                            <i class="fas fa-edit"></i>
                        </a>
                        <a class="icon" href="delete.php?del=<?= urlencode($row['plyr_name']) ?>" title="Delete">
                            <i class="fas fa-trash-alt"></i>
                        </a>
                    </td>
                </tr>
            <?php endwhile; ?>
        </tbody>
    </table>

    <div class="links">
        <br>
        <a class="red-button" href="reg.php">
            <i class="fas fa-user-plus"></i> New Registration
        </a>
        <a class="red-button" href="logout.php">
            <i class="fas fa-sign-out-alt"></i> Logout
        </a>
    </div>

    <script>
    const input = document.getElementById('liveSearch');
    input.addEventListener('keyup', function () {
        const filter = input.value.toLowerCase();
        const rows = document.querySelectorAll('#playerTable tbody tr');

        rows.forEach(row => {
            let match = false;

            // Loop through all cells except the last (actions column)
            row.querySelectorAll('td').forEach((cell, index) => {
                // Skip the last cell (action buttons)
                if (index === 6) return;

                const originalText = cell.textContent;
                cell.innerHTML = originalText;

                if (originalText.toLowerCase().includes(filter)) {
                    match = true;
                }
            });

            if (match) {
                row.style.display = '';
                row.querySelectorAll('td').forEach((cell, index) => {
                    // Highlight matching text in cells except the actions column
                    if (index < 6) {
                        const text = cell.textContent;
                        const regex = new RegExp(`(${filter})`, 'gi');
                        cell.innerHTML = text.replace(regex, '<span class="highlight">$1</span>');
                    }
                });
            } else {
                row.style.display = 'none';
            }
        });
    });
</script>



</body>
</html>

<?php mysqli_close($con); ?>
