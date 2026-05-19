Je veux créer une page web (HTML/CSS/JS pur, UN SEUL fichier .html) qui sert d'activité interactive à la fin d'un oral d'anglais sur le PSG. Elle sera projetée en classe et le public glissera des cartes joueurs sur un terrain pour composer le XI ultime du PSG dans l'histoire du club.

═══════════════════════════════════════════
CHARTE GRAPHIQUE (à respecter strictement)
═══════════════════════════════════════════
- Fond principal : noir profond #0A0A0A
- Rouge PSG : #E30613
- Bleu PSG : #004170
- Texte : blanc cassé #F5F5F5
- Terrain : vert très sombre #0A3A1A avec lignes blanches semi-transparentes
- Police titres : "Arial Black", Impact, sans-serif (style affiche de match)
- Police texte : Arial, sans-serif

═══════════════════════════════════════════
STRUCTURE DE LA PAGE
═══════════════════════════════════════════

EN HAUT (bandeau) :
- Titre "BUILD THE ULTIMATE PSG XI" en rouge énorme, centré
- Sous-titre "All-time legends — choose your starting eleven"
- À droite du bandeau : compteur "X / 12" + bouton "RESET"

ZONE PRINCIPALE (split en 2) :

CÔTÉ GAUCHE (≈ 65% largeur) — LE TERRAIN
- Terrain de foot vu de haut, vertical, en 4-3-3
- Lignes blanches (rond central, surface de réparation, etc.) semi-transparentes
- 11 zones de drop matérialisées par des cercles pointillés blancs avec le nom du poste écrit en dessous (GK, LB, CB, CB, RB, CDM, CM, CM, LW, ST, RW)
- Disposition 4-3-3 du bas vers le haut :
  * Ligne 1 : 1 GK (centré)
  * Ligne 2 : LB - CB - CB - RB (les 4 défenseurs)
  * Ligne 3 : CDM (un cran en dessous) + 2 CM au-dessus à gauche et à droite — triangle inversé
  * Ligne 4 : LW - ST - RW (les 3 attaquants)
- À CÔTÉ du terrain (à gauche du terrain ou en haut) : 1 case ronde séparée "COACH" pour le 12e drop

CÔTÉ DROIT (≈ 35% largeur) — LES CARTES
- Affiche le poste actuellement à pourvoir (gros titre en rouge, exemple : "GOALKEEPER — pick one")
- Affiche les 5 cartes des candidats pour ce poste, empilées verticalement ou en grille 2+3
- Style des cartes : style FIFA Ultimate Team
  * Format vertical, environ 180px × 260px
  * Dégradé doré pour les légendes / argenté pour les actuels (à toi de choisir selon le joueur)
  * Cercle au centre avec les initiales du joueur en gros (placeholder)
  * Nom du joueur en bas, en majuscules
  * Petite icône drapeau pays (emoji ok) en haut à gauche
  * Effet "shine" au survol
- Les cartes sont DRAGGABLES

═══════════════════════════════════════════
MÉCANIQUE
═══════════════════════════════════════════

1. Au chargement, le poste GK est actif. Les 5 cartes gardiens s'affichent à droite.
2. Le présentateur drag une carte sur la case GK du terrain.
3. Au drop réussi :
   - La carte se "fixe" dans la case du terrain (transition smooth, animation rouge qui flashe puis se stabilise)
   - Le compteur passe à "1 / 12"
   - Le poste suivant devient actif (les 5 cartes à droite changent automatiquement)
4. Ordre des postes : GK → LB → CB (gauche) → CB (droit) → RB → CDM → CM gauche → CM droit → LW → ST → RW → COACH
5. Si on drop sur la mauvaise case : la carte revient à sa position d'origine + petit shake animation rouge
6. À la fin (12/12) : animation de confettis aux couleurs PSG + apparition d'un message "VOTRE XI ULTIME" en grand au-dessus du terrain
7. Bouton RESET : remet tout à zéro, terrain vide, premier poste actif

═══════════════════════════════════════════
DONNÉES JOUEURS (12 postes × 5 candidats)
═══════════════════════════════════════════

NOTE : pour chaque joueur, j'aurai besoin d'un type de carte ("gold" pour les légendes / "silver" pour les joueurs actuels) — à toi de choisir intelligemment. Les drapeaux pays sont importants, mets l'emoji correspondant.

1. GK (Goalkeeper)
- Gianluigi Buffon 🇮🇹 (gold)
- Salvatore Sirigu 🇮🇹 (silver)
- Bernard Lama 🇫🇷 (gold)
- Gianluigi Donnarumma 🇮🇹 (gold)
- Lucas Chevalier 🇫🇷 (silver)

