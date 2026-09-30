<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AP Study Hub</title>

    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
        }

        body {
            background: #f4f6fb;
            color: #20232a;
            transition: 0.3s;
        }

        header {
            background: #4D9AD1 ;
            color: blue;
            padding: 25px 8%;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        header h1 {
            font-size: 28px;
        }

        button {
            border: none;
            padding: 10px 16px;
            border-radius: 8px;
            cursor: pointer;
            background: white;
            color: #5b5ce2;
            font-weight: bold;
        }

        .container {
            width: 84%;
            max-width: 1100px;
            margin: 35px auto;
        }

        .welcome {
            margin-bottom: 30px;
        }

        .welcome h2 {
            margin-bottom: 8px;
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            margin-bottom: 35px;
        }

        .stat-card {
            background: white;
            padding: 22px;
            border-radius: 15px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.0.8);
        }

        .stat-card h3 {
            font-size: 14px;
            color: #777;
            margin-bottom: 8px;
        }

        .stat-card p {
            font-size: 28px;
            font-weight: bold;
        }

        .subjects {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
        }

        .subject {
            background: white;
            padding: 25px;
            border-radius: 15px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.08);
        }

        .subject-header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 15px;
        }

        .progress-container {
            background: #e5e7eb;
            height: 10px;
            border-radius: 10px;
            overflow: hidden;
            margin: 12px 0;
        }

        .progress {
            height: 100%;
            background: #5b5ce2;
            border-radius: 10px;
        }

        .study-btn {
            background: #5b5ce2;
            color: white;
            margin-top: 10px;
        }

        .dark {
            background: #171923;
            color: #f5f5f5;
        }

        .dark .stat-card,
        .dark .subject {
            background: #242735;
        }

        .dark .progress-container {
            background: #3b3f4d;
        }

        @media (max-width: 700px) {
            .stats,
            .subjects {
                grid-template-columns: 1fr;
            }

            header {
                padding: 20px;
            }

            .container {
                width: 90%;
            }
        }
    </style>
</head>

<body>

    <header>
        <h1>AP Study Hub</h1>
        <button onclick="toggleDarkMode()">Dark Mode</button>
    </header>

    <main class="container">

        <section class="welcome">
            <h2>Welcome back </h2>
            <p>Keep track of your AP subjects and stay consistent.</p>
        </section>

        <section class="stats">

            <div class="stat-card">
                <h3>Study Streak</h3>
                <p id="streak">7 days </p>
            </div>

            <div class="stat-card">
                <h3>Hours Studied</h3>
                <p id="hours">24</p>
            </div>

            <div class="stat-card">
                <h3>Overall Progress</h3>
                <p id="overall">63%</p>
            </div>

        </section>

        <h2>My AP Subjects</h2>

        <section class="subjects">

            <div class="subject">
                <div class="subject-header">
                    <h3>AP Biology</h3>
                    <span>72%</span>
                </div>

                <p>Cell biology, genetics, evolution</p>

                <div class="progress-container">
                    <div class="progress" style="width: 72%;"></div>
                </div>

                <button class="study-btn" onclick="study('Biology')">
                    Study Now
                </button>
            </div>

            <div class="subject">
                <div class="subject-header">
                    <h3>AP Chemistry</h3>
                    <span>55%</span>
                </div>

                <p>Stoichiometry, bonding, thermodynamics</p>

                <div class="progress-container">
                    <div class="progress" style="width: 55%;"></div>
                </div>

                <button class="study-btn" onclick="study('Chemistry')">
                    Study Now
                </button>
            </div>

            <div class="subject">
                <div class="subject-header">
                    <h3>AP Precalculus</h3>
                    <span>61%</span>
                </div>

                <p>Functions, trigonometry, rational functions</p>

                <div class="progress-container">
                    <div class="progress" style="width: 61%;"></div>
                </div>

                <button class="study-btn" onclick="study('Precalculus')">
                    Study Now
                </button>
            </div>

            <div class="subject">
                <div class="subject-header">
                    <h3>AP Statistics</h3>
                    <span>43%</span>
                </div>

                <p>Probability, distributions, inference</p>

                <div class="progress-container">
                    <div class="progress" style="width: 43%;"></div>
                </div>

                <button class="study-btn" onclick="study('Statistics')">
                    Study Now
                </button>
            </div>

        </section>

    </main>

    <script>

        function toggleDarkMode() {
            document.body.classList.toggle("dark");
        }

        function study(subject) {
            alert("Let's study " + subject + "!");
        }

    </script>

</body>
</html>