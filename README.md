<!DOCTYPE html>
<html lang="fa">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Math with Afzali</title>
<style>
body {
font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
margin: 0;
padding: 0;
background-color: #f4f4f4;
color: #333;
line-height: 1.6;
height: 100%; /* For scrollability */
overflow-y: auto; /* Enable vertical scrolling */
}
.container {
width: 90%;
max-width: 800px;
margin: 20px auto;
background: #fff;
padding: 20px;
border-radius: 8px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
header {
background: #4CAF50;
color: white;
padding: 1em 0;
text-align: center;
border-radius: 8px 8px 0 0;
}
nav {
background: #333;
color: white;
padding: 0.5em 0;
text-align: center;
border-radius: 0 0 8px 8px;
}
nav a {
color: white;
padding: 10px 15px;
text-decoration: none;
display: inline-block;
transition: background-color 0.3s ease;
}
nav a:hover {
background-color: #575757;
}
section {
display: none; /* Hide all sections by default */
padding: 20px 0;
border-top: 1px solid #eee;
}
section:first-of-type {
border-top: none;
}
h2 {
color: #4CAF50;
text-align: center;
margin-bottom: 20px;
}
.form-group {
margin-bottom: 15px;
}
.form-group label {
display: block;
margin-bottom: 5px;
font-weight: bold;
}
.form-group input[type="text"],
.form-group input[type="password"],
.form-group input[type="email"],
.form-group textarea {
width: calc(100% - 22px);
padding: 10px;
border: 1px solid #ddd;
border-radius: 4px;
}
.form-group button {
background-color: #4CAF50;
color: white;
padding: 10px 20px;
border: none;
border-radius: 4px;
cursor: pointer;
font-size: 16px;
transition: background-color 0.3s ease;
}
.form-group button:hover {
background-color: #45a049;
}
.message {
margin-top: 10px;
padding: 10px;
border-radius: 4px;
background-color: #e0ffe0;
color: #4CAF50;
text-align: center;
}
.video-wrapper {
position: relative;
padding-bottom: 56.25%; /* 16:9 Aspect Ratio */
height: 0;
overflow: hidden;
margin-bottom: 20px;
background-color: #000;
}
.video-wrapper iframe {
position: absolute;
top: 0;
left: 0;
width: 100%;
height: 100%;
border: 0;
}
.survey-item {
margin-bottom: 10px;
padding: 10px;
border: 1px solid #eee;
border-radius: 4px;
background-color: #f9f9f9;
}
footer {
text-align: center;
padding: 20px;
background: #333;
color: white;
margin-top: 20px;
border-radius: 0 0 8px 8px;
}
footer a {
color: #4CAF50;
text-decoration: none;
}
.geogebra-embed {
width: 100%;
height: 500px;
border: 1px solid #ddd;
border-radius: 8px;
}

/* Equation Game Specific Styles */
.equation-game-container {
text-align: center;
padding: 20px;
}
.equation-game-container button {
margin: 10px;
padding: 12px 25px;
font-size: 18px;
cursor: pointer;
border: 1px solid #4CAF50;
border-radius: 5px;
background-color: #e0ffe0;
color: #333;
transition: background-color 0.3s ease;
}
.equation-game-container button:hover:not(:disabled) {
background-color: #c8e6c9;
}
.equation-game-container button:disabled {
opacity: 0.6;
cursor: not-allowed;
}
#equation-display {
font-size: 24px;
margin-bottom: 20px;
font-weight: bold;
}
#game-feedback {
margin-top: 15px;
font-size: 18px;
font-weight: bold;
}
#game-result {
font-size: 20px;
margin-top: 20px;
font-weight: bold;
color: #4CAF50;
}
</style>
</head>
<body>
<div class="container">
<header>
<h1>Math with Afzali</h1>
</header>
<nav>
<a href="#" onclick="showSection('home-section')">صفحه اصلی</a>
<a href="#" onclick="showSection('register-section')">ثبت نام</a>
<a href="#" onclick="showSection('login-section')">ورود به پنل کاربری</a>
<a href="#" onclick="showSection('admin-login-section')">ورود مدیر</a>
<a href="#" onclick="showSection('videos-section')">ویدیوها</a>
<a href="#" onclick="showSection('qna-section')">پرسش و پاسخ</a>
<a href="#" onclick="showSection('survey-section')">نظرسنجی</a>
<a href="#" onclick="showSection('geogebra-section')">GeoGebra</a>
<a href="#" onclick="showSection('equation-game-section')">بازی معادله</a>
<a href="#" onclick="showSection('create-exam-section')" id="createExamNavLink" style="display:none;">ساخت آزمون (مدیر)</a>
</nav>

<section id="home-section" style="display:block;">
<h2>به سایت Math with Afzali خوش آمدید!</h2>
<p>این سایت محلی برای یادگیری ریاضیات است. ما منابع آموزشی متنوعی شامل ویدیوها و ابزارهای تعاملی را برای شما فراهم کرده‌ایم.</p>
<p>مدیر سایت: امیرمحمد افضلی</p>
</section>

<section id="register-section">
<h2>ثبت نام</h2>
<form onsubmit="handleRegister(event)">
<div class="form-group">
<label for="reg-username">نام کاربری:</label>
<input type="text" id="reg-username" required
