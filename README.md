Головна сторінка
HTML:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Головна сторінка</title>
</head>
<body>

    <nav>
        <ul>
            <li><a href="index.html">Головна</a></li>
            <li><a href="sales.html">Продажі</a></li>
            <li><a href="pos.html">Касовий термінал</a></li>
            <li><a href="inventory.html">Склад</a></li>
            <li><a href="purchase.html">Купівля</a></li>
            <li><a href="accounting.html">Бухоблік</a></li>
            <li><a href="account-settings.html">Налаштування</a></li>
        </ul>
    </nav>

    <header>
        <h1>Ласкаво просимо на головну сторінку</h1>
    </header>

    <section class="main-content">
        <p>Вітаємо вас у нашому інтернет-магазині! Тут ви знайдете найкращі товари за доступними цінами.</p>
        <div class="product">
            <h2>Комплекс вітамінів</h2>
            <p>Для підтримки вітамінного балансу. Ціна: $19.99</p>
        </div>
    </section>

</body>
</html>

CSS:
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    background-color: #f4f4f4;
}

nav {
    background-color: #333;
    color: #fff;
    padding: 15px 0;
    text-align: center;
}

nav ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
}

nav li {
    display: inline;
    margin-right: 20px;
}

nav a {
    text-decoration: none;
    color: #fff;
    font-weight: bold;
}

header {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 15px 0;
}

.main-content {
    margin: 20px;
    padding: 20px;
    background-color: #fff;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.product {
    margin-top: 20px;
}

.product img {
    max-width: 100%;
    height: auto;
    border-radius: 8px;
    margin-bottom: 10px;
}

h1, h2 {
    color: #333;
}

Продажі:

HTML:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <title>Сторінка продажів</title>
</head>
<body>

    <nav>
        <ul>
            <li><a href="index.html">Головна</a></li>
            <li><a href="sales.html">Продажі</a></li>
            <li><a href="pos.html">Касовий термінал</a></li>
            <li><a href="inventory.html">Склад</a></li>
            <li><a href="purchase.html">Купівля</a></li>
            <li><a href="accounting.html">Бухоблік</a></li>
            <li><a href="account-settings.html">Налаштування</a></li>
        </ul>
    </nav>

    <header>
        <h1>Сторінка продажів</h1>
    </header>

    <section class="main-content">
        <canvas id="salesChart"></canvas>
    </section>

    <script src="sales.js"></script>

</body>
</html>

CSS:
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    background-color: #f4f4f4;
}

nav {
    background-color: #333;
    color: #fff;
    padding: 15px 0;
    text-align: center;
}

nav ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
}

nav li {
    display: inline;
    margin-right: 20px;
}

nav a {
    text-decoration: none;
    color: #fff;
    font-weight: bold;
}

header {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 15px 0;
}

.main-content {
    margin: 20px;
    padding: 20px;
    background-color: #fff;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

h1, h2 {
    color: #333;
}

JS:
document.addEventListener("DOMContentLoaded", function() {
    var ctx = document.getElementById('salesChart').getContext('2d');
    var salesChart = new Chart(ctx, {
        type: 'bar',
        data: {
            labels: ['Січень', 'Лютий', 'Березень', 'Квітень', 'Травень', 'Червень'],
            datasets: [{
                label: 'Продажі за місяць',
                backgroundColor: 'rgba(75, 192, 192, 0.2)',
                borderColor: 'rgba(75, 192, 192, 1)',
                borderWidth: 1,
                data: [65, 59, 80, 81, 56, 55]
            }]
        },
        options: {
            scales: {
                y: {
                    beginAtZero: true
                }
            }
        }
    });
});

Касовий термінал
HTML:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <script src="pos.js"></script>
    <title>Касовий термінал</title>
</head>
<body>

    <nav>
        <ul>
            <li><a href="index.html">Головна</a></li>
            <li><a href="sales.html">Продажі</a></li>
            <li><a href="pos.html">Касовий термінал</a></li>
            <li><a href="inventory.html">Склад</a></li>
            <li><a href="purchase.html">Купівля</a></li>
            <li><a href="accounting.html">Бухоблік</a></li>
            <li><a href="account-settings.html">Налаштування</a></li>
        </ul>
    </nav>

    <header>
        <h1>Касовий термінал</h1>
    </header>

    <section class="main-content">
        <button onclick="editSession()">Редагувати сесію</button>
        <button onclick="startNewSession()">Нова сесія</button>

        <div class="balance">
            <h2>Баланс відкриття:</h2>
            <p id="openingBalance">0.00</p>
        </div>
    </section>

</body>
</html>

CSS:
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    background-color: #f4f4f4;
}

