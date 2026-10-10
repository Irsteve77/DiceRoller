DICEROLLER
==========

Application Android de lancer de dé, développée en Kotlin avec Jetpack Compose (Material 3).


DESCRIPTION
-----------
DiceRoller affiche un dé à l'écran. Au lancement de l'application, une face
aléatoire (de 1 à 6) est affichée. Un clic sur le bouton "Roll" relance le dé
et change l'image.


FONCTIONNALITÉS
---------------
- Face de dé aléatoire au démarrage de l'application
- Bouton pour relancer le dé
- Image du dé mise à jour à chaque lancer
- Description d'accessibilité reflétant la valeur du dé
- Interface Jetpack Compose avec thème Material 3


PRÉREQUIS
---------
- Android Studio (version récente)
- JDK 17 ou plus (le JDK embarqué d'Android Studio convient)
- Un émulateur (ex. Pixel 4, API 33) ou un téléphone Android avec le
  débogage USB activé
- Une connexion Internet pour le premier build (dépendances Gradle)


INSTALLATION ET LANCEMENT
-------------------------
1. Ouvrir le dossier du projet dans Android Studio.
2. Attendre la fin de la synchronisation Gradle.
3. Choisir un appareil (émulateur ou téléphone).
4. Cliquer sur le bouton Run.

Pour générer l'APK de debug en ligne de commande :

    gradlew assembleDebug

L'APK se trouve dans : app/build/outputs/apk/debug/


STRUCTURE DU PROJET
-------------------
app/src/main/java/ci/emu/diceroller/MainActivity.kt   Activité et composables
app/src/main/java/ci/emu/diceroller/ui/theme/         Thème de l'application
app/src/main/res/drawable/                            Images dice_1 à dice_6
app/src/main/res/values/strings.xml                   Textes (ex. "roll")


RESSOURCES NÉCESSAIRES
----------------------
- Les images dice_1 à dice_6 dans res/drawable
- La chaîne "roll" dans res/values/strings.xml


PROBLÈMES COURANTS
------------------
* Échec du téléchargement d'aapt2 ("Remote host terminated the handshake") :
  changer de connexion, désactiver le VPN ou l'antivirus qui inspecte le HTTPS,
  vérifier le JDK utilisé par Gradle (jbr-17).

* Erreur "Can't find service: package" à l'installation :
  l'émulateur n'a pas fini de démarrer. Attendre, puis cliquer sur Retry, ou
  faire un Cold Boot depuis le Device Manager.


TECHNOLOGIES
------------
Kotlin, Jetpack Compose, Material 3, Gradle


AUTEUR
------
Steve