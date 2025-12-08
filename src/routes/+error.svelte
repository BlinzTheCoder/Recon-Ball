<script lang="ts">
  import { page } from '$app/stores';
  
  function goBack() {
    window.history.back();
  }
  
  function goHome() {
    window.location.href = '/';
  }
</script>

<svelte:head>
  <title>404 - Page Not Found</title>
</svelte:head>

<div class="container">
  <div class="content">
    <!-- 404 Number with animated accent -->
    <div class="number-container">
      <h1 class="number-bg">404</h1>
      <div class="number-overlay">
        <span class="number-accent">404</span>
      </div>
    </div>

    <!-- Message -->
    <h2 class="title">Page Not Found</h2>
    <p class="description">
      Oops! The page you're looking for seems to have wandered off into the digital void.
    </p>

    <!-- Action Buttons -->
    <div class="buttons">
      <button class="btn-primary" on:click={goBack}>
        <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <path d="M19 12H5M12 19l-7-7 7-7"/>
        </svg>
        Go Back
      </button>
      
      <button class="btn-secondary" on:click={goHome}>
        <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"/>
          <polyline points="9 22 9 12 15 12 15 22"/>
        </svg>
        Home Page
      </button>
    </div>

    <!-- Decorative Elements -->
    <div class="decoration">
      <div class="circle circle-1"></div>
      <div class="circle circle-2"></div>
      <div class="circle circle-3"></div>
    </div>
  </div>
</div>

<style>
  .container {
    min-height: 92vh;
    min-width: 100vw;
    background: linear-gradient(135deg, #f9fafb 0%, #e0f2fe 100%);
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 1rem;
    position: relative;
    overflow: hidden;
    user-select: none;
  }

  .content {
    max-width: 42rem;
    width: 100%;
    text-align: center;
    position: relative;
    z-index: 10;
  }

  .number-container {
    position: relative;
    margin-bottom: 2rem;
    height: 12rem;
  }

  .number-bg {
    font-size: 9rem;
    font-weight: bold;
    color: #e5e7eb;
    user-select: none;
    margin: 0;
    line-height: 1;
  }

  .number-overlay {
    position: absolute;
    inset: 0;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .number-accent {
    font-size: 7rem;
    font-weight: bold;
    color: #00994d;
    animation: pulse 2s ease-in-out infinite;
  }

  @keyframes pulse {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.7; }
  }

  .title {
    font-size: 2rem;
    font-weight: bold;
    color: #1f2937;
    margin-bottom: 1rem;
  }

  .description {
    font-size: 1.125rem;
    color: #4b5563;
    margin-bottom: 2rem;
    max-width: 28rem;
    margin-left: auto;
    margin-right: auto;
  }

  .buttons {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    justify-content: center;
    align-items: center;
    margin-bottom: 3rem;
  }

  @media (min-width: 640px) {
    .buttons {
      flex-direction: row;
    }
  }

  button {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    padding: 0.75rem 1.5rem;
    border-radius: 0.5rem;
    font-weight: 500;
    transition: all 0.2s;
    cursor: pointer;
    border: none;
    font-size: 1rem;
  }

  .btn-primary {
    background-color: #00994d;
    color: white;
    box-shadow: 0 10px 15px -3px rgba(0, 148, 217, 0.3);
  }

  .btn-primary:hover {
    transform: scale(1.05);
    box-shadow: 0 20px 25px -5px rgba(0, 148, 217, 0.3);
  }

  .btn-primary:active {
    transform: scale(0.95);
  }

  .btn-secondary {
    background-color: white;
    color: #00994d;
    border: 2px solid #00994d;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
  }

  .btn-secondary:hover {
    transform: scale(1.05);
    box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
  }

  .btn-secondary:active {
    transform: scale(0.95);
  }

  .decoration {
    position: absolute;
    inset: 0;
    pointer-events: none;
    z-index: 1;
  }

  .circle {
    position: absolute;
    border-radius: 100%;
    background: linear-gradient(135deg, rgba(0, 148, 217, 0.1), rgba(0, 148, 217, 0.05));
  }

  .circle-1 {
    width: 20rem;
    height: 20rem;
    top: -5rem;
    right: -5rem;
    animation: float 6s ease-in-out infinite;
  }

  .circle-2 {
    width: 15rem;
    height: 15rem;
    bottom: -3rem;
    left: -3rem;
    animation: float 8s ease-in-out infinite reverse;
  }

  .circle-3 {
    width: 10rem;
    height: 10rem;
    top: 50%;
    left: 10%;
    animation: float 10s ease-in-out infinite;
  }

  @keyframes float {
    0%, 100% {
      transform: translateY(0) rotate(0deg);
    }
    50% {
      transform: translateY(-20px) rotate(5deg);
    }
  }

  @media (max-width: 640px) {
    .number-bg {
      font-size: 6rem;
    }
    
    .number-accent {
      font-size: 5rem;
    }
    
    .title {
      font-size: 1.5rem;
    }
    
    .description {
      font-size: 1rem;
    }
  }
</style>