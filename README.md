<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CV - SEYVE Jules</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f0f4f8;
            color: #333;
            margin: 0;
            padding: 0;
        }
        .container {
            max-width: 800px;
            margin: 50px auto;
            background-color: #e1e1e1;
            padding: 30px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            border-radius: 8px;
        }
        h1, h2, h3 {
            margin: 0;
            color: #2c3e50;
        }
        h1 {
            font-size: 2.5em;
            text-align: center;
            margin-bottom: 10px;
        }
        h2 {
            font-size: 1.8em;
            border-bottom: 2px solid #98973f;
            padding-bottom: 5px;
            margin-top: 40px;
            margin-bottom: 15px;
        }
        h3 {
            font-size: 1.2em;
            margin: 10px 0;
            color: #5c5b27;
        }
        p {
            line-height: 1.6;
            margin-bottom: 15px;
        }
        .personal-info {
            text-align: center;
            margin-bottom: 40px;
        }
        .personal-info h2 {
            font-size: 1.5em;
            color: #5c5b27;
        }
        ul {
            list-style-type: none;
            padding: 0;
        }
        ul li {
            background-color: #eaeaea;
            padding: 10px;
            margin-bottom: 10px;
            border-radius: 5px;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>SEYVE Jules</h1>
        <div class="personal-info">
            <h2>18 ans</h2>
        </div>

        <section>
            <h2>Expérience</h2>
            <ul>
                <li><h3>Obtention d'un Bac PRO Systèmes Numériques - Option B</h3></li>
                <li><h3>(Audiovisuel, Réseaux et Équipements Domestiques)</h3></li>
                <li><h3>Lycée Pierre DESGRANGES - Andrézieux Bouthéon</h3></li>
            </ul>
        </section>

        <section>
            <h2>Stages Professionnels</h2>
            <ul>
                <li><h3>Entreprise Abicom</h3></li>
                <li><h3>Opéra de Saint-Etienne</h3></li>
                <li><h3>Pôle culturel de l'OPSIS (Mairie de Roche La Molière)</h3></li>
            </ul>
        </section>

        <section>
            <h2>Compétences</h2>
            <ul>
                <li><h3>Déploiement MDT (Microsoft Deployment Toolkit)</h3></li>
                <li><h3>Maintenance de systèmes informatiques</h3></li>
                <li><h3>Installation réseau</h3></li>
            </ul>
        </section>

        <section>
            <h2>Langues</h2>
            <ul>
                <li><h3>Anglais</h3></li>
                <li><h3>Espagnol</h3></li>
            </ul>
        </section>

        <section>
            <h2>Activités de loisirs</h2>
            <ul>
                <li><h3>Guitare, Musique, Café, Dodo</h3></li>
            </ul>
        </section>
    </div>

</body>
</html>
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Retour en haut</title>
  <style>
    /* Style du bouton */
    #btnTop {
      display: none; /* Caché par défaut */
      position: fixed;
      bottom: 20px;
      right: 30px;
      z-index: 99;
      font-size: 18px;
      border: none;
      outline: none;
      background-color: #555;
      color: white;
      cursor: pointer;
      padding: 15px;
      border-radius: 10px;
    }

    #btnTop:hover {
      background-color: #000;
    }

    /* Style de contenu pour le défilement */
    .content {
      height: 2000px; /* Pour avoir un contenu assez long */
      padding: 20px;
      font-size: 20px;
    }
  </style>
</head>
<body>

  <!-- Bouton pour revenir en haut -->
  <button onclick="topFunction()" id="btnTop" title="Retour en haut">⬆</button>

  <script>
    // Récupérer le bouton
    let btnTop = document.getElementById("btnTop");

    // Montrer le bouton quand on descend de 200px
    window.onscroll = function() {
      if (document.body.scrollTop > 200 || document.documentElement.scrollTop > 200) {
        btnTop.style.display = "block";
      } else {
        btnTop.style.display = "none";
      }
    };

    // Fonction pour revenir en haut de la page
    function topFunction() {
      document.body.scrollTop = 0; // Pour Safari
      document.documentElement.scrollTop = 0; // Pour Chrome, Firefox, IE et Opera
    }
  </script>
</body>
</html>
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mode Sombre ou Classique</title>
  <style>
    /* Styles par défaut (mode classique) */
    body {
      font-family: Arial, sans-serif;
      background-color: rgb(182, 182, 182);
      color: black;
      margin: 0;
      padding: 20px;
      transition: background-color 0.3s, color 0.3s;
    }

    /* Bouton de basculement */
    #toggleBtn {
      position: fixed;
      top: 20px;
      right: 20px;
      padding: 10px 20px;
      font-size: 16px;
      cursor: pointer;
      background-color: #555;
      color: white;
      border: none;
      border-radius: 5px;
      z-index: 100;
    }

    #toggleBtn:hover {
      background-color: #333;
    }

    /* Mode sombre */
    body.dark-mode {
      background-color: #2c2c2c;
      color: #2c2c2c;
    }
  </style>
</head>
<body>

  <button id="toggleBtn">Mode Sombre</button>

  <script>
    const toggleBtn = document.getElementById('toggleBtn');
    const body = document.body;

    // Fonction pour basculer entre les modes
    toggleBtn.addEventListener('click', function() {
      body.classList.toggle('dark-mode');
      
      // Changer le texte du bouton selon le mode actif
      if (body.classList.contains('dark-mode')) {
        toggleBtn.textContent = 'Mode Classique';
      } else {
        toggleBtn.textContent = 'Mode Sombre';
      }
    });
  </script>
</body>
</html>
