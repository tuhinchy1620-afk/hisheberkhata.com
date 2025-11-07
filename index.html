<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>আমার দৈনিক হিসেব</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; font-family: Arial; }
        body { background: #f0f2f5; padding: 20px; }
        .container { max-width: 800px; margin: 0 auto; background: white; padding: 20px; border-radius: 10px; box-shadow: 0 0 10px rgba(0,0,0,0.1); }
        .header { background: #2E86C1; color: white; padding: 20px; text-align: center; border-radius: 10px; margin-bottom: 20px; }
        .login-box, .main-app { text-align: center; padding: 30px; }
        input, button { padding: 10px; margin: 5px; border: 1px solid #ddd; border-radius: 5px; }
        button { background: #27ae60; color: white; border: none; cursor: pointer; }
        table { width: 100%; border-collapse: collapse; margin: 20px 0; }
        th, td { border: 1px solid #ddd; padding: 10px; text-align: left; }
        th { background: #34495e; color: white; }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>আমার দৈনিক হিসেব</h1>
            <p>Netlify এ হোস্টেড</p>
        </div>

        <div class="login-box" id="loginSection">
            <h2>লগইন করুন</h2>
            <input type="text" id="username" placeholder="ইউজারনেম" value="admin"><br>
            <input type="password" id="password" placeholder="পাসওয়ার্ড" value="12345"><br>
            <button onclick="login()">লগইন</button>
        </div>

        <div class="main-app" id="mainApp" style="display:none">
            <button onclick="logout()" style="background:red;">লগআউট</button>
            <h2>নতুন এন্ট্রি</h2>
            <input type="date" id="entryDate">
            <input type="text" id="description" placeholder="বিবরণ">
            <input type="number" id="amount" placeholder="টাকা">
            <select id="type">
                <option value="income">আয়</option>
                <option value="expense">খরচ</option>
            </select>
            <button onclick="addEntry()">যোগ করুন</button>

            <div id="entriesList"></div>
            <div id="totalSection"></div>
        </div>
    </div>

    <script>
        function login() {
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            if (username === "admin" && password === "12345") {
                document.getElementById('loginSection').style.display = 'none';
                document.getElementById('mainApp').style.display = 'block';
                loadEntries();
            } else {
                alert('ভুল ইউজারনেম বা পাসওয়ার্ড!');
            }
        }

        function logout() {
            document.getElementById('loginSection').style.display = 'block';
            document.getElementById('mainApp').style.display = 'none';
        }

        function addEntry() {
            const date = document.getElementById('entryDate').value;
            const description = document.getElementById('description').value;
            const amount = parseFloat(document.getElementById('amount').value);
            const type = document.getElementById('type').value;

            if (!date || !description || !amount) {
                alert('সব তথ্য পূরণ করুন!');
                return;
            }

            const entries = JSON.parse(localStorage.getItem('expenseEntries') || '[]');
            entries.push({ id: Date.now(), date, description, amount, type });
            localStorage.setItem('expenseEntries', JSON.stringify(entries));
            loadEntries();
            
            document.getElementById('description').value = '';
            document.getElementById('amount').value = '';
        }

        function deleteEntry(id) {
            if (confirm('ডিলিট করতে চান?')) {
                const entries = JSON.parse(localStorage.getItem('expenseEntries') || '[]');
                const filtered = entries.filter(entry => entry.id !== id);
                localStorage.setItem('expenseEntries', JSON.stringify(filtered));
                loadEntries();
            }
        }

        function loadEntries() {
            const entries = JSON.parse(localStorage.getItem('expenseEntries') || '[]');
            const entriesList = document.getElementById('entriesList');
            const totalSection = document.getElementById('totalSection');

            if (entries.length === 0) {
                entriesList.innerHTML = '<p>কোনো এন্ট্রি নেই</p>';
                totalSection.innerHTML = '';
                return;
            }

            let tableHTML = '<table><tr><th>তারিখ</th><th>বিবরণ</th><th>টাইপ</th><th>টাকা</th><th>কাজ</th></tr>';
            let totalIncome = 0;
            let totalExpense = 0;

            entries.forEach(entry => {
                if (entry.type === 'income') totalIncome += entry.amount;
                else totalExpense += entry.amount;

                tableHTML += `
                    <tr>
                        <td>${entry.date}</td>
                        <td>${entry.description}</td>
                        <td>${entry.type === 'income' ? 'আয়' : 'খরচ'}</td>
                        <td>${entry.amount} ৳</td>
                        <td><button onclick="deleteEntry(${entry.id})" style="background:red;">ডিলিট</button></td>
                    </tr>
                `;
            });

            tableHTML += '</table>';
            entriesList.innerHTML = tableHTML;

            const balance = totalIncome - totalExpense;
            totalSection.innerHTML = `
                <div style="background:#2ecc71; color:white; padding:15px; border-radius:10px;">
                    <h3>মোট সারাংশ</h3>
                    <p>মোট আয়: ${totalIncome} ৳</p>
                    <p>মোট খরচ: ${totalExpense} ৳</p>
                    <p>ব্যালেন্স: ${balance} ৳</p>
                </div>
            `;
        }

        // আজকের তারিখ সেট করুন
        window.onload = function() {
            document.getElementById('entryDate').value = new Date().toISOString().split('T')[0];
        };
    </script>
</body>
</html>
