CodexGenNamae
Générateur d'identités françaises, fantasy et compagnons — pour MJ, refuges, écrivains et devs. Offline, gratuit, sans pub.

CodexGenNamae est un utilitaire Python / CustomTkinter léger, pensé pour donner un nom cohérent en un clic. Pas d'API, pas de cloud. Il tourne sur un vieux PC sous Windows 10, même sans internet. Un clic, une identité. Ou 1000.

Licence
Offline
Python
Version

Fonctionnalités v2.2.2
Identité unique : prénom + nom / lignée / clan cohérent
Génération en masse : 12, 100, 1000 noms d'un coup (TXT / MD / CSV)
Genres : Féminine / Masculine / Neutre → vert clair #BBF7D0
14 Univers (sans doublons) :
Essentiels : 🧑 Humain Réaliste
Fantasy : 🧝 Elfe (Aube-de-Givre...), ⛏️ Nain (Barbe-d'Acier...), 👹 Orc (Arrache-Tripes...)
Divin & Démoniaque : 👼 Ange Céleste, 😈 Démon, ✨ Divinité
Mythologie : 🏺 Grecque, ⚡ Nordique
Cyber & Synth : 🌃 Netrunner, 🤖 Synthétique
Compagnons : 🐱 Chat (29F/29H/27N), 🐶 Chien, 🐦 Oiseau — F/H/Neutre (Chaussette, Biscuit...)
Base figée : tout le stock de noms dans templates/namae.json → tu étoffes sans toucher au code
Interface : CustomTkinter claire, sidebar à catégories, compatible Windows 10/11 (emojis 👼 🏺)
Principe
Chaque univers est un module Python indépendant dans _Code/modules/univers/.

python
# Exemple d'appel direct
from modules.univers.fantasy_elfe import generer
prenom, nom = generer("f")  # -> "Aelwen Brise-de-Mousse"
namae.json = la banque de noms (préfixes, suffixes, lignées)
loader.py = charge le JSON
*_*.py = un univers = 1 fichier = 1 icône
Pas de cloud. Pas d'abonnement.

Utilisation
Lancer _Code/CodexGenNamae_v2.1.1_FINAL.py ou CodexGenNamae.exe (build)
Choisir un univers à gauche (Essentiels, Fantasy, Divin & Démoniaque...)
Choisir Féminine / Masculine / Neutre
Générer → Copier
Génération en masse → Copier / Exporter en TXT, MD, CSV
Astuce : vide les dossiers __pycache__ après chaque mise à jour de modules.

Organisation v2.2.2
CodexGenNamae/
│   README.md
│   LICENCE.md / LICENSE.md
├───_Assets/
│   └───icons/ (CodexGenNamae_diagonal.ico)
├───_Code/
│   │   CodexGenNamae_v2.1.1_FINAL.py   # Main UI (v2.2.2 ULTRA CLEAN)
│   ├───modules/
│   │   ├───univers/ (14 modules SANS _1 / _2)
│   │   │   ├───realiste.py
│   │   │   ├───fantasy_elfe.py / nain / orc
│   │   │   ├───divin.py / demoniaque.py / celeste_ange.py
│   │   │   ├───mythologie_grec.py / nordique.py
│   │   │   ├───cyberpunk_netrunner.py / synthetique.py
│   │   │   └───animal_chat.py / chien / oiseaux.py  # F/H/Neutre
│   │   └───loader.py
│   └───templates/
│       └───namae.json   # Base étoffée v2.2 (seul fichier à garder)
└───_Doc/
    ├───LICENCE.md
    └───THIRD_PARTY_LICENSES.md
Versions
v1.0 - v1.3 (2025-2026) : Base Tkinter, modules f/h/autre, humain/ECA, export TXT/MD/CSV
v2.0 (2026-07-27) : Passage CustomTkinter, architecture par univers
v2.1.1 FINAL (2026-07-28) : Base figée, catégories, 14 univers, génération en masse
v2.2.2 ULTRA CLEAN (2026-07-29) :
Fix logos Windows 10 (👼 🏺), espacement, bouton vert clair
Fix animaux F/H/Neutre (KeyError corrigé)
JSON étoffé : 24 divinités, 24 démons, 25 anges, 35 lignées elfes/nains/orcs, 30 chats/chiens/oiseaux par genre
Suppression de tous les doublons _1 / _2
Roadmap - Avenir (v3.0)
Historique : Romain, Gaulois
Ethnique : Indien, Latino
Gangster Années 20 : Tom la Gachette, Tony le Casseur
i18n : Sélecteur de langue en haut à droite (FR/EN) → namae_fr.json / namae_en.json
ex: FR Jean Dubois / EN Jason Douglass
ex: Nain FR Edwyn Marteau d'Acier / EN Edwyn Steelhammer
L'architecture actuelle permet d'ajouter un univers en 2 minutes : 1 fichier .py + 1 section dans le JSON.

Lore
Un monde sans noms est un monde sans mémoire. CodexGenNamae donne un nom à ceux qui n'en ont pas encore — du chat de refuge à la divinité du firmament.

Licence
CircaFrax Proprietary Freeware v1.0 — Voir LICENCE.md (FR) / LICENSE.md (EN)

Gratuit à vie, perso / asso / pro / commercial
Distribution gratuite à l'identique avec licence intacte
Code source privé, non open-source
Offline, sans pub, sans télémétrie
Composants tiers : customtkinter — MIT License, voir _Doc/THIRD_PARTY_LICENSES.md

Libre d'usage. Source gardée. Comme un atelier qui prête ses outils mais garde ses plans.
CircaFrax — Strasbourg, France — 2026

