
- Une injection SQL, c’est une application web utilisant le langage SQL qui peut se transformer en injection SQL lorsque des données fournies par l'utilisateur sont incluses dans la requête SQL.

- Aspect : https://website.thm/blog?id=1  qui est traduit ainsi => SELECT * from blog where id=1 and private=0 LIMIT 1;

- https://website.thm/blog?id=2;--  : Le point-virgule dans l'URL signifie la fin de l'instruction SQL, et les deux tirets font que tout ce qui suit est traité comme un commentaire.

**In-Band SQL Injection** :
    C'est le type d'injection le plus facile à détecter et à exploiter | simplement à la même méthode de communication utilisée pour exploiter la vulnérabilité et recevoir les résultats.

**Error-Based SQL injection** :
    Ce type d'injection SQL est le plus utile pour obtenir facilement des informations sur la structure de la base de données, car les messages d'erreur de la base de données sont imprimés directement sur l'écran du navigateur. Ce type d'injection peut souvent être utilisé pour énumérer une base de données entière. 


**Union-Based SQL Injection** : 
    Ce type d'injection utilise l'opérateur SQL UNION avec une instruction SELECT pour renvoyer des résultats supplémentaires à la page. Cette méthode est le moyen le plus courant d'extraire de grandes quantités de données par le biais d'une vulnérabilité d'injection SQL.

**Blind SQLi - Authentification Bypass**
    Se produit lorsque nous n'obtenons que peu ou pas de retour d'information pour confirmer si nos requêtes injectées ont réussi ou non, car les messages d'erreur ont été désactivés, mais l'injection fonctionne quand même.
    Pour le Bypass nous voulons contourner les méthodes d'authentification telles que les formulaires de connexion. Dans ce cas, nous ne sommes pas intéressés par l'extraction de données de la base de données ; nous voulons simplement passer le formulaire de connexion.

    Exemple : L'application web demande à la base de données "avez-vous un utilisateur avec le nom d'utilisateur bob et le mot de passe bob123 ?", et la base de données répond par oui ou non (vrai/faux) et, en fonction de cette réponse, dicte si l'application web vous laisse continuer ou non.

**Blind SQLi - Boolean Based**
    Cela fait référence à la réponse que nous recevons en retour de nos tentatives d'injection. Il peut s'agir d'une réponse de type vrai/faux, oui/non, on/off, 1/0 ou de toute autre réponse qui ne peut avoir que deux résultats. Ce résultat nous confirme que notre charge utile d'injection SQL a réussi ou non. À première vue, vous pouvez avoir l'impression que cette réponse limitée ne fournit pas beaucoup d'informations.

**Blind SQLi - Time Based**
    Similaire à l'injection booléenne, en ce sens que les mêmes requêtes sont envoyées, mais qu'il n'y a pas d'indicateur visuel de l'exactitude ou de l'inexactitude de vos requêtes cette fois-ci. Au lieu de cela, l'indicateur d'une requête correcte est basé sur le temps que prend la requête pour se terminer. Ce délai est introduit par l'utilisation de méthodes intégrées telles que SLEEP(x) avec l'instruction UNION.
