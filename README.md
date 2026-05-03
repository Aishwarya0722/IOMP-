# IOMP- FRONTEND HTML CODE
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CyberShield - Cybersecurity Assessment Platform</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        :root {
            --bg-main: #0f172a;
            --card-bg: #ffffff;
            --primary-color: #4f46e5;
            --secondary-color: #7c3aed;
            --text-main: #1e293b;
            --text-muted: #64748b;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f1f5f9;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }

        .app-container {
            background: #ffffff;
            width: 100%;
            max-width: 1150px;
            border-radius: 16px;
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1);
            display: flex;
            flex-direction: row;
            min-height: 620px;
            overflow: hidden;
        }

        .sidebar {
            width: 260px;
            background-color: #090d16;
            color: #cbd5e1;
            padding: 28px 20px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .sidebar h1 {
            color: #ffffff;
            font-size: 1.4rem;
            margin-bottom: 2.5rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .nav-links {
            display: flex;
            flex-direction: column;
            gap: 8px;
        }

        .nav-btn {
            background: transparent;
            border: none;
            color: #94a3b8;
            padding: 12px 16px;
            border-radius: 8px;
            text-align: left;
            font-size: 0.95rem;
            cursor: pointer;
            transition: all 0.2s ease-in-out;
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .nav-btn:hover, .nav-btn.active {
            background-color: #1e293b;
            color: #ffffff;
        }

        .nav-btn.active {
            background-color: #4f46e5;
        }

        .user-panel {
            font-size: 0.85rem;
            color: #64748b;
        }

        .user-panel span {
            color: #ffffff;
            display: block;
            margin-top: 4px;
            font-weight: 500;
        }

        .logout-btn {
            background-color: #1e293b;
            color: #f87171;
            border: none;
            padding: 10px 14px;
            border-radius: 8px;
            cursor: pointer;
            margin-top: 12px;
            font-size: 0.85rem;
            width: 100%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: background-color 0.2s;
        }

        .logout-btn:hover {
            background-color: rgba(153, 27, 27, 0.2);
        }

        .workspace {
            flex-grow: 1;
            padding: 40px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            background-color: #fafafa;
            overflow-y: auto;
            max-height: 620px;
        }

        .view {
            max-width: 800px;
            width: 100%;
            margin: 0 auto;
        }

        .view-center {
            text-align: center;
        }

        h2 {
            color: var(--text-main);
            font-size: 2.2rem;
            margin-bottom: 8px;
        }

        p {
            color: var(--text-muted);
            margin-bottom: 2rem;
        }

        .form-group {
            margin-bottom: 1.2rem;
            text-align: left;
        }

        label {
            display: block;
            font-size: 0.85rem;
            font-weight: 600;
            color: #475569;
            margin-bottom: 6px;
        }

        input {
            width: 100%;
            padding: 12px 14px;
            border: 1px solid #cbd5e1;
            border-radius: 8px;
            box-sizing: border-box;
            background-color: #ffffff;
            font-size: 0.95rem;
            transition: border 0.15s;
            outline: none;
        }

        input:focus {
            border-color: #4f46e5;
            box-shadow: 0 0 0 3px rgba(79, 70, 229, 0.2);
        }

        .btn-primary {
            width: 100%;
            padding: 14px;
            background: linear-gradient(135deg, #4f46e5 0%, #7c3aed 100%);
            color: white;
            border: none;
            border-radius: 8px;
            font-weight: bold;
            font-size: 1rem;
            cursor: pointer;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
            transition: opacity 0.2s;
        }

        .btn-primary:hover {
            opacity: 0.9;
        }

        .btn-secondary {
            width: 100%;
            padding: 12px;
            background-color: #ffffff;
            color: #4f46e5;
            border: 1px solid #cbd5e1;
            border-radius: 8px;
            font-weight: bold;
            font-size: 0.95rem;
            cursor: pointer;
            margin-top: 10px;
            transition: background-color 0.1s;
        }

        .btn-secondary:hover {
            background-color: #f1f5f9;
        }

        .hidden { display: none !important; }
        .flex { display: flex !important; }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 20px;
            margin-top: 2rem;
        }

        .card {
            background: #ffffff;
            border: 1px solid #e2e8f0;
            border-radius: 12px;
            padding: 24px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.02);
            cursor: pointer;
            transition: all 0.2s;
        }

        .card:hover {
            border-color: #4f46e5;
            box-shadow: 0 8px 16px rgba(0,0,0,0.04);
            transform: translateY(-2px);
        }

        table {
            width: 100%;
            border-collapse: collapse;
            text-align: left;
            margin-top: 1rem;
            background: white;
            border-radius: 8px;
            overflow: hidden;
        }

        th, td {
            padding: 16px;
            border-bottom: 1px solid #f1f5f9;
        }

        th {
            background-color: #f8fafc;
            color: #475569;
            font-size: 0.85rem;
            font-weight: 600;
        }

        .badge-success {
            background-color: #ecfdf5;
            color: #059669;
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 0.8rem;
        }

        .alert {
            margin-top: 20px;
            padding: 14px 18px;
            border-radius: 8px;
            font-size: 0.9rem;
        }

        .alert-success {
            background: #f0fdf4;
            border: 1px solid #bbf7d0;
            color: #15803d;
        }

        .alert-danger {
            background: #fef2f2;
            border: 1px solid #fecaca;
            color: #991b1b;
        }

        /* Extra components for new features */
        .widget-box {
            background: #ffffff;
            border: 1px solid #cbd5e1;
            border-radius: 8px;
            padding: 16px;
            margin-bottom: 1.5rem;
        }
        
        .chat-box {
            height: 140px;
            overflow-y: auto;
            background: #f8fafc;
            padding: 10px;
            border-radius: 6px;
            font-size: 0.85rem;
            margin-bottom: 10px;
            border: 1px solid #e2e8f0;
        }
    </style>
</head>
<body>

    <div class="app-container">
        <aside class="sidebar hidden" id="sidebar-nav">
            <div>
                <h1>
                    <i class="fas fa-shield-halved" style="color: #6366f1;"></i> CyberShield
                </h1>
                <nav class="nav-links">
                    <button class="nav-btn active" onclick="switchView('dashboard-view')">
                        <i class="fas fa-home"></i> Dashboard
                    </button>
                    <button class="nav-btn" onclick="switchView('modules-view')">
                        <i class="fas fa-book-open"></i> Modules
                    </button>
                    <button class="nav-btn" onclick="switchView('leaderboard-view')">
                        <i class="fas fa-trophy"></i> Leaderboard
                    </button>
                    <button class="nav-btn" onclick="switchView('profile-view')">
                        <i class="fas fa-user-circle"></i> Profile
                    </button>
                </nav>
            </div>
            <div class="user-panel">
                User: <span id="user-display">Agent</span>
                <button class="logout-btn" onclick="logout()">
                    <span>Sign Out</span> <i class="fas fa-right-from-bracket"></i>
                </button>
            </div>
        </aside>

        <main class="workspace">
            <div id="login-view" class="view">
                <div class="view-center">
                    <i class="fas fa-user-shield" style="font-size: 3.5rem; color: #4f46e5; margin-bottom: 1.5rem;"></i>
                    <h2>Sign In</h2>
                    <p>Access your platform telemetry and learning modules</p>
                </div>
                <form onsubmit="handleLogin(event)">
                    <div class="form-group">
                        <label>Email Address</label>
                        <input type="email" id="login-email" placeholder="agent@security.org" required>
                    </div>
                    <div class="form-group">
                        <label>Password</label>
                        <input type="password" id="login-password" placeholder="••••••••" required>
                    </div>
                    <button type="submit" class="btn-primary">Login</button>
                </form>
                <div style="text-align: center; margin-top: 1.5rem; font-size: 0.9rem;">
                    Don't have an account? <a onclick="switchView('register-view')" style="color: #4f46e5; font-weight: bold; cursor: pointer; text-decoration: underline;">Register</a>
                    <br><br>
                    <a onclick="switchView('forgot-view')" style="color: #7c3aed; cursor: pointer; text-decoration: underline;">Forgot Password?</a>
                </div>
            </div>

            <div id="register-view" class="view hidden">
                <div class="view-center" style="margin-bottom: 2rem;">
                    <h2>Register Account</h2>
                    <p>Start learning cybersecurity with us</p>
                </div>
                <form id="regForm" onsubmit="handleRegister(event)">
                    <div class="form-group">
                        <label>Username</label>
                        <input type="text" id="reg-username" required>
                    </div>
                    <div class="form-group">
                        <label>Email Address</label>
                        <input type="email" id="reg-email" required>
                    </div>
                    <div class="form-group">
                        <label>Password</label>
                        <input type="password" id="reg-password" oninput="validatePassword(this.value)" required>
                    </div>
                    <div id="rules-container" style="font-size: 0.75rem; color: #64748b; margin-bottom: 1.2rem;">
                        <p style="margin-bottom: 4px;">Password must contain:</p>
                        <ul style="margin: 0; padding-left: 15px;">
                            <li id="rule-length" style="color: #ef4444;"><i class="fas fa-circle-xmark"></i> At least 8 characters</li>
                            <li id="rule-upper" style="color: #ef4444;"><i class="fas fa-circle-xmark"></i> 1 Uppercase (A-Z)</li>
                            <li id="rule-lower" style="color: #ef4444;"><i class="fas fa-circle-xmark"></i> 1 Lowercase (a-z)</li>
                            <li id="rule-number" style="color: #ef4444;"><i class="fas fa-circle-xmark"></i> 1 Number (0-9)</li>
                            <li id="rule-symbol" style="color: #ef4444;"><i class="fas fa-circle-xmark"></i> 1 Symbol</li>
                        </ul>
                    </div>
                    <button type="submit" id="reg-submit-btn" class="btn-primary" disabled style="opacity: 0.6; cursor: not-allowed;">Create Account</button>
                    <button type="button" class="btn-secondary" onclick="switchView('login-view')">Back to Login</button>
                </form>
            </div>

            <div id="forgot-view" class="view hidden">
                <div class="view-center">
                    <h2>Password Recovery</h2>
                    <p>Enter your registered email address to receive a reset link</p>
                </div>
                <form onsubmit="handleForgotPassword(event)">
                    <div class="form-group">
                        <label>Email Address</label>
                        <input type="email" id="forgot-email" required>
                    </div>
                    <button type="submit" class="btn-primary">Send Reset Email</button>
                    <button type="button" class="btn-secondary" onclick="switchView('login-view')">Back to Login</button>
                </form>
            </div>

            <div id="reset-view" class="view hidden">
                <div class="view-center">
                    <h2>Reset Password</h2>
                    <p>Please enter your new password</p>
                </div>
                <form onsubmit="handleResetPassword(event)">
                    <div class="form-group">
                        <label>New Password</label>
                        <input type="password" id="reset-password" required>
                    </div>
                    <button type="submit" class="btn-primary">Update Password</button>
                </form>
            </div>

            <div id="dashboard-view" class="view hidden">
                <div style="background-color: #f0fdf4; border: 1px solid #bbf7d0; color: #15803d; padding: 16px 24px; border-radius: 8px; display: flex; justify-content: space-between; align-items: center; margin-bottom: 2.5rem;">
                    <div>
                        <i class="fas fa-medal" style="color: #eab308; font-size: 1.3rem;"></i> <strong id="level-title">Level 1 Novice Status</strong>
                    </div>
                    <div style="font-weight: 600;">XP Points: <span id="xp-display">0</span> XP</div>
                </div>

                <h2>Workspace Dashboard</h2>
                <p>Choose an action or course module below to launch a lesson.</p>
                
                <div class="widget-box">
                    <div style="display: flex; justify-content: space-between;">
                        <div>
                            <strong>Streak:</strong> <span id="streak-display">0 Days</span>
                        </div>
                        <div>
                            <strong>Total Badges:</strong> <span id="badge-display">0</span>
                        </div>
                    </div>
                </div>

                <div class="grid">
                    <div class="card" onclick="switchView('modules-view')">
                        <i class="fas fa-graduation-cap" style="color: #4f46e5; font-size: 1.8rem; margin-bottom: 12px;"></i>
                        <h3 style="font-size: 1.1rem; color: #1e293b; margin: 0 0 6px 0;">Course Modules</h3>
                        <p style="margin: 0; font-size: 0.85rem; color: #64748b;">Read study materials and attempt an adaptive quiz.</p>
                    </div>
                    <div class="card" onclick="switchView('leaderboard-view')">
                        <i class="fas fa-ranking-star" style="color: #4f46e5; font-size: 1.8rem; margin-bottom: 12px;"></i>
                        <h3 style="font-size: 1.1rem; color: #1e293b; margin: 0 0 6px 0;">Global Leaderboards</h3>
                        <p style="margin: 0; font-size: 0.85rem; color: #64748b;">Check how you compare to other analysts globally.</p>
                    </div>
                    <div class="card" onclick="logout()">
                        <i class="fas fa-door-open" style="color: #4f46e5; font-size: 1.8rem; margin-bottom: 12px;"></i>
                        <h3 style="font-size: 1.1rem; color: #1e293b; margin: 0 0 6px 0;">Sign Out</h3>
                        <p style="margin: 0; font-size: 0.85rem; color: #64748b;">Log out of your session securely.</p>
                    </div>
                </div>
            </div>

            <div id="modules-view" class="view hidden">
                <h2 style="font-size: 1.9rem; margin-bottom: 16px;">Select a Module</h2>
                <div class="grid" id="modules-grid"></div>
                <button class="btn-secondary" style="max-width: 200px; margin-top: 2rem;" onclick="switchView('dashboard-view')">Back to Dashboard</button>
            </div>

            <div id="study-view" class="view hidden">
                <div style="background: #e0e7ff; border-left: 4px solid #4f46e5; padding: 18px; margin-bottom: 2rem; border-radius: 0 8px 8px 0;">
                    <h2 id="study-title" style="font-size: 1.5rem; color: #1e1b4b; margin: 0;">Module Study Material</h2>
                </div>
                <div style="background: #ffffff; border: 1px solid #cbd5e1; padding: 30px; border-radius: 12px; margin-bottom: 2rem; color: #475569; line-height: 1.6;">
                    <p id="study-content" style="margin: 0;">Loading content...</p>
                </div>
                <div style="display: flex; gap: 12px;">
                    <button class="btn-primary" onclick="enterAssessment()">Begin Quiz Assessment</button>
                    <button class="btn-secondary" onclick="switchView('modules-view')">Back</button>
                </div>
            </div>

            <div id="assessment-view" class="view hidden">
                <div style="background: #0f172a; color: white; padding: 16px 24px; border-radius: 10px 10px 0 0; display: flex; justify-content: space-between; align-items: center;">
                    <span style="font-size: 0.75rem; letter-spacing: 1px;">Adaptive AI Quiz</span>
                    <span id="difficulty-badge" style="background: #4f46e5; padding: 4px 12px; border-radius: 12px; font-size: 0.75rem;">Difficulty: Level 1</span>
                </div>
                <div style="background: white; border: 1px solid #cbd5e1; border-top: none; padding: 32px; border-radius: 0 0 10px 10px;">
                    <p id="question" style="font-weight: bold; color: #0f172a; font-size: 1.1rem; margin-bottom: 2rem; line-height: 1.5;">Loading question...</p>
                    <div id="options-container" style="display: flex; flex-direction: column; gap: 12px;"></div>
                </div>
                
                <div class="widget-box" style="margin-top: 1.5rem;">
                    <h4><i class="fas fa-robot" style="color: #7c3aed;"></i> AI Mentorship Assistant</h4>
                    <p style="font-size: 0.8rem; margin-bottom: 8px;">Ask the mentor a question about the current topic or for a hint.</p>
                    <div class="chat-box" id="chat-output">System: Hello! I am your AI Mentor. I'm ready to help you on this module.</div>
                    <div style="display: flex; gap: 8px;">
                        <input type="text" id="chat-input" placeholder="Ask for a hint..." style="margin: 0;">
                        <button onclick="askAIMentor()" class="btn-primary" style="width: auto; padding: 10px 16px; margin: 0;">Ask</button>
                    </div>
                </div>

                <button class="btn-secondary" style="margin-top: 1.5rem; max-width: 240px;" onclick="switchView('modules-view')"><i class="fas fa-arrow-left"></i> Return to Modules</button>
            </div>

            <div id="leaderboard-view" class="view hidden">
                <h2>Global Leaderboards</h2>
                <div style="overflow-x: auto;">
                    <table>
                        <thead>
                            <tr>
                                <th>Rank</th>
                                <th>Username</th>
                                <th>XP Points</th>
                            </tr>
                        </thead>
                        <tbody id="leaderboard-body"></tbody>
                    </table>
                </div>
                <button class="btn-secondary" style="max-width: 200px; margin-top: 2rem;" onclick="switchView('dashboard-view')">Back to Dashboard</button>
            </div>

            <div id="profile-view" class="view hidden">
                <h2>Analyst Profile</h2>
                <p>Overview of your metrics and credentials</p>
                <div class="widget-box">
                    <p style="margin: 4px 0;"><strong>Username:</strong> <span id="profile-username">Agent</span></p>
                    <p style="margin: 4px 0;"><strong>Email:</strong> <span id="profile-email">agent@security.org</span></p>
                    <p style="margin: 4px 0;"><strong>Level:</strong> <span id="profile-level">Level 1 Novice</span></p>
                    <p style="margin: 4px 0;"><strong>Total XP:</strong> <span id="profile-xp">0</span></p>
                    <p style="margin: 4px 0;"><strong>Current Streak:</strong> <span id="profile-streak">0 days</span></p>
                    
                    <div style="margin-top: 16px;">
                        <strong>Badges Earned:</strong>
                        <div id="profile-badges" style="margin-top: 8px; display: flex; gap: 8px;">None</div>
                    </div>
                </div>
                <button class="btn-secondary" style="max-width: 200px;" onclick="switchView('dashboard-view')">Back to Dashboard</button>
            </div>

            <div id="feedback" class="alert hidden"></div>
        </main>
    </div>

    <script>
        let currentUser = "";
        let currentDifficulty = 1;
        let selectedModule = 1;
        let startTime;

        // Persistent database storage directly in memory
        let localDatabase = {
            "agent@security.org": { 
                username: "Agent", 
                password: "Password123!", 
                xp: 420,
                streak: 3,
                badges: ["Bronze - Network"],
                level: 3,
                passedModules: [1],
                attempts: 1
            }
        };

        const modules = [
            { id: 1, title: "Network Security & Defense", short: "Network Security prevents unauthorized access across your system perimeter.", material: "Network security prevents unauthorized access across your system perimeter. Cryptographic protocols like HTTPS protect information when moving across networks. RLS limits data access inside database tables.", difficulty: 1 },
            { id: 2, title: "Password Hashing & Cryptography", short: "Explore the mechanics of defending against brute-force attacks.", material: "Cryptographic storage techniques (like Bcrypt) slow down authentication processing time to stop attackers from breaking your systems. Using strong policies and HIBP checking prevents breaches.", difficulty: 1 },
            { id: 3, title: "Phishing & Social Engineering", short: "Identify deceptive methods and fraudulent links used by actors.", material: "Social engineering is the psychological manipulation of people into performing actions or divulging confidential information. Phishing leverages emails or malicious sites.", difficulty: 1 },
            { id: 4, title: "Malware Defense & Sandboxing", short: "Analyze and neutralize malicious software payloads and logic.", material: "Malware includes trojans, spyware, and ransomware. We use strict sandboxing and signature detection tools to analyze behavior safely without affecting data.", difficulty: 1 },
            { id: 5, title: "Web Application Security", short: "Understand injection vulnerabilities and input sanitization techniques.", material: "Web apps require protection against SQL injection and cross-site scripting. Strong session management and input data validation are key mitigation practices.", difficulty: 1 }
        ];

        const questions = {
            1: {
                id: "m1q1",
                topic: "Network Security & Defense",
                text: "Which protocol secures information against eavesdropping when using an unsecure network?",
                options: ["A) Telnet", "B) HTTP", "C) HTTPS", "D) FTP"],
                correctIndex: 2
            },
            2: {
                id: "m2q1",
                topic: "Cryptography & Hashing",
                text: "Which of the following hashing techniques is most effective for slowing down brute-force attacks on credentials?",
                options: ["A) Plain Text", "B) Simple MD5", "C) Bcrypt Hashing", "D) Base64"],
                correctIndex: 2
            },
            3: {
                id: "m3q1",
                topic: "Phishing & Social Engineering",
                text: "What deceptive technique involves sending fraudulent messages designed to trick a person into revealing sensitive info?",
                options: ["A) DNS Spoofing", "B) Phishing", "C) Sandboxing", "D) SQL Injection"],
                correctIndex: 1
            },
            4: {
                id: "m4q1",
                topic: "Malware Defense & Sandboxing",
                text: "What safety precaution allows a security researcher to analyze suspicious files without harming the host system?",
                options: ["A) Plaintext analysis", "B) Sandboxing", "C) Clear Cookies", "D) Port scanning"],
                correctIndex: 1
            },
            5: {
                id: "m5q1",
                topic: "Web Application Security",
                text: "Which vulnerability occurs when user-supplied data is inserted directly into a database query?",
                options: ["A) XSS", "B) SQL Injection", "C) Phishing", "D) Brute force"],
                correctIndex: 1
            }
        };

        window.onload = () => {
            populateModulesGrid();
            switchView('login-view');
        };

        function populateModulesGrid() {
            const grid = document.getElementById('modules-grid');
            grid.innerHTML = '';
            modules.forEach(mod => {
                const card = document.createElement('div');
                card.className = 'card';
                card.onclick = () => startModule(mod.id);
                card.innerHTML = `
                    <h3 style="color: #4f46e5; margin: 0 0 6px 0;">Module ${mod.id}</h3>
                    <p style="font-weight: 600; font-size: 0.95rem; color: #1e293b; margin-bottom: 16px;">${mod.title}</p>
                    <p style="font-size: 0.8rem; color: #64748b; margin-bottom: 24px;">${mod.short}</p>
                    <span style="background: #e0e7ff; color: #4338ca; padding: 4px 12px; border-radius: 4px; font-size: 0.75rem;">Start Assessment &rarr;</span>
                `;
                grid.appendChild(card);
            });
        }

        function switchView(viewId) {
            if (!currentUser && viewId !== 'login-view' && viewId !== 'register-view' && viewId !== 'forgot-view' && viewId !== 'reset-view') {
                viewId = 'login-view';
            }

            ['login-view', 'register-view', 'forgot-view', 'reset-view', 'dashboard-view', 'modules-view', 'study-view', 'assessment-view', 'leaderboard-view', 'profile-view'].forEach(v => {
                document.getElementById(v).classList.add('hidden');
            });

            document.getElementById(viewId).classList.remove('hidden');
            document.getElementById('feedback').classList.add('hidden');

            const sidebar = document.getElementById('sidebar-nav');
            if (currentUser) {
                sidebar.classList.remove('hidden');
                sidebar.classList.add('flex');
                updateDashboard();
            } else {
                sidebar.classList.add('hidden');
                sidebar.classList.remove('flex');
            }
        }

        function showFeedback(type, message) {
            const fb = document.getElementById('feedback');
            fb.classList.remove('hidden');
            if (type === 'success') {
                fb.className = "alert alert-success";
            } else {
                fb.className = "alert alert-danger";
            }
            fb.innerHTML = message;
        }

        function handleLogin(event) {
            event.preventDefault();
            const emailInput = document.getElementById('login-email').value.trim();
            const passwordInput = document.getElementById('login-password').value;

            if (!localDatabase[emailInput]) {
                showFeedback('error', "No account found with this email. Please check your spelling or register.");
                return;
            }

            if (localDatabase[emailInput].password !== passwordInput) {
                showFeedback('error', "Incorrect password. Please try again.");
                return;
            }

            currentUser = emailInput;
            document.getElementById('user-display').textContent = localDatabase[emailInput].username;
            
            // Reset inputs
            document.getElementById('login-email').value = "";
            document.getElementById('login-password').value = "";

            switchView('dashboard-view');
        }

        function handleRegister(event) {
            event.preventDefault();
            const usernameInput = document.getElementById('reg-username').value.trim();
            const emailInput = document.getElementById('reg-email').value.trim();
            const passwordInput = document.getElementById('reg-password').value;

            if (localDatabase[emailInput]) {
                showFeedback('error', "An account with this email address already exists.");
                return;
            }

            localDatabase[emailInput] = { 
                username: usernameInput, 
                password: passwordInput, 
                xp: 0,
                streak: 1,
                badges: [],
                level: 1,
                passedModules: [],
                attempts: 0
            };

            showFeedback('success', "Account registered successfully. Redirecting to sign in...");
            
            document.getElementById('reg-username').value = "";
            document.getElementById('reg-email').value = "";
            document.getElementById('reg-password').value = "";
            document.getElementById('reg-submit-btn').disabled = true;
            document.getElementById('reg-submit-btn').style.opacity = "0.6";
            
            setTimeout(() => switchView('login-view'), 2000);
        }

        function handleForgotPassword(event) {
            event.preventDefault();
            const email = document.getElementById('forgot-email').value.trim();
            if (!localDatabase[email]) {
                showFeedback('error', "Email address not found in the database.");
                return;
            }
            // Actual email delivery simulation using alert as specified by user correction requirements
            alert(`[System Email Delivery] A password reset link has been sent to ${email}`);
            document.getElementById('forgot-email').value = '';
            switchView('reset-view');
        }

        function handleResetPassword(event) {
            event.preventDefault();
            const newPass = document.getElementById('reset-password').value;
            // Find current resetting user email or prompt (we use the last entered)
            const email = document.getElementById('forgot-email').value || Object.keys(localDatabase)[0];
            if (localDatabase[email]) {
                localDatabase[email].password = newPass;
                showFeedback('success', "Password successfully updated. Please sign in.");
                document.getElementById('reset-password').value = '';
                setTimeout(() => switchView('login-view'), 2000);
            }
        }

        function logout() {
            currentUser = "";
            switchView('login-view');
        }

        function updateDashboard() {
            const userObj = localDatabase[currentUser];
            if (!userObj) return;

            // Calculate level
            let levelText = "Level 1 Novice";
            if (userObj.xp >= 1000) levelText = "Level 3 Master";
            else if (userObj.xp >= 500) levelText = "Level 2 Analyst";

            document.getElementById('xp-display').textContent = userObj.xp;
            document.getElementById('level-title').textContent = levelText;
            document.getElementById('user-display').textContent = userObj.username;
            document.getElementById('streak-display').textContent = `${userObj.streak || 1} Days`;
            document.getElementById('badge-display').textContent = (userObj.badges || []).length;

            // Profile view update
            document.getElementById('profile-username').textContent = userObj.username;
            document.getElementById('profile-email').textContent = currentUser;
            document.getElementById('profile-level').textContent = levelText;
            document.getElementById('profile-xp').textContent = userObj.xp;
            document.getElementById('profile-streak').textContent = `${userObj.streak || 1} days`;
            
            let badgesHtml = userObj.badges.map(b => `<span class="badge-success">${b}</span>`).join(" ");
            document.getElementById('profile-badges').innerHTML = badgesHtml || 'None';

            populateLeaderboard();
        }

        function populateLeaderboard() {
            const boardBody = document.getElementById('leaderboard-body');
            let boardData = [
                { rank: 1, name: "SecOps_Master", xp: 4850 },
                { rank: 2, name: "Cipher_33", xp: 4120 },
                { rank: 3, name: "CyberUser_77", xp: 1250 },
                { rank: 4, name: "HackAnalyzer", xp: 950 },
                { rank: 5, name: "ShieldAdmin", xp: 600 }
            ];

            const userObj = localDatabase[currentUser];
            boardData.push({ rank: 6, name: userObj.username + " (You)", xp: userObj.xp });
            boardData.sort((a,b) => b.xp - a.xp);

            let html = '';
            boardData.forEach((item, index) => {
                let activeStyle = item.name.includes("You") ? "background: #e0e7ff4d;" : "";
                html += `<tr style="${activeStyle}">
                    <td><strong>#${index + 1}</strong></td>
                    <td>${item.name}</td>
                    <td>${item.xp} XP</td>
                </tr>`;
            });
            boardBody.innerHTML = html;
        }

        function startModule(moduleId) {
            selectedModule = moduleId;
            switchView('study-view');
            const title = document.getElementById('study-title');
            const content = document.getElementById('study-content');
            
            const mod = modules.find(m => m.id === moduleId);
            if (mod) {
                title.textContent = `Module ${mod.id}: ${mod.title}`;
                content.textContent = mod.material;
            }
        }

        function enterAssessment() {
            switchView('assessment-view');
            loadQuestion();
        }

        function loadQuestion() {
            startTime = Date.now();
            const q = questions[selectedModule] || questions[1];
            document.getElementById('difficulty-badge').textContent = `Difficulty: Level ${currentDifficulty}`;
            document.getElementById('question').textContent = q.text;

            const container = document.getElementById('options-container');
            container.innerHTML = "";

            q.options.forEach((opt, idx) => {
                const btn = document.createElement('button');
                btn.style.padding = "14px";
                btn.style.border = "1px solid #cbd5e1";
                btn.style.borderRadius = "8px";
                btn.style.textAlign = "left";
                btn.style.backgroundColor = "white";
                btn.style.cursor = "pointer";
                btn.style.fontSize = "0.95rem";
                btn.style.transition = "all 0.2s";
                
                btn.onmouseover = function() {
                    this.style.borderColor = "#4f46e5";
                    this.style.backgroundColor = "#e0e7ff4d";
                };
                btn.onmouseout = function() {
                    this.style.borderColor = "#cbd5e1";
                    this.style.backgroundColor = "white";
                };
                
                btn.textContent = opt;
                btn.onclick = () => checkAnswer(idx, q);
                container.appendChild(btn);
            });
            
            document.getElementById("chat-output").textContent = "System: Hello! I am your AI Mentor. I'm ready to help you on this module.";
        }

        function askAIMentor() {
            const inputVal = document.getElementById('chat-input').value.trim();
            const out = document.getElementById('chat-output');
            
            if (!inputVal) return;
            
            let reply = "Mentor: I understand. Let's think about this. Network defenses use HTTPS to prevent data from being intercepted, and encryption helps secure data transit!";
            if (selectedModule === 2) {
                reply = "Mentor: For hashing, Bcrypt uses an intentionally slower algorithm to keep brute-force procedures in check.";
            } else if (selectedModule === 3) {
                reply = "Mentor: Look out for urgent links and requests to authenticate, as they are hallmarks of phishing.";
            } else if (selectedModule === 4) {
                reply = "Mentor: Use sandboxing to isolate threats before executing signature or behavioral detection.";
            } else if (selectedModule === 5) {
                reply = "Mentor: SQL injections alter data queries because user inputs aren't sanitized before running.";
            }

            out.textContent = `User: ${inputVal}\nAI Mentor: ${reply}`;
            document.getElementById('chat-input').value = "";
        }

        function checkAnswer(idx, q) {
            const isCorrect = idx === q.correctIndex;
            const userObj = localDatabase[currentUser];

            if (isCorrect) {
                let xpGain = 140;
                userObj.xp += xpGain;
                if (!userObj.passedModules.includes(selectedModule)) {
                    userObj.passedModules.push(selectedModule);
                }
                
                // Medals check
                let badgeName = "Bronze Certification";
                if (userObj.passedModules.length === 2) badgeName = "Silver Certification";
                if (userObj.passedModules.length >= 3) badgeName = "Gold Certification";

                if (!userObj.badges.includes(badgeName)) {
                    userObj.badges.push(badgeName);
                }

                showFeedback('success', `<strong>Result: Correct!</strong> +${xpGain} XP! Your analyst metrics and level have grown.`);
            } else {
                showFeedback('error', `<strong>Result: Incorrect.</strong> Review the material to speed up your response times and accuracy.`);
            }

            currentDifficulty = 2;
            
            setTimeout(() => {
                switchView('modules-view');
            }, 6500);
        }

        function validatePassword(pass) {
            const rules = [
                { id: "rule-length", valid: pass.length >= 8 },
                { id: "rule-upper", valid: /[A-Z]/.test(pass) },
                { id: "rule-lower", valid: /[a-z]/.test(pass) },
                { id: "rule-number", valid: /[0-9]/.test(pass) },
                { id: "rule-symbol", valid: /[^A-Za-z0-9]/.test(pass) }
            ];
            let allValid = true;
            rules.forEach(r => {
                const el = document.getElementById(r.id);
                if (r.valid) {
                    el.style.color = "#059669";
                    el.innerHTML = `<i class="fas fa-circle-check"></i> ${el.textContent.trim().split(" ").slice(1).join(" ")}`;
                } else {
                    el.style.color = "#ef4444";
                    el.innerHTML = `<i class="fas fa-circle-xmark"></i> ${el.textContent.trim().split(" ").slice(1).join(" ")}`;
                    allValid = false;
                }
            });

            const btn = document.getElementById('reg-submit-btn');
            if (allValid) {
                btn.disabled = false;
                btn.style.opacity = "1";
                btn.style.cursor = "pointer";
            } else {
                btn.disabled = true;
                btn.style.opacity = "0.6";
                btn.style.cursor = "not-allowed";
            }
        }
    </script>
</body>
</html>
