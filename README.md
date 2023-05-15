# Mood AI

<img src="https://fs.npstatic.com/userfiles/7687254/image/Weather-app-w810h462.jpg"></img>

Au cours de ce Coding-club, tu vas apprendre a developper ta première application mobile réactive, créer son interface graphique, comprendre comment fonctionne une intelligence artificielle et ses enjeux de demain.

### Qu'est-ce que Flutter ?

<img src="https://humancoders-formations.s3.amazonaws.com/uploads/course/logo/1148/formation-flutter.png" height="150"></img>

Flutter est un framework open-source développé par Google qui permet de créer des applications multiplateformes avec une seule base de code. Il utilise le langage de programmation Dart et fournit une vaste collection de widgets prêts à l'emploi pour construire des interfaces utilisateur réactives.

## Prérequis

Avant de commencer à coder l'application, assurez-vous d'avoir téléchargé éléments suivants :

- Flutter SDK installé sur votre machine.
- VScode installé avec l'extension Flutter.
- Prendre connaissance de tablemachine.withgoogle.com

## Creation du projet

Créez un nouveau projet Flutter en utilisant la commande suivante dans votre terminal :
`flutter create my_mood_ai_app`

differents fichiers vont apparaitre sur votre table de travail, parmis eux le fichier
`pubspec.yaml`, celui ci permet d'installer une extensions permettant d'ajouter des paquets afin d'elargir les possibilités de developpment avec flutter.

l'extension que nous allons utiliser pour mener a bien ce projet se nomme `google_mlkit_face_detection` et permettra la detection faciale.

### Mais qu'est ce qu'une IA?

<img src="https://d1fmx1rbmqrxrr.cloudfront.net/zdnet/optim/i/edit/ne/2023/IArobot__w1200.jpg"></img>

ensemble des théories et des techniques développant des programmes informatiques complexes capables de simuler certains traits de l'intelligence humaine.

Pour installer un package, tapez la commande `flutter pub add nom_du_package` dans le terminal.

## Familiarisation de l'espace de travail

<img src="https://blog.logrocket.com/wp-content/uploads/2022/02/main-dart-flutter-great-opener.png"></img>

Vous pouvez constater qu'il y a sur votre espace de travail plusieurs noms de système d'exploitation tel que `ios`, `android`, c'est grâce à ces dossier que le code de chaque plateforme est traité puis est ensuite compilé dans le dossier `build` qui apparaitra lors votre première compilation.

Maintenant, concentrons nous sur le dossier `lib`, dans celui ci vous trouverez le fichier `main.dart` qui est le fichier principal de l'application, c'est dedans que l'on vas pouvoir coder l'entierté de l'application.

## Lancement de l'application

<img height="250" src="https://www.emanprague.com/wp-content/uploads/2018/04/first_start.png"></img>

Dans le fichier `main.dart` se trouve du code par defaut proposé par flutter, vous pouvez desormais lancer l'application de base de flutter sur la plateforme de votre choix (dans la mesure du possible), pour cela tappez la commande `flutter run`, vous pourrez desormais chosir de compiler votre application sur Chrome, peut etre un simulateur android, ou bien votre propre téléphone si celui ci est branché à votre ordinateur. Pour selectionner quel appareil compiler l'application tapez 1, 2, 3 ou plus dans votre terminal.

Vous pouvez essayer de changer le titre de l'application dans le code dans `main.dart` en remplacant par exemple "Flutter Demo HomePage" par le titre de l'application de votre choix, une fois cela fais tapez la commande `r` pour rafraîchir les widgets de l'application, assurez vous d'avoir activé l'auto-save sur vscode.

### Qu'est ce qu'un widget?

<img  src="https://static.javatpoint.com/tutorial/flutter/images/flutter-widgets.png"></img>

Les widgets sont les éléments de base utilisés pour construire l'interface utilisateur d'une application. Un widget est une classe qui décrit la structure et l'apparence d'une partie de l'interface utilisateur, tel qu'un bouton, une image, un texte, etc... Les widgets peuvent être imbriqués les uns dans les autres pour créer une hiérarchie d'éléments d'interface plus complexes.

tu pourras comprendre comment fonctionne chaque widget grâce a la documentation suivante: 
https://api.flutter.dev/flutter/widgets/Image-class.html

## Conseil

Essayez de changer les valeurs, les ordres d'embriquements des widgets pour vous y familiariser.

Gardez à l'esprit que toutes l'interface graphique de l'application et les widgets sont placé à l'interieur des accolades de `Widget build(BuildContext context){}`.

## Procédé d'arriere plan

Tout ce qui est donc au dessus de `Widget build(BuildContext context){}` servira pour la partie arrière plan de l'application, dans l'exemple de `main.dart` proposé par flutter, 
`void initState()`, tu devras la developper pour récupérer les valeurs de l'api et qui nous fournira des données météorologique, s'elle ci devra etre placer au dessus de `initState`.

## Étape 1

Le projet se decompose en 3 importantes parties, la premiere est la creation du fichier `camera`
dans lequel tu créera un fichier te permettant de pouvoir appeler la caméra de ton télephone, en important le package `camera`, en lisant la documentation de l'implémentation du package camera, tu sera libre la crée ta camera personnalisé en modifiant le curseur de zoom, mode selfie, grand angle, les possibilités de la creation de ta camera sont infini.

## Étape 2

Une fois ta camera réalisé, tu vas pouvoir crée un fichier `painter` dans lequel tu vas pouvoir ajouter les points de tracking pour chaque partie du visage detectable par le package proposé soit plus de 12 points de tracking.

## Étape 3

Une fois ta le painting et la camera réalisé, tu vas pouvoir rassembler les 2 en appelant les 2 classes que tu as crées dans leur fichier respectif pour que la camera s'empile par dessus la couche painting afin de detecter le visage.

Félicitaion tu as réaliser ton projet IA, maintenant tu peux paufiner ton interface graphique pour qu'elle te corresponde.

## Bonus

Afficher de maniere explicite les emotions du visage, pour cela tu peux te rendre sur le site https://teachablemachine.withgoogle.com

Tu vas pouvoir commencer un projet d'image, entrainer une `Class 1` que tu appelera Happy par exemple et en allumant la camera tu vas pouvoir te filmer et prendre plusieurs photos de toi joyeux,

Ensuite cree une classe Sad ou de meme tu vas te montrer triste, repete ce procéder pour toutes les emotions que tu souhaite detecter.

Ensuite entraine le modele et exporte le en "Tensorflow lite". Dans ce fichier télecharger tu trouvera les labels de chaque nom de tes classe dans un fichier texte, et un fichier .tsf dans lequel tes emotions du visage sont belles et bien entrainé.

Plus qu'a importer la librairie Tensorflow dans laquelle tu pourra lire le modèle entrainé au prealable et l'associé a la camera pour detecter correctemps les emotions et les afficher de la maniere te souhait selon ton interface graphique dans un widget `Text`

PS: Le package tensorflow ne fonctionne uniquement que pour les télephones iOS et Android, la version web et desktop ne sont pas encore compatibles pour associé le modele a ce que la camera recoit.