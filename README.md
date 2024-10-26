<!DOCTYPE html>
<html lang="uk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Оплата буфет</title>
    <style>
        /* Стиль для фону */
        body {
            background-image: url('https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSJZqKao76q9UNbduH1_UKeCBeuSVD0ZYHaUA&s'); /* Заміни на URL твоєї картинки */
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            font-family: Arial, sans-serif;
            color: #333;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }
        /* Основний контейнер для карток */
        .container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            background-color: rgba(255, 255, 255, 0.8);
            padding: 20px;
            border-radius: 8px;
        }
        /* Стиль для кожної картки */
        .card {
            width: 200px;
            padding: 15px;
            border-radius: 8px;
            background-color: #f4f4f4;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            text-align: center;
            font-size: 16px;
        }
        .card h2 {
            font-size: 20px;
            margin: 10px 0;
        }
        .card p {
            font-size: 14px;
            color: #666;
            border: 1px solid #ccc; /* Додає рамку */
            padding: 5px;
            border-radius: 4px; /* Згладжує кути рамки */
            margin: 10px 0; /* Відстань між параграфами */
        }
        /* Кнопка копіювання */
        .copy-button {
            background-color: #4CAF50;
            color: white;
            padding: 5px 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 14px;
        }
        /* Стиль для логотипів */
        .card img {
            width: 50%; /* Встановлює ширину логотипів */
            margin: 10px 0; /* Відстань навколо логотипів */
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="card">
            <img src="data:image/jpeg;base64,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" alt="Монобанк"> <!-- Зображення Монобанк -->
            <h2>Монобанк</h2>
            <p>Опис картки Монобанк</p>
            <p id="card-number-1">Номер карти: 4441 1111 3882 6197</p>
            <button class="copy-button" onclick="copyToClipboard('card-number-1')">Скопіювати номер</button>
        </div>
        <div class="card">
            <img src="data:image/png;base64,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" alt="ПриватБанк"> <!-- Зображення ПриватБанк -->
            <h2>ПриватБанк</h2>
            <p>Опис картки ПриватБанк</p>
            <p id="card-number-2">Номер карти: 4149 6090 2971 8972</p>
            <button class="copy-button" onclick="copyToClipboard('card-number-2')">Скопіювати номер</button>
        </div>
        <!-- Додай більше карток, якщо потрібно -->
    </div>

    <script>
        // Функція для копіювання тексту в буфер обміну
        function copyToClipboard(elementId) {
            const text = document.getElementById(elementId).innerText;
            navigator.clipboard.writeText(text)
                .then(() => alert('Номер карти скопійовано!'))
                .catch(err => alert('Не вдалося скопіювати текст', err));
        }
    </script>
</body>
</html>
