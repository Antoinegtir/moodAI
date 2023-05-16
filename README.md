# Mood AI

Au cours de ce Coding-club, tu vas apprendre a developper ta première application mobile réactive, créer son interface graphique, comprendre comment fonctionne une intelligence artificielle et ses enjeux de demain.

### Qu'est-ce que Flutter ?

<img src="https://humancoders-formations.s3.amazonaws.com/uploads/course/logo/1148/formation-flutter.png" height="150"></img>

Flutter est un framework open-source développé par Google qui permet de créer des applications multiplateformes avec une seule base de code. Il utilise le langage de programmation Dart et fournit une vaste collection de widgets prêts à l'emploi pour construire des interfaces utilisateur réactives.

## L'utilité ?

- Application utilisable pour detecter les emotions du visage humain.

<img src="https://static.vecteezy.com/ti/vecteur-libre/p3/7802611-niveaux-d-emotion-sur-l-echelle-de-differents-visages-icone-element-de-conception-pour-l-evaluation-des-retroactions-notation-evaluation-du-produit-ensemble-emoji-avec-differentes-emotions-sur-fond-blanc-illustrationle-vectoriel.jpg" height="150"></img>

- Application utilisable pour remplacer son visage par un filtre de type réseaux social

<img src="https://www.it-connect.fr/wp-content-itc/uploads/2020/04/teams-filtre-snap-02.jpg" height="150"></img>

- Application utilisable dans l'industrie du cinéma pour effectuer des points de traking visant a remplacer le visage par un modele 3D et quelconque effets speciaux.

<img src="https://i.pinimg.com/originals/0e/7a/36/0e7a368f8bf361ec53eee9de527181f0.jpg" height="150"></img>

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
