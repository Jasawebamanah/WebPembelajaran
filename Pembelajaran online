<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Platform Edukasi Islam</title>
    <script>
        const users = [
            { username: "pelajar1", password: "123456", role: "pelajar" },
            { username: "pengajar1", password: "abcdef", role: "pengajar" },
            { username: "affiliate1", password: "789012", role: "affiliate" }
        ];

        function login() {
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            
            const user = users.find(user => user.username === username && user.password === password);
            
            if (user) {
                document.getElementById('loginMessage').innerText = `Selamat datang, ${user.role}!`;
                if (user.role === 'pelajar') {
                    window.location.href = "dashboard_pelajar.html";
                } else if (user.role === 'pengajar') {
                    window.location.href = "dashboard_pengajar.html";
                } else {
                    window.location.href = "dashboard_affiliate.html";
                }
            } else {
                document.getElementById('loginMessage').innerText = "Username atau password salah!";
            }
        }

        const classes = [
            { title: "E-book Fiqih", type: "ebook" },
            { title: "E-Course Tahfidz", type: "ecourse" },
            { title: "Template Kajian", type: "template" },
            { title: "Zoom Tahsin", type: "zoom" }
        ];

        function showClasses() {
            const classList = document.getElementById('classList');
            classList.innerHTML = "";
            classes.forEach(klass => {
                const classItem = document.createElement('li');
                classItem.innerText = `${klass.title} (${klass.type})`;
                classList.appendChild(classItem);
            });
        }

        const notes = [];

        function addNote() {
            const noteContent = document.getElementById('noteContent').value;
            if (noteContent) {
                notes.push(noteContent);
                document.getElementById('noteContent').value = "";
                displayNotes();
            }
        }

        function displayNotes() {
            const notesList = document.getElementById('notesList');
            notesList.innerHTML = "";
            notes.forEach(note => {
                const noteItem = document.createElement('li');
                noteItem.innerText = note;
                notesList.appendChild(noteItem);
            });
        }

        function makePayment() {
            const amount = document.getElementById('amount').value;
            if (amount) {
                alert(`Terima kasih atas donasi atau pembayaran sebesar Rp${amount}!`);
            }
        }
    </script>
</head>
<body>
    <h1>Platform Edukasi Islam</h1>

    <h2>Login</h2>
    <input type="text" id="username" placeholder="Username" required>
    <input type="password" id="password" placeholder="Password" required>
    <button onclick="login()">Login</button>
    <p id="loginMessage"></p>

    <h2>Kelas</h2>
    <button onclick="showClasses()">Tampilkan Kelas</button>
    <ul id="classList"></ul>

    <h2>Catatan Pelajar</h2>
    <textarea id="noteContent" placeholder="Tulis catatan..."></textarea>
    <button onclick="addNote()">Tambahkan Catatan</button>
    <ul id="notesList"></ul>

    <h2>Pembayaran dan Donasi</h2>
    <input type="number" id="amount" placeholder="Jumlah Pembayaran/Donasi" required>
    <button onclick="makePayment()">Bayar / Donasi</button>
</body>
</html>
