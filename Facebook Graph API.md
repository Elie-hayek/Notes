# 1. Facebook API 

L’API Graph est le meilleur moyen d’insérer et de récupérer des données dans la plate-forme Facebook. Il s’agit d’une API basée sur le protocole HTTP qui permet aux apps d’avoir recours à la programmation pour interroger des données, publier de nouvelles actualités, gérer des publicités, importer des photos et réaliser un large éventail d’autres tâches.

Une représentation des informations sur Facebook. II est composé de **nœuds, d’arêtes et de champs**. Généralement, vous utilisez les nœuds pour obtenir des données sur un objet en particulier, les arêtes pour obtenir des collections d’objets sur un objet unique et les champs pour obtenir des données sur un objet unique ou sur chaque objet d’une collection.

Tous les transferts de données sont conformes au protocole HTTP1.1 et tous les points de terminaison nécessitent le protocole HTTPS.

resque toutes les demandes sont transmises à l’URL d’hébergement graph.facebook.com. Les seules exceptions sont les importations de vidéos, qui utilisent graph-video.facebook.com

### Tokens d’accès

Les tokens d’accès permettent à votre application d’accéder à l’API Graph. Presque tous les points de terminaison de l’API Graph exigent un token d’accès d’une certaine nature. Votre demande peut donc en nécessiter un chaque fois que vous accédez à un point de terminaison. Ils remplissent généralement deux fonctions :

- Ils permettent à votre application d’accéder aux informations d’un utilisateur sans avoir besoin du mot de passe de ce dernier ; Par exemple, votre application a besoin de l’e-mail d’un utilisateur pour exécuter une fonction. Si l’utilisateur accepte d’autoriser votre application à récupérer son adresse e-mail à partir de Facebook, il n’aura pas à saisir son mot de passe Facebook pour la récupération.

- Ils nous permettent d’identifier votre application, son utilisateur et le type de données que celui-ci permet à votre application de consulter.

Le token contient notamment sa date d’expiration et le nom de l’app qui l’a généré. La plupart des appels d’API sur Facebook doivent contenir un token d’accès, en raison des contrôles de confidentialité. Il existe différents types de tokens d’accès pour prendre en charge les divers cas d’utilisation :


![Capture d’écran 2022-07-06 à 09 55 58](https://user-images.githubusercontent.com/108743863/177499674-8d66205f-b341-41b4-98da-daefcdd8eccf.png)

# 2. Obtenir un jeton d’accès:

1. Créez une application Facebook ou utilisez-en une que vous avez déjà créée :
 [Facebook Developers apps](https://developers.facebook.com/apps)

2. Saisissez les informations de création de l’application

3. Notez quelque-part les informations concernant l’identité de votre application

   Client ID = 564101085273434, et Client Secret = a7ba11ca9bc85956234070defc1279a5
   
4. Rendez-vous ensuite sur : [Explorateur de l’API Graph de Facebook](https://developers.facebook.com/tools/explorer)

5. Sélectionnez l’application que vous venez de créer dans le menu déroulant en haut à droite

6. Cliquez ensuite sur le bouton « Obtenir un token d’accès de Page »

7. Sélectionnez maintenant la page en question sur laquelle vous souhaitez publier du contenu

8. Copiez le jeton d’accès (access token) disponible dans le champ d’entré à « Jeton d’accès »

    *EAAIBDATOHVoBAFAdbCaBCGnMJX2uk2ZCi4eTKVJOs3Fq6oWa78OEuwQZBSejFCJeacoienpvRccoiL7ybXUrcOwkg4TLFVqVyZBeoMymmuGvemc13uNBAmLz2EzKRZCUlurX5pEal2TzVvumvX H551ZAt1k9mkdKUsP8yqXIMIHR0ZBxZARzJiX*
    
9. Remplacez ensuite dans l’URL suivante :

   https://graph.facebook.com/oauth/access_token?client_id=CID&client_secret=CS&grant_type=fb_exchange_token&fb_exchange_token=AT
  
    - CID par l’ID de votre application relevé plus haut
    - CS par le code secret de votre application relevé plus haut
    - AT par le jeton d’accès précédemment copié

# 3. Vérifier le durée de validation d’un jeton d’accès et étendre sa validité:

1. Accédez à [Explorateur de l’API Graph de Facebook](https://developers.facebook.com/tools/explorer)

2. Sélectionnez votre application dans le menu déroulant en haut à droite

3. Cliquez sur le bouton « Obtenir un token d’accès de Page » juste en dessous

4. Dans le champ de saisie « Jeton d’accès », cliquez sur l’icône du point d’exclamation bleu

5. Dans le menu contextuel, cliquez sur le bouton « Ouvrir dans l’outil Access Token » en bas à gauche de la fenêtre contextuelle

6. Cela ouvrira une nouvelle page avec les détails du jeton d’accès (access token) de cette application, vous verrez probablement que le jeton ne dure qu’une heure ou plus

8. Pour étendre ce jeton d’accès et en obtenir un qui n’expire pas, cliquez sur le bouton « Extension du jeton d’accès »
Cela vous donnera un jeton d’accès jamais expiré

{"access_token":"EAAIBDATOHVoBADIkubeVgZARnbKELj6ZBZA7xrvZCWd0vZAvbLlxZAuESoMVJZAZA5SZClfFCFUYaEEL0LeyqTF8GySlPOKzuxoZBx7yRuoArt7Hv4ZBudzM61LKHBYnDRZA9UG3HESlBIlz2rRSiIz69vxnmy5ZByTbFISQrfcjnzjRmx7ZA9UpdqE3lr","token_type":"bearer","expires_in":5181341}
