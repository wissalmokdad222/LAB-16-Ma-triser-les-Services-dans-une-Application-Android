#  Service Chronomètre Android (Java)

Bienvenue dans le projet **Service Chronomètre Java**. Cette application Android illustre l'implémentation d'un **Foreground Service** (service de premier plan) pour maintenir un chronomètre actif, même lorsque l'utilisateur quitte l'application ou que le système réduit ses ressources.

##  Fonctionnalités

- **Chronomètre Persistant** : Le temps continue de s'écouler en arrière-plan grâce à un service dédié.
- **Notification Interactive** : Affiche le temps écoulé en temps réel dans le volet des notifications.
- **Bound Service** : Communication bidirectionnelle entre l'activité principale (`MainActivity`) et le service (`ChronometreService`).
- **Conformité Android 14+** : Utilisation du type de service `dataSync` et gestion des permissions modernes.

##  Architecture du Projet

Le projet est structuré autour de composants clés d'Android :

1.  **`ChronometreService.java`** : Le cœur de l'application. Il gère le timer via un `ScheduledExecutorService` et met à jour la notification.
2.  **`MainActivity.java`** : L'interface utilisateur qui permet de démarrer et d'arrêter le service. Elle se "lie" (bind) au service pour interagir avec lui.
3.  **`AndroidManifest.xml`** : Déclare les permissions nécessaires (`FOREGROUND_SERVICE`, `POST_NOTIFICATIONS`) et le type de service.

##  Aperçu de l'Utilisation

1.  **Démarrer** : Appuyez sur le bouton "DÉMARRER SERVICE". Une notification apparaît et le chrono commence.
2.  **Arrière-plan** : Vous pouvez fermer l'application, le chrono reste visible dans vos notifications.
3.  **Arrêter** : Revenez dans l'app et appuyez sur "ARRÊTER SERVICE" pour stopper le timer et supprimer la notification.

##  Configuration Requise

- **Langage** : Java
- **SDK Minimum** : API 24 (Android 7.0)
- **SDK Cible** : API 34+ (Android 14)
- **IDE** : Android Studio (Koala ou plus récent recommandé)

## Demonstration:
![Video](https://github.com/user-attachments/assets/17d8ad75-8cbc-46dc-b5ca-cf672592a67b)


