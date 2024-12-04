<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login Dashboard</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        .container {
            width: 300px;
            padding: 20px;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            text-align: center;
        }

        h2 {
            margin-bottom: 20px;
        }

        input {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        button {
            width: 100%;
            padding: 10px;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        button:hover {
            background-color: #0056b3;
        }

        .error {
            color: red;
            font-size: 0.9em;
            margin-top: 10px;
        }

        .dashboard-link {
            margin-top: 20px;
        }
    </style>
</head>
<body>

<div class="container" id="login-container">
    <h2>Login to Dashboard</h2>
    <input type="text" id="username" placeholder="Username" required>
    <input type="password" id="password" placeholder="Password" required>
    <button onclick="login()">Login</button>
    <p class="error" id="error-message"></p>
</div>

<div class="container" id="dashboard-container" style="display: none;">
    <h2>Welcome to the Dashboard</h2>
    <p>Click the link below to view the Power BI report:</p>
    <a href="https://app.powerbi.com/groups/me/reports/ed71ebae-5a34-462b-86d7-16469e28d738/2c7c5304e29c672d071b?experience=power-bi" target="_blank" class="dashboard-link">View Power BI Report</a>
</div>

<script>
    function login() {
        const username = document.getElementById('username').value;
        const password = document.getElementById('password').value;
        const errorMessage = document.getElementById('error-message');

        // Dummy credentials
        if (username === 'admin' && password === '1234') {
            document.getElementById('login-container').style.display = 'none';
            document.getElementById('dashboard-container').style.display = 'block';
        } else {
            errorMessage.textContent = 'Invalid username or password. Please try again.';
        }
    }
</script>

</body>
</html>
