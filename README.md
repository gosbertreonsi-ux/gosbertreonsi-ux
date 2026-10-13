<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>How Coding FEELS</title>
  <style>
    @property --angle {
      syntax: "<angle>";
      initial-value: 0deg;
      inherits: false;
    }
    body {
      margin: 0;
      padding: 24px;
      background: #0d1117; /* dark, so the white arc is visible */
      color: #e6edf3;
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
    }
  .row {
      display: flex;
      flex-direction: row;
      align-items: center;
      gap: 16px;
    }
   .loader-border {
      width: 30%;
      padding: 4px;                 /* border thickness */
      border-radius: 20px;          /* rounding */
      background: conic-gradient(
        from var(--angle),
        transparent 0deg,
        transparent 240deg,
        rgba(255, 255, 255, 0.2) 280deg,
        #fff 360deg                 /* bright head of the arc */
      );
      animation: spin 1.5s linear infinite;
    }
    .loader-border img {
      display: block;
      width: 100%;
      border-radius: 16px;          /* container radius minus padding */
    }
    @keyframes spin {
      to { --angle: 360deg; }
    }
  </style>
</head>
<body>
  <div class="row">
    <div class="loader-border">
      <img src="image.gif" alt="" />
    </div>
    <p>How Coding FEELS 🎭</p>
  </div>
</body>
</html>
