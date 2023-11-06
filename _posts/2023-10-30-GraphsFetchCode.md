---
toc: false
comments: false
layout: post
title: Graphs Fetch Code
description: 
type: tangibles
courses: { compsci: {week: 12}}
---



%%html

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Instruments Practice Tracker</title>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
            background-color: white;
        }
        header {
            background-color: #ffb6c1;
            color: #fff;
            padding: 10px;
            text-align: center;
        }
        h1 {
            margin: 0;
        }
        section {
            max-width: 800px;
            margin: 20px auto;
            padding: 20px;
            background-color: white;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.3);
            border-radius: 10px;
            overflow: hidden;
        }
        footer {
            background-color: #333;
            color: #fff;
            text-align: center;
            padding: 10px;
            position: fixed;
            width: 100%;
            bottom: 0;
        }
    </style>
</head>
<body>
    <section>
        <h1>Instruments Practice Tracker</h1>
        <form id="practice-form">
            <label for="practice-time">Practice Time (minutes):</label>
            <input type="number" id="practice-time" required>
            <button type="submit">Save</button>
        </form>
        <canvas id="practice-chart" width="400" height="200"></canvas>
    </section>

    <script>
        const practiceData = {
            labels: [],
            datasets: [
                {
                    label: 'Practice Time (minutes)',
                    data: [],
                    backgroundColor: 'rgba(75, 192, 192, 0.2)',
                    borderColor: 'rgba(75, 192, 192, 1)',
                    borderWidth: 1,
                },
            ],
        };

        const ctx = document.getElementById('practice-chart').getContext('2d');
        const practiceChart = new Chart(ctx, {
            type: 'bar',
            data: practiceData,
            options: {
                scales: {
                    y: {
                        beginAtZero: true,
                    },
                },
            },
        });

        const practiceForm = document.getElementById('practice-form');
        practiceForm.addEventListener('submit', function (e) {
            e.preventDefault();

            const practiceTimeInput = document.getElementById('practice-time');
            const practiceTime = parseInt(practiceTimeInput.value);

            if (!isNaN(practiceTime)) {
                // Add the practice time to the chart data
                const currentDate = new Date().toLocaleDateString();
                practiceData.labels.push(currentDate);
                practiceData.datasets[0].data.push(practiceTime);

                // Update the chart
                practiceChart.update();

                // Clear the input field
                practiceTimeInput.value = '';
            }
        });
    </script>
</body> 
