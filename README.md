<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>My Secure CodeShare</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  
  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Fira+Code&display=swap" rel="stylesheet">

  <!-- CodeMirror CSS -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.12/codemirror.min.css">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.12/theme/dracula.min.css">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html, body {
      height: 100%;
      background-color: #000000; /* Fully black background */
      color: #00FF00; /* Green text color like Python code share */
      font-family: 'Fira Code', monospace;
      display: flex;
      flex-direction: column;
    }

    header {
      background-color: #1f1f2e;
      padding: 20px 30px;
      text-align: center;
      font-size: 1.8rem;
      font-weight: bold;
      box-shadow: 0 2px 10px rgba(0,0,0,0.5);
      color: #fff;
    }

    #editor {
      flex-grow: 1;
      margin: 0 20px;
      border: 2px solid #333;
      border-radius: 8px;
      overflow: hidden;
      height: calc(100vh - 140px); /* Makes the editor take up most of the screen height */
    }

    .CodeMirror {
      height: 100% !important;
      width: 100% !important;
    }

    .actions {
      display: none; /* Hide the actions buttons */
    }

    @media (max-width: 600px) {
      .actions {
        flex-direction: column;
        gap: 10px;
      }
    }
  </style>
</head>
<body>

  <header>My CodeShare</header>

  <div id="editor"></div>

  <!-- CodeMirror Scripts -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.12/codemirror.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.12/mode/python/python.min.js"></script>
  <script>
    const editor = CodeMirror(document.getElementById("editor"), {
      mode: "python",  // Change to Python mode for CodeShare-like syntax highlighting
      theme: "dracula",
      lineNumbers: true,
      lineWrapping: true,
      value: "# Start typing your Python code here...\n"
    });
  </script>
</body>
</html>
