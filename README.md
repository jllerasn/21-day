<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>21-Day Glow Reset Plan</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #f5f3f0 0%, #e8e4df 100%);
            min-height: 100vh;
            padding: 40px 20px;
            color: #5a5a5a;
        }
        
        .container {
            max-width: 800px;
            margin: 0 auto;
            background: #fefcfa;
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
            overflow: hidden;
            position: relative;
        }
        
        .container::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 8px;
            background: linear-gradient(90deg, #7ba05b, #c4755b, #7ba05b);
            border-radius: 20px 20px 0 0;
        }
        
        .header {
            background: linear-gradient(135deg, #7ba05b 0%, #8fb069 100%);
            padding: 40px 30px;
            text-align: center;
            color: white;
            position: relative;
            overflow: hidden;
        }
        
        .header::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 1px, transparent 1px);
            background-size: 30px 30px;
            animation: float 20s linear infinite;
        }
        
        @keyframes float {
            0% { transform: translate(0, 0) rotate(0deg); }
            100% { transform: translate(-30px, -30px) rotate(360deg); }
        }
        
        .title {
            font-size: 2.5em;
            font-weight: 600;
            margin-bottom: 10px;
            position: relative;
            z-index: 1;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
        }
        
        .subtitle {
            font-size: 1.1em;
            font-weight: 300;
            opacity: 0.9;
            position: relative;
            z-index: 1;
        }
        
        .chart-container {
            padding: 40px 30px;
            background: #fefcfa;
        }
        
        .intro-text {
            text-align: center;
            margin-bottom: 30px;
            font-size: 1.1em;
            color: #6b5b5b;
            line-height: 1.6;
        }
        
        .habit-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }
        
        .habit-table th {
            background: linear-gradient(135deg, #7ba05b 0%, #8fb069 100%);
            color: white;
            padding: 20px 15px;
            text-align: left;
            font-weight: 500;
            font-size: 1.1em;
            position: relative;
        }
        
        .habit-table th:first-child {
            width: 10%;
            text-align: center;
        }
        
        .habit-table th:nth-child(2) {
            width: 50%;
        }
        
        .habit-table th:nth-child(3) {
            width: 20%;
            text-align: center;
        }
        
        .habit-table th:nth-child(4) {
            width: 20%;
            text-align: center;
        }
        
        .habit-table td {
            padding: 18px 15px;
            border-bottom: 1px solid #e8e4df;
            vertical-align: middle;
            background: white;
        }
        
        .habit-table tr:nth-child(even) td {
            background: #faf9f7;
        }
        
        .habit-table tr:hover td {
            background: #f0f4ec;
            transform: translateY(-2px);
            transition: all 0.3s ease;
        }
        
        .day-number {
            font-weight: 600;
            color: #7ba05b;
            font-size: 1.2em;
            text-align: center;
        }
        
        .habit-text {
            font-weight: 400;
            color: #5a5a5a;
            line-height: 1.4;
            position: relative;
            padding-left: 25px;
        }
        
        .habit-text::before {
            content: '✨';
            position: absolute;
            left: 0;
            top: 0;
            color: #c4755b;
            font-size: 1.1em;
        }
        
        .checkbox-cell {
            text-align: center;
            padding: 15px;
        }
        
        .custom-checkbox {
            width: 25px;
            height: 25px;
            border: 2px solid #c4755b;
            border-radius: 6px;
            display: inline-block;
            cursor: pointer;
            position: relative;
            transition: all 0.3s ease;
        }
        
        .custom-checkbox:hover {
            border-color: #7ba05b;
            transform: scale(1.1);
        }
        
        .custom-checkbox.checked {
            background: linear-gradient(135deg, #7ba05b, #8fb069);
            border-color: #7ba05b;
        }
        
        .custom-checkbox.checked::after {
            content: '✓';
            position: absolute;
            color: white;
            font-weight: bold;
            font-size: 16px;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
        }
        
        .feeling-input {
            width: 100%;
            padding: 8px 12px;
            border: 2px solid #e8e4df;
            border-radius: 8px;
            font-family: 'Poppins', sans-serif;
            font-size: 0.9em;
            color: #5a5a5a;
            background: white;
            transition: border-color 0.3s ease;
        }
        
        .feeling-input:focus {
            outline: none;
            border-color: #7ba05b;
            box-shadow: 0 0 0 3px rgba(123, 160, 91, 0.1);
        }
        
        .footer {
            background: linear-gradient(135deg, #c4755b 0%, #d4865b 100%);
            padding: 30px;
            text-align: center;
            color: white;
        }
        
        .footer-text {
            font-size: 1.1em;
            font-weight: 300;
            margin-bottom: 10px;
        }
        
        .footer-quote {
            font-style: italic;
            font-size: 0.95em;
            opacity: 0.9;
        }
        
        @media (max-width: 768px) {
            .container {
                margin: 10px;
            }
            
            .title {
                font-size: 2em;
            }
            
            .chart-container {
                padding: 20px 15px;
            }
            
            .habit-table th,
            .habit-table td {
                padding: 12px 8px;
                font-size: 0.9em;
            }
            
            .habit-text {
                padding-left: 20px;
            }
            
            .feeling-input {
                font-size: 0.8em;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1 class="title">21-DAY GLOW RESET PLAN</h1>
            <p class="subtitle">Your Journey to Radiant Wellness</p>
        </div>
        
        <div class="chart-container">
            <p class="intro-text">
                Transform your daily routine with these mindful habits designed to enhance your natural glow from within. 
                Check off each habit as you complete it and reflect on how it made you feel.
            </p>
            
            <table class="habit-table">
                <thead>
                    <tr>
                        <th>Day</th>
                        <th>Glow Habit of the Day</th>
                        <th>Did You Do It?</th>
                        <th>How Did You Feel?</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td class="day-number">1</td>
                        <td class="habit-text">Drink 8 glasses of water + morning collagen</td>
                        <td class="checkbox-cell"><div class="custom-checkbox" onclick="toggleCheck(this)"></div></td>
                        <td><input type="text" class="feeling-input" placeholder="Energized, refreshed..."></td>
                    </tr>
                    <tr>
                        <td class="day-number">2</td>
                        <td class="habit-text">20-minute outdoor walk in nature</td>
                        <td class="checkbox-cell"><div class="custom-checkbox" onclick="toggleCheck(this)"></div></td>
                        <td><input type="text" class="feeling-input" placeholder="Peaceful, grounded..."></td>
                    </tr>
                    <tr>
                        <td class="day-number">3</td>
                        <td class="habit-text">No caffeine after 2pm</td>
                        <td class="checkbox-cell"><div class="custom-checkbox" onclick="toggleCheck(this)"></div></td>
                        <td><input type="text" class="feeling-input" placeholder="Calm, well-rested..."></td>
                    </tr>
                    <tr>
                        <td class="day-number">4</td>
                        <td class="habit-text">Write 3 things you're grateful for</td>
                        <td class="checkbox-cell"><div class="custom-checkbox" onclick="toggleCheck(this)"></div></td>
                        <td><input type="text" class="feeling-input" placeholder="Grateful, positive..."></td>
                    </tr>
                    <tr>
                        <td class="day-number">5</td>
                        <td class="habit-text">10-minute morning meditation</td>
                        <td class="checkbox-cell"><div class="custom-checkbox" onclick="toggleCheck(this)"></div></td>
                        <td><input type="text" class="feeling-input" placeholder="Centered, focused..."></td>
                    </tr>
                    <tr>
                        <td class="day-number">6</td>
                        <td class="habit-text">Eat a rainbow of colorful vegetables</td>
                        <td class="checkbox-cell"><div class="custom-checkbox" onclick="toggleCheck(this)"></div></td>
                        <td><input type="text" class="feeling-input" placeholder="Nourished, vibrant..."></td>
                    </tr>
                    <tr>
                        <td class="day-number">7</td>
                        <td class="habit-text">Screen-free time 1 hour before bed</td>
                        <td class="checkbox-cell"><div class="custom-checkbox" onclick="toggleCheck(this)"></div></td>
                        <td><input type="text" class="feeling-input" placeholder="Relaxed, sleepy..."></td>
                    </tr>
                    <tr>
                        <td class="day-number">8</td>
                        <td class="habit-text">Practice deep breathing exercises</td>
                        <td class="checkbox-cell"><div class="custom-checkbox" onclick="toggleCheck(this)"></div></td>
                        <td><input type="text" class="feeling-input" placeholder="Calm, present..."></td>
                    </tr>
                    <tr>
                        <td class="day-number">9</td>
                        <td class="habit-text">Gentle yoga or stretching session</td>
                        <td class="checkbox-cell"><div class="custom-checkbox" onclick="toggleCheck(this)"></div></td>
                        <td><input type="text" class="feeling-input" placeholder="Flexible, strong..."></td>
                    </tr>
                    <tr>
                        <td class="day-number">10</td>
                        <td class="habit-text">Apply SPF and moisturize skin</td>
                        <td class="checkbox-cell"><div class="custom-checkbox" onclick="toggleCheck(this)"></div></td>
                        <td><input type="text" class="feeling-input" placeholder="Protected, glowing..."></td>
                    </tr>
                    <tr>
                        <td class="day-number">11</td>
                        <td class="habit-text">Read for 30 minutes instead of scrolling</td>
                        <td class="checkbox-cell"><div class="custom-checkbox" onclick="toggleCheck(this)"></div></td>
                        <td><input type="text" class="feeling-input" placeholder="Inspired, focused..."></td>
                    </tr>
                    <tr>
                        <td class="day-number">12</td>
                        <td class="habit-text">Prepare and eat a nourishing breakfast</td>
                        <td class="checkbox-cell"><div class="custom-checkbox" onclick="toggleCheck(this)"></div></td>
                        <td><input type="text" class="feeling-input" placeholder="Satisfied, energized..."></td>
                    </tr>
                    <tr>
                        <td class="day-number">13</td>
                        <td class="habit-text">Take 5 deep breaths before meals</td>
                        <td class="checkbox-cell"><div class="custom-checkbox" onclick="toggleCheck(this)"></div></td>
                        <td><input type="text" class="feeling-input" placeholder="Mindful, present..."></td>
                    </tr>
                    <tr>
                        <td class="day-number">14</td>
                        <td class="habit-text">Spend time in natural sunlight</td>
                        <td class="checkbox-cell"><div class="custom-checkbox" onclick="toggleCheck(this)"></div></td>
                        <td><input type="text" class="feeling-input" placeholder="Warm, energized..."></td>
                    </tr>
                    <tr>
                        <td class="day-number">15</td>
                        <td class="habit-text">Practice positive self-talk</td>
                        <td class="checkbox-cell"><div class="custom-checkbox" onclick="toggleCheck(this)"></div></td>
                        <td><input type="text" class="feeling-input" placeholder="Confident, loved..."></td>
                    </tr>
                    <tr>
                        <td class="day-number">16</td>
                        <td class="habit-text">Dry brush skin before showering</td>
                        <td class="checkbox-cell"><div class="custom-checkbox" onclick="toggleCheck(this)"></div></td>
                        <td><input type="text" class="feeling-input" placeholder="Smooth, invigorated..."></td>
                    </tr>
                    <tr>
                        <td class="day-number">17</td>
                        <td class="habit-text">Listen to uplifting music or podcast</td>
                        <td class="checkbox-cell"><div class="custom-checkbox" onclick="toggleCheck(this)"></div></td>
                        <td><input type="text" class="feeling-input" placeholder="Inspired, joyful..."></td>
                    </tr>
                    <tr>
                        <td class="day-number">18</td>
                        <td class="habit-text">Declutter and organize one small space</td>
                        <td class="checkbox-cell"><div class="custom-checkbox" onclick="toggleCheck(this)"></div></td>
                        <td><input type="text" class="feeling-input" placeholder="Clear, accomplished..."></td>
                    </tr>
                    <tr>
                        <td class="day-number">19</td>
                        <td class="habit-text">Connect with a friend or loved one</td>
                        <td class="checkbox-cell"><div class="custom-checkbox" onclick="toggleCheck(this)"></div></td>
                        <td><input type="text" class="feeling-input" placeholder="Connected, loved..."></td>
                    </tr>
                    <tr>
                        <td class="day-number">20</td>
                        <td class="habit-text">Practice mindful eating - no distractions</td>
                        <td class="checkbox-cell"><div class="custom-checkbox" onclick="toggleCheck(this)"></div></td>
                        <td><input type="text" class="feeling-input" placeholder="Satisfied, mindful..."></td>
                    </tr>
                    <tr>
                        <td class="day-number">21</td>
                        <td class="habit-text">Celebrate your transformation journey</td>
                        <td class="checkbox-cell"><div class="custom-checkbox" onclick="toggleCheck(this)"></div></td>
                        <td><input type="text" class="feeling-input" placeholder="Proud, accomplished..."></td>
                    </tr>
                </tbody>
            </table>
        </div>
        
        <div class="footer">
            <p class="footer-text">Your glow comes from within - nurture it daily</p>
            <p class="footer-quote">"Small daily improvements are the key to staggering long-term results"</p>
        </div>
    </div>
    
    <script>
        function toggleCheck(element) {
            element.classList.toggle('checked');
        }
        
        // Add some interactive touches
        document.querySelectorAll('.feeling-input').forEach(input => {
            input.addEventListener('focus', function() {
                this.parentElement.parentElement.style.background = '#f0f4ec';
            });
            
            input.addEventListener('blur', function() {
                this.parentElement.parentElement.style.background = '';
            });
        });
    </script>
</body>
</html>
