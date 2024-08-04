<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Coin Balance Mini App</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #FFA500; /* Orange background */
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh; /* Full height of the viewport */
            margin: 0;
            padding: 20px; /* Padding for mobile responsiveness */
            box-sizing: border-box; /* Include padding in height/width calculations */
        }
        
        .coin {
            width: 80px; /* Increased size for better touch targets */
            height: 80px; /* Increased size for better touch targets */
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 50px; /* Increased font size for the emoji */
            cursor: pointer;
            transition: transform 0.2s;
            margin-top: 10px; /* Added margin for spacing */
            background-color: white; /* White background for the coin button */
            border-radius: 50%; /* Rounded shape */
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); /* Shadow for depth */
        }

        .coin:hover {
            transform: scale(1.1);
        }

        .balance {
            font-size: 32px;
            font-weight: bold;
            margin-bottom: 10px; /* Space between balance and coin */
            color: white; /* White text for contrast */
        }

        .menu {
            display: flex;
            justify-content: space-around;
            width: 100%;
            margin-top: 20px;
        }

        .menu-item {
            background-color: #4CAF50; /* Green background for menu items */
            color: white;
            padding: 10px 15px; /* Adjusted padding for mobile */
            text-align: center;
            text-decoration: none;
            display: inline-block;
            font-size: 16px;
            border-radius: 5px;
            cursor: pointer;
        }

        .task-list, .mine, .wallet {
            margin-top: 20px;
            color: white;
            font-size: 18px;
            text-align: center;
        }

        .task, .mine-item {
            margin: 5px 0;
            padding: 10px;
            background-color: rgba(255, 255, 255, 0.2);
            border-radius: 10px;
        }

        .complete-task, .unlock-button, .upgrade-button, .max-lvl-button {
            margin-left: 10px;
            background-color: #FF6347; /* Tomato color for buttons */
            color: white;
            border: none;
            padding: 5px 10px;
            border-radius: 5px;
            cursor: pointer;
        }

        .completed, .max-lvl-button {
            background-color: #808080; /* Gray color for completed tasks and max level */
            cursor: default;
        }

        .coming-soon {
            font-size: 36px;
            font-weight: bold;
            color: white;
        }

        .message {
            font-size: 18px;
            color: white;
            margin-top: 10px;
        }

        @media (max-width: 768px) {
            .menu-item {
                font-size: 14px; /* Smaller font size for mobile */
            }
        }
    </style>