nav {
    background-color: #333;
    color: #fff;
    padding: 15px 0;
    text-align: center;
}

nav ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
}

nav li {
    display: inline;
    margin-right: 20px;
}

nav a {
    text-decoration: none;
    color: #fff;
    font-weight: bold;
}

header {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 15px 0;
}

.main-content {
    margin: 20px;
    padding: 20px;
    background-color: #fff;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

button {
    display: inline-block;
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
    background-color: #4CAF50;
    color: #fff;
    border: none;
    border-radius: 4px;
    margin-right: 10px;
}

button:hover {
    background-color: #45a049;
}

.balance {
    text-align: center;
    margin-top: 30px;
}

.balance h2 {
    margin-bottom: 10px;
    color: #333;
}

.balance p {
    font-size: 20px;
    font-weight: bold;
    color: #4CAF50;
}

Склад
HTML:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Склад</title>
</head>
<body>

    <nav>
        <ul>
            <li><a href="index.html">Головна</a></li>
            <li><a href="sales.html">Продажі</a></li>
            <li><a href="pos.html">Касовий термінал</a></li>
            <li><a href="inventory.html">Склад</a></li>
            <li><a href="purchase.html">Купівля</a></li>
            <li><a href="accounting.html">Бухоблік</a></li>
            <li><a href="account-settings.html">Налаштування</a></li>
        </ul>
    </nav>

    <header>
        <h1>Склад</h1>
    </header>

    <section class="main-content">
        <div class="transactions">
            <h2>Останні транзакції</h2>
            <ul id="transactionList">
                <!-- Сюди будуть додаватись транзакції за допомогою JavaScript -->
            </ul>
        </div>

        <div class="counts">
            <h2>Статистика</h2>
            <p>Кількість надходжень: <span id="incomingCount">0</span></p>
            <p>Кількість внутрішніх переміщень: <span id="internalMoveCount">0</span></p>
            <p>Кількість запізнених замовлень: <span id="delayedOrderCount">0</span></p>
        </div>
    </section>

    <script src="inventory.js"></script>

</body>
</html>

CSS:
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    background-color: #f4f4f4;
}

nav {
    background-color: #333;
    color: #fff;
    padding: 15px 0;
    text-align: center;
}

nav ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
}

nav li {
    display: inline;
    margin-right: 20px;
}

nav a {
    text-decoration: none;
    color: #fff;
    font-weight: bold;
}

header {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 15px 0;
}

.main-content {
    margin: 20px;
    padding: 20px;
    background-color: #fff;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

button {
    display: inline-block;
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
    background-color: #4CAF50;
    color: #fff;
    border: none;
    border-radius: 4px;
    margin-right: 10px;
    transition: background-color 0.3s;
}

button:hover {
    background-color: #45a049;
}

.transactions {
    margin-top: 30px;
}

.transactions h2 {
    color: #333;
}

#transactionList {
    list-style-type: none;
    padding: 0;
}

#transactionList li {
    margin-bottom: 10px;
    padding: 15px;
    background-color: #f5f5f5;
    border-radius: 8px;
}

#transactionList li.delayed {
    background-color: #ffe6e6;
    border: 1px solid #ff6666;
}

.counts {
    margin-top: 30px;
}

.counts h2 {
    color: #333;
}

.counts p {
    font-size: 16px;
    margin: 10px 0;
}

.counts span {
    font-weight: bold;
    color: #4CAF50;
}

JS:
document.addEventListener("DOMContentLoaded", function () {
    // Додамо тестові дані для транзакцій
    var transactions = [
        { type: "5", description: "Отримано новий товар", delayed: false },
        { type: "8", description: "Внутрішнє переміщення", delayed: false },
        { type: "7", description: "Замовлено товар", delayed: true }
    ];

    // Відображаємо транзакції
    var transactionList = document.getElementById("transactionList");
    transactions.forEach(function (transaction) {
        var listItem = document.createElement("li");
        listItem.textContent = `${transaction.description} (${transaction.type})`;
        if (transaction.delayed) {
            listItem.style.color = "red";
        }
        transactionList.appendChild(listItem);
    });

    // Відображаємо статистику
    var incomingCount = transactions.filter(t => t.type === "incoming").length;
    var internalMoveCount = transactions.filter(t => t.type === "internalMove").length;
    var delayedOrderCount = transactions.filter(t => t.type === "order" && t.delayed).length;

    document.getElementById("incomingCount").textContent = incomingCount;
    document.getElementById("internalMoveCount").textContent = internalMoveCount;
    document.getElementById("delayedOrderCount").textContent = delayedOrderCount;
});

