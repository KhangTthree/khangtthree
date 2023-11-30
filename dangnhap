<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hệ thống Đăng nhập và Bài viết</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
        }

        #loginForm, #registerForm, #loginSuccess, #mainScreen {
            text-align: center;
        }

        #registerForm, #mainScreen {
            display: none;
        }
    </style>
</head>
<body>
    <div id="loginForm">
        <h2>Đăng nhập</h2>
        <form id="login">
            <label for="loginUsername">Tên đăng nhập:</label>
            <input type="text" id="loginUsername" name="username" required><br>

            <label for="loginPassword">Mật khẩu:</label>
            <input type="password" id="loginPassword" name="password" required><br>

            <button type="button" onclick="login()">Đăng nhập</button>
            <p>Chưa có tài khoản? <a href="#" onclick="showRegisterForm()">Đăng ký ngay</a></p>
        </form>
        <div id="loginResult"></div>
    </div>

    <div id="registerForm">
        <h2>Đăng ký</h2>
        <form id="register">
            <label for="registerUsername">Tên đăng nhập:</label>
            <input type="text" id="registerUsername" name="username" required><br>

            <label for="registerPassword">Mật khẩu:</label>
            <input type="password" id="registerPassword" name="password" required><br>

            <button type="button" onclick="register()">Đăng ký</button>
        </form>
        <div id="registerResult"></div>
        <p>Đã có tài khoản? <a href="#" onclick="showLoginForm()">Đăng nhập tại đây</a></p>
    </div>

    <div id="loginSuccess" style="display: none;">
        <p>Đăng nhập thành công!</p>
        <button type="button" onclick="showMainScreen()">Chuyển đến Màn hình chính</button>
    </div>

    <div id="mainScreen">
        <h2>Màn hình chính</h2>
        <p>Đọc bài viết của người khác</p>
        <p>Tạo bài viết của bạn</p>
    </div>

    <script>
        function showRegisterForm() {
            document.getElementById('loginForm').style.display = 'none';
            document.getElementById('registerForm').style.display = 'block';
        }

        function showLoginForm() {
            document.getElementById('registerForm').style.display = 'none';
            document.getElementById('loginForm').style.display = 'block';
            document.getElementById('loginSuccess').style.display = 'none';
        }

        function login() {
            var username = document.getElementById('loginUsername').value;
            var password = document.getElementById('loginPassword').value;

            // Điều kiện kiểm tra đăng nhập
            if (username === 'admin' && password === 'password') {
                document.getElementById('loginResult').innerHTML = 'Đăng nhập thành công!';
                document.getElementById('loginForm').style.display = 'none';
                document.getElementById('loginSuccess').style.display = 'block';
            } else {
                document.getElementById('loginResult').innerHTML = 'Đăng nhập thất bại. Vui lòng kiểm tra tên đăng nhập và mật khẩu.';
            }
        }

        function register() {
            var username = document.getElementById('registerUsername').value;
            var password = document.getElementById('registerPassword').value;

            // Xử lý đăng ký (ở đây có thể thêm vào cơ sở dữ liệu)
            document.getElementById('registerResult').innerHTML = 'Đăng ký thành công!';
            document.getElementById('registerForm').style.display = 'none';
            document.getElementById('loginSuccess').style.display = 'block';
        }

        function showMainScreen() {
            document.getElementById('loginSuccess').style.display = 'none';
            document.getElementById('mainScreen').style.display = 'block';
        }
    </script>
</body>
</html>
