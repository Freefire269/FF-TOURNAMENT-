<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FF Tournament</title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@picocss/pico@1/css/pico.min.css">
    <style>
        body {
            background-color: #f7f7f7;
        }
        .tournament-list, .registration-form, .payment-section {
            margin-bottom: 2rem;
            padding: 1rem;
            border: 1px solid #ddd;
            border-radius: 8px;
        }
        h1 {
            text-align: center;
        }
    </style>
</head>
<body>
    <nav class="container-fluid">
        <ul>
            <li><strong>FF Tournament</strong></li>
        </ul>
        <ul>
            <li><a href="#tournaments">Tournaments</a></li>
            <li><a href="#register">Register</a></li>
            <li><a href="#payment">Payment</a></li>
        </ul>
    </nav>

    <main class="container">
        <header>
            <h1>Welcome to FF Tournament</h1>
            <p>Join thrilling Free Fire tournaments and showcase your skills!</p>
        </header>

        <!-- Tournament List -->
        <section id="tournaments" class="tournament-list">
            <h2>Tournament List</h2>
            <ul>
                <li>
                    <strong>Tournament 1</strong> - Date: 20th Jan 2025 - Entry Fee: $10
                    <button onclick="joinTournament('Tournament 1')">Join</button>
                </li>
                <li>
                    <strong>Tournament 2</strong> - Date: 25th Jan 2025 - Entry Fee: $15
                    <button onclick="joinTournament('Tournament 2')">Join</button>
                </li>
                <li>
                    <strong>Tournament 3</strong> - Date: 30th Jan 2025 - Entry Fee: $20
                    <button onclick="joinTournament('Tournament 3')">Join</button>
                </li>
            </ul>
        </section>

        <!-- Tournament Registration -->
        <section id="register" class="registration-form">
            <h2>Register a New Tournament</h2>
            <form>
                <label for="tournamentName">Tournament Name:</label>
                <input type="text" id="tournamentName" name="tournamentName" placeholder="Enter tournament name" required>
                
                <label for="date">Date:</label>
                <input type="date" id="date" name="date" required>
                
                <label for="entryFee">Entry Fee:</label>
                <input type="number" id="entryFee" name="entryFee" placeholder="Enter entry fee" required>
                
                <button type="submit" onclick="event.preventDefault(); registerTournament()">Register Tournament</button>
            </form>
        </section>

        <!-- Payment Section -->
        <section id="payment" class="payment-section">
            <h2>Payment</h2>
            <p>Select a tournament and proceed with payment:</p>
            <form>
                <label for="tournamentSelect">Tournament:</label>
                <select id="tournamentSelect" name="tournamentSelect">
                    <option value="Tournament 1">Tournament 1 - $10</option>
                    <option value="Tournament 2">Tournament 2 - $15</option>
                    <option value="Tournament 3">Tournament 3 - $20</option>
                </select>

                <label for="paymentMethod">Payment Method:</label>
                <select id="paymentMethod" name="paymentMethod">
                    <option value="Credit Card">Credit Card</option>
                    <option value="PayPal">PayPal</option>
                    <option value="Crypto">Crypto</option>
                </select>
                
                <button type="submit" onclick="event.preventDefault(); processPayment()">Proceed to Pay</button>
            </form>
        </section>
    </main>

    <footer class="container">
        <small>
            <a href="#">Privacy Policy</a> • <a href="#">Terms of Service</a>
        </small>
    </footer>

    <script>
        // Functionality placeholders
        function joinTournament(name) {
            alert(`You have joined ${name}`);
        }

        function registerTournament() {
            const name = document.getElementById('tournamentName').value;
            const date = document.getElementById('date').value;
            const fee = document.getElementById('entryFee').value;

            alert(`Tournament Registered: ${name}, Date: ${date}, Entry Fee: $${fee}`);
        }

        function processPayment() {
            const tournament = document.getElementById('tournamentSelect').value;
            const method = document.getElementById('paymentMethod').value;

            alert(`Payment for ${tournament} using ${method} was successful.`);
        }
    </script>
</body>
</html>
