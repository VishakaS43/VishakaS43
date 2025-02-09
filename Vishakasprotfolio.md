<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Portfolio Form</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      margin: 20px;
      background: #f4f4f9;
    }
    h1 {
      text-align: center;
      color: #4CAF50;
    }
    form {
      max-width: 600px;
      margin: 20px auto;
      padding: 20px;
      background: white;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
      border-radius: 5px;
    }
    label {
      font-weight: bold;
    }
    input, textarea {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    button {
      background: #4CAF50;
      color: white;
      border: none;
      padding: 10px 20px;
      cursor: pointer;
      border-radius: 5px;
    }
    button:hover {
      background: #45a049;
    }
    .portfolio {
      max-width: 600px;
      margin: 20px auto;
      padding: 20px;
      background: #fff;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
      border-radius: 5px;
    }
  </style>
</head>
<body>

<h1>Portfolio Form</h1>
<form id="portfolioForm">
  <label for="name">Name:</label>
  <input type="text" id="name" placeholder="Enter your name" required>
  
  <label for="about">About Me:</label>
  <textarea id="about" placeholder="Write a short bio" rows="4" required></textarea>
  
  <label for="skills">Skills (comma-separated):</label>
  <input type="text" id="skills" placeholder="e.g., Communication, Time Management, Excel" required>
  
  <label for="experience">Experience:</label>
  <textarea id="experience" placeholder="Describe your work experience" rows="4"></textarea>
  
  <label for="email">Email:</label>
  <input type="email" id="email" placeholder="Enter your email" required>
  
  <button type="button" onclick="generatePortfolio()">Generate Portfolio</button>
</form>

<div class="portfolio" id="portfolioOutput" style="display:none;">
  <h2>Portfolio</h2>
  <p><strong>Name:</strong> <span id="outputName"></span></p>
  <p><strong>About Me:</strong> <span id="outputAbout"></span></p>
  <p><strong>Skills:</strong> <span id="outputSkills"></span></p>
  <p><strong>Experience:</strong> <span id="outputExperience"></span></p>
  <p><strong>Email:</strong> <span id="outputEmail"></span></p>
</div>

<script>
  function generatePortfolio() {
    document.getElementById('outputName').innerText = document.getElementById('name').value;
    document.getElementById('outputAbout').innerText = document.getElementById('about').value;
    document.getElementById('outputSkills').innerText = document.getElementById('skills').value;
    document.getElementById('outputExperience').innerText = document.getElementById('experience').value;
    document.getElementById('outputEmail').innerText = document.getElementById('email').value;
    
    document.getElementById('portfolioOutput').style.display = 'block';
  }
</script>

</body>
</html>