Купівля
HTML:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Купівля</title>
</head>
<body>

    <nav>
        <ul>
            <li><a href="index.html">Головна</a></li>
            <li><a href="sales.html">Продажі</a></li>
            <li><a href="pos.html">Касовий термінал</a></li>
            <li><a href="inventory.html">Склад</a></li>
            <li><a href="purchase.html">Купівля</a></li>
            <li><a href="accounting.html">Бухоблік</a></li>
            <li><a href="account-settings.html">Налаштування</a></li>
        </ul>
    </nav>

    <header>
        <h1>Купівля</h1>
    </header>

    <section class="main-content">
        <form id="purchaseForm">
            <label for="supplier">Постачальник:</label>
            <select id="supplier" name="supplier">
                <option value="supplier1">Постачальник 1</option>
                <option value="supplier2">Постачальник 2</option>
                <!-- Додайте інші постачальники за потреби -->
            </select>

            <label for="reference">Референс постачальника:</label>
            <input type="text" id="reference" name="reference" placeholder="Введіть референс">

            <label for="orderDate">Дата замовлення:</label>
            <input type="date" id="orderDate" name="orderDate">

            <h2>Товари:</h2>
            <table id="productTable">
                <thead>
                    <tr>
                        <th>Товар</th>
                        <th>Опис</th>
                        <th>Запланована дата</th>
                        <th>Кількість</th>
                        <th>Одиниця виміру</th>
                    </tr>
                </thead>
                <tbody>
                    <!-- Тут буде додаватися вміст таблиці за допомогою JavaScript -->
                </tbody>
            </table>

            <button type="button" onclick="addProduct()">Додати товар</button>
        </form>
    </section>

    <script src="purchase.js"></script>

</body>
</html>

CSS:
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    background-color: #f4f4f4;
}

nav {
    background-color: #333;
    color: #fff;
    padding: 15px 0;
    text-align: center;
}

nav ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
}

nav li {
    display: inline;
    margin-right: 20px;
}

nav a {
    text-decoration: none;
    color: #fff;
    font-weight: bold;
}

header {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 15px 0;
}

.main-content {
    margin: 20px;
    padding: 20px;
    background-color: #fff;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

#purchaseForm {
    margin-top: 20px;
}

label {
    display: block;
    margin-bottom: 5px;
}

select, input {
    width: 100%;
    padding: 10px;
    margin-bottom: 10px;
    box-sizing: border-box;
}

table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 20px;
}

th, td {
    padding: 10px;
    text-align: left;
    border: 1px solid #ddd;
}

th {
    background-color: #f2f2f2;
}

button {
    display: inline-block;
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
    background-color: #4CAF50;
    color: #fff;
    border: none;
    border-radius: 4px;
    margin-right: 10px;
    transition: background-color 0.3s;
}

button:hover {
    background-color: #45a049;
}

Бухоблік:
HTML:<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Бухоблік</title>
</head>
<body>

    <nav>
        <ul>
            <li><a href="index.html">Головна</a></li>
            <li><a href="sales.html">Продажі</a></li>
            <li><a href="pos.html">Касовий термінал</a></li>
            <li><a href="inventory.html">Склад</a></li>
            <li><a href="purchase.html">Купівля</a></li>
            <li><a href="accounting.html">Бухоблік</a></li>
            <li><a href="account-settings.html">Налаштування</a></li>
        </ul>
    </nav>

    <header>
        <h1>Бухоблік</h1>
    </header>

    <section class="main-content">
        <div class="account-window">
            <h2>Рахунки клієнтам (продаж)</h2>
            <button onclick="createInvoice('customer')">Створити новий рахунок</button>
            <div class="invoice-summary">
                <p class="confirmed">Підтверджено: $5000</p>
                <p class="expected">Очікується оплата: $1000</p>
            </div>
        </div>

        <div class="account-window">
            <h2>Рахунок постачальників (купівля)</h2>
            <button onclick="createInvoice('supplier')">Створити новий рахунок</button>
            <div class="invoice-summary">
                <p class="confirmed">Підтверджено: $3000</p>
                <p class="expected">Очікується оплата: $500</p>
            </div>
        </div>

        <div class="account-window">
            <h2>Банк</h2>
            <button onclick="createInvoice('bank')">Створити новий рахунок</button>
            <div class="invoice-summary">
                <p class="confirmed">Підтверджено: $10000</p>
                <p class="expected">Очікується оплата: $2000</p>
            </div>
        </div>

        <div class="account-window">
            <h2>Каса</h2>
            <button onclick="createInvoice('cash')">Створити новий рахунок</button>
            <div class="invoice-summary">
                <p class="confirmed">Підтверджено: $2000</p>
                <p class="expected">Очікується оплата: $300</p>
            </div>
        </div>
    </section>

    <script src="accounting.js"></script>

