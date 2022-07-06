## API Graph 

L’API Graph est le meilleur moyen d’insérer et de récupérer des données dans la plate-forme Facebook. Il s’agit d’une API basée sur le protocole HTTP qui permet aux apps d’avoir recours à la programmation pour interroger des données, publier de nouvelles actualités, gérer des publicités, importer des photos et réaliser un large éventail d’autres tâches.

Une représentation des informations sur Facebook. II est composé de **nœuds, d’arêtes et de champs**. Généralement, vous utilisez les nœuds pour obtenir des données sur un objet en particulier, les arêtes pour obtenir des collections d’objets sur un objet unique et les champs pour obtenir des données sur un objet unique ou sur chaque objet d’une collection.

Tous les transferts de données sont conformes au protocole HTTP1.1 et tous les points de terminaison nécessitent le protocole HTTPS.

resque toutes les demandes sont transmises à l’URL d’hébergement graph.facebook.com. Les seules exceptions sont les importations de vidéos, qui utilisent graph-video.facebook.com

### Tokens d’accès

Les tokens d’accès permettent à votre application d’accéder à l’API Graph. Presque tous les points de terminaison de l’API Graph exigent un token d’accès d’une certaine nature. Votre demande peut donc en nécessiter un chaque fois que vous accédez à un point de terminaison. Ils remplissent généralement deux fonctions :
