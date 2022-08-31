<script></script>

<div class="main"> 
  <h1>Guillem Sardà Parreu</h1>
  <span class="animated">
    <h2>Coming soon...</h2>
  </span>
</div>

<style>
  .main {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    height: 100vh;
    width: 100vw;
  }
  h1 {
    font-family: 'Courier New', Courier, monospace;
    transition: 1.5s ease;
    justify-self: center;
  }
  h1:hover {
    color: #ff3e00;
  }
  h2 {
    font-family: 'Courier New', Courier, monospace;
  }
  .animated {
    width: 100vw;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    animation: bounceIn 5s;
    animation-iteration-count: infinite;
  }

  @keyframes bounceIn {
   0% { 
    opacity: 0; 
    transform: translateX(-10vw);
   }
   10% {
    opacity: 0.5;
   }
   35% {
    /* transform: translateX(5vw); */
    color: #ff3e00;
    opacity: 1;
   }
   70% { 
    opacity: 0;
    transform: translateX(10vw);
   }
   100% {
    opacity: 0;
   }
} 
</style>