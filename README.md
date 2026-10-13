<div style="display: flex; flex-direction: row; align-items: center; gap: 16px;">
  <div class="loader-border">
    <img src="image.gif" alt="" />
  </div>
  <p>How Coding FEELS 🎭</p>
</div>

<style>
  @property --angle {
    syntax: "<angle>";
    initial-value: 0deg;
    inherits: false;
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
