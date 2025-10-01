<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Sunnydale School</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f5f7fa;
      color: #333;
      line-height: 1.6;
    }
    .container {
      max-width: 900px;
      margin: auto;
      padding: 20px;
    }
    h1 {
      font-size: 32px;
      font-weight: bold;
      color: #1E90FF;
      text-align: center;
      margin-bottom: 10px;
    }
    h1::after {
      content: "";
      display: block;
      width: 60px;
      margin: 10px auto;
      border-bottom: 3px solid #1E90FF;
    }
    h2 {
      font-size: 22px;
      margin-top: 30px;
      color: #2c3e50;
      border-left: 5px solid #1E90FF;
      padding-left: 10px;
    }
    #mission {
      background: #ffffff;
      padding: 15px;
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }
    #upcoming-events {
      background: #ffffff;
      padding: 15px;
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }
    #upcoming-events ul {
      list-style: none;
      padding: 0;
    }
    #upcoming-events li {
      padding: 8px;
      margin-bottom: 8px;
      border-radius: 5px;
    }
    #upcoming-events li span {
      font-weight: bold;
      color: #e74c3c;
    }
    .outdoor {
      background-color: #e6f7f9;
      border: 1px solid #b0e0e6;
    }
    #contact .section {
      background-color: #ffffff;
      padding: 15px;
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }
    #contact a {
      color: #1E90FF;
      text-decoration: none;
    }
    #contact a:hover {
      text-decoration: underline;
    }
    footer {
      text-align: center;
      margin-top: 30px;
      font-size: 14px;
      color: #777;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>UCC School</h1>
    <div id="mission">
      <h2>Mission Statement</h2>
      <p>At Sunnydale School, our mission is to inspire students to achieve their full potential through
     a balanced education that fosters creativity, critical thinking, and community values</p>
    </div>
    <div id="upcoming-events">
      <h2>Upcoming Events</h2>
      <ul>
        <li data-event-type="indoor" title="Event Type: Indoor">
          Science Fair - <span>June 10</span>
        </li>
        <li class="outdoor" data-event-type="outdoor" title="Event Type: Outdoor">
          Art Exhibition - <span>June 15</span>
        </li>
        <li class="outdoor" data-event-type="outdoor" title="Event Type: Outdoor">
          Sports Day - <span>June 20</span>
        </li>
      </ul>
    </div>
    <div id="contact">
      <h2>Contact Us</h2>
      <div class="section">
        <p>Email: <a href="mailto:nherreramarkjan@gmail.com" title="Click to copy email">nherreramarkjan@gmail.com</a></p>
        <p>Phone: <a href="tel:09971435799" title="Click to copy phone">09971435799</a></p>
        <p>Address: 123 Sunny Street, Brightsville</p>
      </div>
    </div>
    <footer>
      &copy; 2025 UCC School |
    </footer>
  </div>
</body>
</html>
