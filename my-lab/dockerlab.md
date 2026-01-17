<style>
  /* On force le container à être large (92% de l'écran) */
  .img-wrapper {
    width: 92vw !important; 
    max-width: 1500px !important; 
    /* Cette formule magique centre l'image parfaitement avec des petits bords */
    margin-left: calc(50% - 46vw) !important; 
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 10px 0;
  }

  .img-wrapper img {
    display: block;
    width: 100% !important;
    height: auto !important;
    margin-bottom: 45px;
    border-radius: 12px;
    box-shadow: 0 10px 40px rgba(0, 0, 0, 0.5);
    transition: all 0.4s ease-in-out;
  }

  .img-wrapper img:hover {
    transform: translateY(-5px);
    box-shadow: 0 20px 50px rgba(0, 217, 255, 0.3);
    filter: brightness(1.05);
  }

  /* Évite les bugs de défilement sur mobile */
  body {
    overflow-x: hidden;
  }
</style>

<div class="img-wrapper">
  <img src="https://github.com/user-attachments/assets/5b6bcc1a-6f76-46fd-88fb-34b43fbaa0e5" />
  <img src="https://github.com/user-attachments/assets/8d54004b-3bcb-4f57-b5a0-310241f73b75" />
  <img src="https://github.com/user-attachments/assets/972ed0ac-d641-4f54-bd52-c4f9b4380774" />
  <img src="https://github.com/user-attachments/assets/39848e20-ce8b-49cb-ab3a-5679691abe8c" />
</div>