</head>
<body>
    <h1 style="color: white;">Welcome, <span id="username"></span>!</h1>
    <div class="balance" id="coin-balance">0 Coins</div> <!-- Coin balance displayed here -->
    <div class="coin" onclick="increaseCoinBalance()">
        🎃 <!-- Pumpkin emoji as the coin button -->
    </div>
    <div class="menu">
        <div class="menu-item" onclick="generateInviteLink()">Friends</div>
        <div class="menu-item" onclick="showTasks()">Tasks</div>
        <div class="menu-item" onclick="showMine()">Mine</div>
        <div class="menu-item" onclick="showWallet()">Wallet</div>
    </div>

    <div class="invite-link" id="invite-link"></div>
    <div class="friend-list" id="friend-list"></div>
    <div class="task-list" id="task-list"></div>
    <div class="mine" id="mine"></div>
    <div class="wallet" id="wallet"></div>

    <script>
        // Initialize Telegram Web App
        window.onload = function() {
            Telegram.WebApp.onEvent('visibilitychanged', function() {
                if (Telegram.WebApp.isVisible) {
                    // Load user data when the app is visible
                    loadUserData();
                }
            });
        };

        // Mock user data storage
        let users = {}; // Store users by invite link
        let coinBalance = 0; // Initialize coin balance
        let tasks = [
            { id: 1, name: "Task 1", url: "https://example.com/task1", completed: false },
            { id: 2, name: "Task 2", url: "https://example.com/task2", completed: false },
            { id: 3, name: "Task 3", url: "https://example.com/task3", completed: false },
            { id: 4, name: "Task 4", url: "https://example.com/task4", completed: false },
            { id: 5, name: "Task 5", url: "https://example.com/task5", completed: false }
        ];

        function loadUserData() {
            // Get the user's name from Telegram
            document.getElementById('username').textContent = Telegram.WebApp.initDataUnsafe.user.first_name;

            // Get the initial coin balance from Telegram (you may need to set this up on your server)
            let initialBalance = parseInt(Telegram.WebApp.initDataUnsafe.user.balance) || 0;
            coinBalance = initialBalance;
            document.getElementById('coin-balance').textContent = coinBalance + " Coins";

            // Load coin balance and card data from local storage
            const storedBalance = localStorage.getItem('coinBalance');
            if (storedBalance) {
                coinBalance = parseInt(storedBalance);
                document.getElementById('coin-balance').textContent = coinBalance + " Coins";
            }

            const storedCards = JSON.parse(localStorage.getItem('cards'));
            if (storedCards) {
                cards = storedCards;
            }
        }

        function saveUserData() {
            // Save coin balance and card data to local storage
            localStorage.setItem('coinBalance', coinBalance);
            localStorage.setItem('cards', JSON.stringify(cards));
        }

        function increaseCoinBalance() {
            coinBalance++;
            document.getElementById('coin-balance').textContent = coinBalance + " Coins";

            // Send the updated balance to Telegram
            Telegram.WebApp.sendData(JSON.stringify({ balance: coinBalance }));

            // Save user data
            saveUserData();
        }

        function generateInviteLink() {
            // Generate a random invite link
            const inviteCode = Math.random().toString(36).substring(2, 8); // Random string
            const inviteLink = `https://yourdomain.com/join?invite=${inviteCode}`; // Replace with your domain

            // Store the user data associated with the invite code
            users[inviteCode] = {
                name: document.getElementById('username').textContent,
                balance: coinBalance
            };

            document.getElementById('invite-link').textContent = `Invite your friends using this link: ${inviteLink}`;
        }

        function showFriendList() {
            const friendList = document.getElementById('friend-list');
            friendList.innerHTML = ''; // Clear previous entries

            // Display friends who joined using the invite links
            for (const invite in users) {
                const user = users[invite];
                friendList.innerHTML += `<div>${user.name} - ${user.balance} Coins (Joined via: ${invite})</div>`;
            }
        }

        function showTasks() {
            const taskList = document.getElementById('task-list');
            taskList.innerHTML = ''; // Clear previous tasks

            tasks.forEach(task => {
                if (task.completed) {
                    taskList.innerHTML += `
                        <div class="task">
                            ${task.name}
                            <button class="complete-task completed" disabled>Completed</button>
                        </div>
                    `;
                } else {
                    taskList.innerHTML += `
                        <div class="task">
                            ${task.name}
                            <button class="complete-task" onclick="completeTask('${task.url}')">Complete</button>
                        </div>
                    `;
                }
            });
        }

        function completeTask(taskUrl) {
            // Find the task based on the URL
            const task = tasks.find(t => t.url === taskUrl);
            if (task && !task.completed) {
                task.completed = true; // Mark task as completed
                coinBalance += 500; // Add 500 coins
                document.getElementById('coin-balance').textContent = coinBalance + " Coins"; // Update balance

                // Send the updated balance to Telegram
                Telegram.WebApp.sendData(JSON.stringify({ balance: coinBalance }));

                // Redirect the user to the task URL
                window.open(taskUrl, '_blank');

                // Update the task display immediately
                showTasks();

                // Save user data
                saveUserData();
            }
        }

        let cards = {
            injection: { level: 0, profit: 0 },
            poison: { level: 0, profit: 0 }
        };

        function showMine() {
            const mine = document.getElementById('mine');
            mine.innerHTML = ''; // Clear previous content

            mine.innerHTML += `
                <div class="mine-item" id="injection-card">
                    💉 Injection <br>
                    Profit per second: <span id="injection-profit">+${cards.injection.profit}</span> coins <br>
                    Level: <span id="injection-level">${cards.injection.level}</span> <br>
                    ${cards.injection.level === 0 ? `<button class="unlock-button" onclick="unlockCard('injection', 2000, 200)">Unlock for 2000 coins</button>` : ''}
                </div>
                <div class="mine-item" id="poison-card">
                    🧪 Poison <br>
                    Profit per second: <span id="poison-profit">+${cards.poison.profit}</span> coins <br>
                    Level: <span id="poison-level">${cards.poison.level}</span> <br>
                    ${cards.poison.level === 0 ? `<button class="unlock-button" onclick="unlockCard('poison', 5000, 500)">Unlock for 5000 coins</button>` : ''}
                </div>
            `;

            // Add upgrade buttons if the cards are already unlocked
            if (cards.injection.level > 0 && cards.injection.level < 5) {
                addUpgradeButton('injection');
            } else if (cards.injection.level === 5) {
                document.getElementById('injection-card').innerHTML += `<button class="max-lvl-button" disabled>Max Level</button>`;
            }

            if (cards.poison.level > 0 && cards.poison.level < 5) {
                addUpgradeButton('poison');
            } else if (cards.poison.level === 5) {
                document.getElementById('poison-card').innerHTML += `<button class="max-lvl-button" disabled>Max Level</button>`;
            }
        }

        function unlockCard(card, cost, profit) {
            if (coinBalance >= cost) {
                coinBalance -= cost;
                document.getElementById('coin-balance').textContent = coinBalance + " Coins";
                cards[card].level = 1;
                cards[card].profit = profit;
                document.getElementById(`${card}-profit`).textContent = `+${profit}`;
                document.getElementById(`${card}-level`).textContent = "1";
                document.getElementById(`${card}-card`).innerHTML += `<button class="upgrade-button" onclick="upgradeCard('${card}', 2, 8000, 4000)">Upgrade to level 2 for 8000 coins</button>`;
                document.querySelector(`#${card}-card .unlock-button`).remove();
                
                setInterval(() => {
                    coinBalance += profit;
                    document.getElementById('coin-balance').textContent = coinBalance + " Coins";
                }, 1000);

                // Save user data
                saveUserData();
            } else {
                alert("No balance");
            }
        }

        function upgradeCard(card, level, cost, profit) {
            if (coinBalance >= cost) {
                coinBalance -= cost;
                document.getElementById('coin-balance').textContent = coinBalance + " Coins";
                cards[card].level = level;
                cards[card].profit = profit;
                document.getElementById(`${card}-level`).textContent = level;
                document.getElementById(`${card}-profit`).textContent = `+${profit}`;
                
                document.querySelector(`#${card}-card .upgrade-button`).remove();
                if (level < 5) {
                    addUpgradeButton(card);
                } else {
                    document.getElementById(`${card}-card`).innerHTML += `<button class="max-lvl-button" disabled>Max Level</button>`;
                }

                setInterval(() => {
                    coinBalance += profit;
                    document.getElementById('coin-balance').textContent = coinBalance + " Coins";
                }, 1000);

                // Save user data
                saveUserData();
            } else {
                alert("No balance");
            }
        }

        function addUpgradeButton(card) {
            const level = cards[card].level;
            const nextLevel = level + 1;
            const nextCost = level === 1 ? 8000 : level === 2 ? 10000 : 12000;
            const nextProfit = level === 1 ? 4000 : level === 2 ? 8000 : 10000;

            document.getElementById(`${card}-card`).innerHTML += `<button class="upgrade-button" onclick="upgradeCard('${card}', ${nextLevel}, ${nextCost}, ${nextProfit})">Upgrade to level ${nextLevel} for ${nextCost} coins</button>`;
        }

        function showWallet() {
            const wallet = document.getElementById('wallet');
            wallet.innerHTML = `
                <div class="coming-soon">Coming Soon</div>
                <div class="message">We are dealing with blockchain network to get listed and verified. We will notify you when we are in wallet.</div>
                <div class="message">Thank you</div>
            `;
        }
    </script>
</body>
</html>