2. LB (Left Back)
- Layvin Kurzawa 🇫🇷 (silver)
- Maxwell 🇧🇷 (gold)
- Juan Bernat 🇪🇸 (silver)
- Nuno Mendes 🇵🇹 (gold)
- Lucas Hernandez 🇫🇷 (silver)

3. CB LEFT (Center Back gauche)
- Mamadou Sakho 🇫🇷 (gold)
- Alex 🇧🇷 (silver)
- Presnel Kimpembe 🇫🇷 (gold)
- Willian Pacho 🇪🇨 (silver)
- David Luiz 🇧🇷 (silver)

4. CB RIGHT (Center Back droit)
- Marquinhos 🇧🇷 (gold)
- Thiago Silva 🇧🇷 (gold)
- Alessandro Nesta 🇮🇹 (silver)
- Sergio Ramos 🇪🇸 (gold)
- Illia Zabarnyi 🇺🇦 (silver)

5. RB (Right Back)
- Achraf Hakimi 🇲🇦 (gold)
- Dani Alves 🇧🇷 (gold)
- Gregory Van der Wiel 🇳🇱 (silver)
- Serge Aurier 🇨🇮 (silver)
- Thomas Meunier 🇧🇪 (silver)

6. CDM (Defensive Midfielder)
- Marco Verratti 🇮🇹 (gold)
- Claude Makélélé 🇫🇷 (gold)
- Thiago Motta 🇮🇹 (gold)
- Blaise Matuidi 🇫🇷 (silver)
- Vitinha 🇵🇹 (gold)

7. CM RIGHT (box-to-box)
- Adrien Rabiot 🇫🇷 (silver)
- Idrissa Gueye 🇸🇳 (silver)
- Fabián Ruiz 🇪🇸 (gold)
- João Neves 🇵🇹 (silver)
- Warren Zaïre-Emery 🇫🇷 (silver)

8. CM LEFT (créatif)
- Ronaldinho 🇧🇷 (gold)
- Marco Verratti 🇮🇹 (gold)
- Javier Pastore 🇦🇷 (gold)
- Désiré Doué 🇫🇷 (gold)
- Kang-In Lee 🇰🇷 (silver)

9. RW (Right Winger)
- Lionel Messi 🇦🇷 (gold)
- Bradley Barcola 🇫🇷 (silver)
- Ousmane Dembélé 🇫🇷 (gold)
- Lucas Moura 🇧🇷 (silver)
- Ángel Di María 🇦🇷 (gold)

10. ST (Striker, n°9)
- Zlatan Ibrahimović 🇸🇪 (gold)
- Edinson Cavani 🇺🇾 (gold)
- Pauleta 🇵🇹 (gold)
- Kylian Mbappé 🇫🇷 (gold)
- George Weah 🇱🇷 (gold)

11. LW (Left Winger)
- Neymar Jr. 🇧🇷 (gold)
- Khvicha Kvaratskhelia 🇬🇪 (gold)
- Ezequiel Lavezzi 🇦🇷 (silver)
- Jérôme Rothen 🇫🇷 (silver)
- Safet Sušić 🇧🇦 (gold)

12. COACH
- Luis Enrique 🇪🇸 (gold)
- Laurent Blanc 🇫🇷 (silver)
- Carlo Ancelotti 🇮🇹 (gold)
- Unai Emery 🇪🇸 (silver)
- Mauricio Pochettino 🇦🇷 (silver)

═══════════════════════════════════════════
DÉTAILS TECHNIQUES
═══════════════════════════════════════════
- UN SEUL fichier .html avec tout dedans (CSS dans <style>, JS dans <script>)
- Pas de framework, pas de dépendances externes (sauf éventuellement une lib confettis CDN si tu veux)
- Drag and drop natif HTML5 (dragstart, dragover, drop)
- Compatible Chrome / Firefox récents
- Pas de backend, tout en mémoire
- Optimisé pour projection en classe : résolution cible 1920×1080, mais fonctionnel jusqu'à 1280×720
- Cartes joueurs : PAS de vraies photos pour l'instant, juste un placeholder rond (background dégradé) avec les initiales du joueur en gros au centre

═══════════════════════════════════════════
PRIORITÉS DE DESIGN
═══════════════════════════════════════════
1. Effet "affiche de match" maintenu partout (gros titres, fond noir, accents rouges)
2. Les cartes doivent vraiment ressembler à des cartes FIFA UT, c'est LE point visuel clé
3. L'animation de fin (12/12 complet) doit être satisfaisante visuellement
4. Tout doit être lisible projeté à 5 mètres : pas de texte en dessous de 18px