<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>الوقت منذ هدف ناصر منسي</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f4f4f9;
            color: #333;
            margin: 0;
            padding: 0;
            direction: rtl;
        }
        .container {
            margin-top: 50px;
        }
        .time {
            font-size: 1.5rem;
            margin: 20px 0;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>الوقت منذ هدف ناصر منسي</h1>
        <p>هدف ناصر منسي ضد الأهلي في السوبر الأفريقي.</p>
        <div class="time" id="time-since"></div>
    </div>

    <script>
        // تاريخ الهدف (قم بتعديله إذا كنت تعرف التاريخ المحدد)
        const goalDate = new Date("2024-10-01T22:47:00"); // مثال لتاريخ الهدف

        function updateTime() {
            const now = new Date();
            const diff = now - goalDate;

            const weeks = Math.floor(diff / (1000 * 60 * 60 * 24 * 7));
            const days = Math.floor((diff % (1000 * 60 * 60 * 24 * 7)) / (1000 * 60 * 60 * 24));
            const hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((diff % (1000 * 60)) / 1000);

            document.getElementById("time-since").innerText = 
                `${weeks} أسبوع، ${days} يوم، ${hours} ساعة، ${minutes} دقيقة، ${seconds} ثانية`;
        }

        setInterval(updateTime, 1000); // تحديث كل ثانية
    </script>
</body>
</html>
