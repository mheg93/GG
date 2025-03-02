# GG
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Animated Sphinx Saying Sorry</title>
  <style>
    /* Reset default margins/padding */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    
    /* Fullscreen container with a light blue background */
    body, html {
      height: 100%;
      background: #87CEEB;
      overflow: hidden;
      font-family: Arial, sans-serif;
    }
    
    .container {
      position: relative;
      width: 100%;
      height: 100%;
    }
    
    /* The sphinx container is centered at the bottom and gently floats */
    .sphinx {
      position: absolute;
      left: 50%;
      bottom: 20px;
      transform: translateX(-50%);
      animation: float 3s ease-in-out infinite;
    }
    
    /* The sphinx head: a simple circle */
    .sphinx-head {
      position: relative;
      width: 80px;
      height: 80px;
      border-radius: 50%;
      background: #f1c27d;
      border: 3px solid #333;
      margin: 0 auto;
      z-index: 2;
    }
    
    /* Optionally add eyes (using pseudo-elements) */
    .sphinx-head::before,
    .sphinx-head::after {
      content: "";
      position: absolute;
      top: 30%;
      width: 10px;
      height: 10px;
      background: #333;
      border-radius: 50%;
    }
    .sphinx-head::before {
      left: 20px;
    }
    .sphinx-head::after {
      right: 20px;
    }
    
    /* The sphinx body: a rounded rectangle */
    .sphinx-body {
      position: relative;
      width: 120px;
      height: 180px;
      background: #f4a460;
      border: 3px solid #333;
      border-radius: 20px;
      margin: 0 auto;
      top: -20px;
      z-index: 1;
    }
    
    /* The sign is positioned to the right of the body and swings */
    .sphinx-sign {
      position: absolute;
      top: 50px;
      right: -110px;
      width: 100px;
      height: 50px;
      background: #fff;
      border: 3px solid #333;
      border-radius: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: bold;
      color: #333;
      transform-origin: left center;
      animation: swing 2s ease-in-out infinite;
    }
    
    /* Keyframe for the sign swing animation */
    @keyframes swing {
      0%   { transform: rotate(0deg); }
      50%  { transform: rotate(15deg); }
      100% { transform: rotate(0deg); }
    }
    
    /* Keyframe for the gentle floating animation of the sphinx */
    @keyframes float {
      0%   { transform: translateX(-50%) translateY(0px); }
      50%  { transform: translateX(-50%) translateY(-20px); }
      100% { transform: translateX(-50%) translateY(0px); }
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="sphinx">
      <div class="sphinx-head"></div>
      <div class="sphinx-body"></div>
      <div class="sphinx-sign">Sorry</div>
    </div>
  </div>
  
  <!-- JavaScript section (for additional interactivity if needed) -->
  <script>
    // For now the animation is driven entirely by CSS.
    // This JavaScript code simply logs a message to the console.
    console.log("Animated Sphinx is ready!");
  </script>
</body>
</html>
