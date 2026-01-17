<style>
  /* On force le conteneur à sortir du cadre du thème et à se centrer réellement */
  .img-wrapper {
    width: 90vw !important; /* Largeur de 90% de l'écran */
    max-width: 1400px !important;
    
    /* LA CORRECTION : On centre par rapport à la fenêtre (viewport) */
    position: relative;
    left: 50%;
    transform: translateX(-50%);
    
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 40px 0 !important;
  }

  .img-wrapper img {
    display: block;
    width: 100% !important;
    height: auto !important;
    margin-bottom: 40px;
    border-radius: 12px;
    box-shadow: 0 10px 40px rgba(0, 0, 0, 0.5);
    transition: all 0.4s ease-in-out;
  }

  .img-wrapper img:hover {
    transform: translateY(-5px);
    box-shadow: 0 20px 50px rgba(0, 217, 255, 0.3);
    filter: brightness(1.05);
  }

  /* Indispensable pour éviter que la page bouge sur les côtés */
  html, body {
    overflow-x: hidden;
  }
</style>

<div class="img-wrapper">
  <img src="https://github.com/user-attachments/assets/5b6bcc1a-6f76-46fd-88fb-34b43fbaa0e5" />
  <img src="https://github.com/user-attachments/assets/8d54004b-3bcb-4f57-b5a0-310241f73b75" />
  <img src="https://github.com/user-attachments/assets/972ed0ac-d641-4f54-bd52-c4f9b4380774" />
  <img src="https://github.com/user-attachments/assets/39848e20-ce8b-49cb-ab3a-5679691abe8c" />
</div>
