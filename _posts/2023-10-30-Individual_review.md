<!-- ---
toc: false
comments: false
layout: post
title: Individual Review
description: Tri 1 Individual Review
courses: { compsci: { week: 11 } }
type: tangibles
--- -->

<style>
  .bullet-points {
    list-style-type: disc; 
    margin-left: 40px; 
  }
  .bullet-points li {
    margin-bottom: 20px; 
  }
</style>

# Development Journey

---

### Getting data

Objective: Get details on each type of intrument 

<ul class = "bullet-points">
  <li>Approach: Acquire information about different types of insturments</li>
  <li>Challenges: Utilize a custom Python script to gather data</li>
  <li>Problems faced: None</li>
</ul>

---

### Connecting frontend and backend

Objective: Send data from frontend to backend and get data

<ul class = "bullet-points">
  <li>Approach: Used JavaScript to send a request to the API with the GET method</li>
  <li>Challenges: JavaScript code was complicated and took a while to get working</li>
  <li>Problems faced: None</li>
</ul>

---

# Code Snippet

---

These are some code snippets I think show contribution to the code

### HTML

This code snippet I worked on is how the data for the graph is created

<!-- <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Instruments Practice Tracker</title>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style> -->


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


# Github Analytics

### Key Commits:

<ul class = "bullet-points">
  <li>Creating backend code for the graph</li>
  <li>Connecting frontend and backend for the graph</li>
</ul>

### Issues:

<ul class = "bullet-points">
  <li>Connecting Frontend and Backend took a long time </li>
</ul>

---

# Individual Blog

### Snippet from Simulations team teach

```python
Hack: Given initial parameters for a car simulation, including its initial speed, acceleration rate, deceleration rate, maximum speed, and initial distance, write a program to simulate the car’s journey and determine the final speed, distance covered, and time taken before it either covers 1000 meters or slows down to below 5 m/s?
```

```python
initial_speed = 10
acceleration_rate = 2
deceleration_rate = -1
max_speed = 20
initial_distance = 0
target_distance = 1000
min_speed = 5

speed = initial_speed
distance = initial_distance
time = 0

while distance < target_distance and speed >= min_speed:
    time_to_max_speed = (max_speed - speed) / acceleration_rate
    distance_covered_acceleration = speed * time_to_max_speed + 0.5 * acceleration_rate * time_to_max_speed ** 2

    if distance + distance_covered_acceleration >= target_distance:
        time += (-speed + (speed ** 2 + 2 * acceleration_rate * (target_distance - distance)) ** 0.5) / acceleration_rate
        speed = max_speed
        distance = target_distance
    else:
        time += time_to_max_speed
        speed = max_speed
        distance += distance_covered_acceleration

        if distance < target_distance:
            time_to_decelerate = (speed - min_speed) / abs(deceleration_rate)
            distance_covered_deceleration = speed * time_to_decelerate + 0.5 * deceleration_rate * time_to_decelerate ** 2

            if distance + distance_covered_deceleration >= target_distance:
                time += (-speed + (speed ** 2 - 2 * deceleration_rate * (distance - target_distance)) ** 0.5) / abs(deceleration_rate)
                speed = min_speed
                distance = target_distance
            else:
                time += time_to_decelerate
                speed = min_speed
                distance += distance_covered_deceleration

print(f"Final Speed: {speed} m/s")
print(f"Distance Covered: {distance} meters")
print(f"Time Taken: {time} seconds")
```

# Trimester One Reflections

### Memories and Learning:

<ul class = "bullet-points">
  <li> Agile development process</li>
  <li> Learning how to work in groups to create a large project</li>
  <li> Working on and debugging Code especially Python and JavaScript</li>
  <li> Helping out other groups with code issues</li>
</ul>

### Positive Accomplishments

<ul class = "bullet-points">
  <li> Working on backend and frontend development to create a full stack web project</li>
  <li> Implementing the Flask framework for our website</li>
  <li> Learning and using new tools and programs</li>
</ul>

### Opportunites for Growth and things I hope to learn in Tri 2

<ul class = "bullet-points">
  <li> Debugging code. Espescially with breakpoints</li>
  <li> Deepen CompSci knowledge with backend data</li>
  <li> More about API's and creating full stack web apps</li>
  <li> Become more fluent and comfortable with the CLI</li>
</ul>