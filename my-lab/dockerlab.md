<style>
    /* 1. On réinitialise TOUT pour éviter les conflits */
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    html, body {
        width: 100%;
        overflow-x: hidden; /* Empêche le décalage vers la droite */
        background: #1a1f2e;
    }

    /* 2. On crée un conteneur pour s'assurer que rien ne dépasse */
    .image-container {
        width: 100%;
        display: flex;
        flex-direction: column;
    }

    img {
        width: 100% !important; /* Prend toute la largeur disponible */
        height: auto !important; /* Garde les proportions réelles */
        display: block;
        border: none;
        /* On retire les max-width qui pourraient bloquer */
        max-width: 100vw; 
    }
</style>

<div class="image-container">
    <img src="https://github.com/user-attachments/assets/5b6bcc1a-6f76-46fd-88fb-34b43fbaa0e5" />
    <img src="https://github.com/user-attachments/assets/8d54004b-3bcb-4f57-b5a0-310241f73b75" />
    <img src="https://github.com/user-attachments/assets/972ed0ac-d641-4f54-bd52-c4f9b4380774" />
    <img src="https://github.com/user-attachments/assets/39848e20-ce8b-49cb-ab3a-5679691abe8c" />
</div>