</body>
</html>

CSS:
body {
    font-family: 'Arial', sans-serif;
    margin: 0;
    padding: 0;
}

nav {
    background-color: #333;
    color: #fff;
    padding: 10px;
}

nav ul {
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex;
}

nav li {
    margin-right: 20px;
}

nav a {
    text-decoration: none;
    color: #fff;
    font-weight: bold;
    font-size: 16px;
}

header {
    background-color: #4CAF50;
    color: #fff;
    text-align: center;
    padding: 20px;
}

.main-content {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    padding: 20px;
}

.account-window {
    background-color: #fff;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    margin-bottom: 20px;
    padding: 20px;
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
}

.account-window h2 {
    color: #333;
    margin-bottom: 10px;
}

.account-window button {
    display: inline-block;
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
    background-color: #4CAF50;
    color: #fff;
    border: none;
    border-radius: 4px;
    margin-bottom: 10px;
    transition: background-color 0.3s;
}

.account-window button:hover {
    background-color: #45a049;
}

.invoice-summary {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.invoice-summary p {
    margin: 0;
    font-size: 14px;
}

.invoice-summary .confirmed,
.invoice-summary .expected {
    color: #4CAF50;
    margin-bottom: 5px;
}

Налаштування акаунту
HTML:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Налаштування</title>
</head>
<body>

    <nav>
        <ul>
            <li><a href="index.html">Головна</a></li>
            <li><a href="sales.html">Продажі</a></li>
            <li><a href="pos.html">Касовий термінал</a></li>
            <li><a href="inventory.html">Склад</a></li>
            <li><a href="purchase.html">Купівля</a></li>
            <li><a href="accounting.html">Бухоблік</a></li>
            <li><a href="account-settings.html">Налаштування</a></li>
        </ul>
    </nav>

    <header>
        <h1>Налаштування</h1>
    </header>

    <section class="main-content">
        <div class="settings-section">
            <h2>Керування правами доступу</h2>
            <button onclick="managePermissions()">Керувати правами доступу</button>
        </div>

        <div class="settings-section">
            <h2>Запрошення користувачів</h2>
            <button onclick="inviteUsers()">Запросити користувачів</button>
        </div>

        <div class="settings-section">
            <h2>Список користувачів онлайн</h2>
            <ul id="onlineUsersList">
                <!-- Список користувачів буде заповнюватися динамічно через JavaScript -->
            </ul>
        </div>
    </section>

    <script src="account-settings.js"></script>

</body>
</html>

CSS:
body {
    font-family: 'Arial', sans-serif;
    margin: 0;
    padding: 0;
}

nav {
    background-color: #333;
    color: #fff;
    padding: 10px;
}

nav ul {
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex;
}

nav li {
    margin-right: 20px;
}

nav a {
    text-decoration: none;
    color: #fff;
    font-weight: bold;
    font-size: 16px;
}

header {
    background-color: #4CAF50;
    color: #fff;
    text-align: center;
    padding: 20px;
}

.main-content {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    padding: 20px;
}

.settings-section {
    background-color: #fff;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    margin-bottom: 20px;
    padding: 20px;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
}

.settings-section h2 {
    color: #333;
    margin-bottom: 10px;
}

.settings-section button {
    display: inline-block;
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
    background-color: #4CAF50;
    color: #fff;
    border: none;
    border-radius: 4px;
    margin-bottom: 10px;
    transition: background-color 0.3s;
}

.settings-section button:hover {
    background-color: #45a049;
}

#onlineUsersList {
    list-style: none;
    padding: 0;
    margin: 0;
}

#onlineUsersList li {
    font-size: 14px;
    margin-bottom: 5px;
}

