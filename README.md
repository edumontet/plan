# Mon plan

Web app pour se guider à pied sur la photo d'un plan (zoo, parc, salon…), à l'adresse `https://edumontet.github.io/plan/`. Elle s'installe sur l'écran d'accueil de l'iPhone (Safari › Partager › Sur l'écran d'accueil).

1. On photographie le plan, puis on place ses 4 coins pour redresser la photo (prise de biais).
2. On touche l'endroit où l'on est, puis la destination.
3. **Calage** (une fois par plan) : téléphone à plat, on marche jusqu'à un repère reconnaissable et on le touche sur le plan. Le trajet mesuré (pas comptés par l'accéléromètre, direction donnée par la boussole) comparé au trajet sur le plan donne l'échelle et l'orientation du plan.
4. Le triangle bleu suit ensuite les pas et la direction du téléphone ; le bandeau indique la distance à vol d'oiseau et le sens à prendre. « Je suis ici » corrige la position et affine le calage.

Les plans et leur calage sont enregistrés dans le téléphone (rien n'est envoyé en ligne). Il faut autoriser « Mouvements et orientation » au premier lancement. Ajouter `?demo` à l'adresse permet de simuler le cap et les pas sur un ordinateur.

## Mettre en ligne

Dans le dépôt GitHub : **Settings › Pages**, source **Deploy from a branch**, branche **main**, dossier **/ (root)**, puis **Save**.

## Technique

HTML, CSS et JavaScript sans étape de build ni dépendance (`index.html`, `plan.css`, `plan.js`).

## Mises à jour automatiques

L'appli charge `update.js` : quand on la rouvre, elle compare ses fichiers à ceux du serveur et se recharge seule s'ils ont changé. Pas besoin de la réinstaller depuis l'écran d'accueil.
