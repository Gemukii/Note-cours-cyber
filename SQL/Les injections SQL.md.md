
- Une injection SQL, c’est une application web utilisant le langage SQL qui peut se transformer en injection SQL lorsque des données fournies par l'utilisateur sont incluses dans la requête SQL.

- Aspect : https://website.thm/blog?id=1  qui est traduit ainsi => SELECT * from blog where id=1 and private=0 LIMIT 1;

- https://website.thm/blog?id=2;--  : Le point-virgule dans l'URL signifie la fin de l'instruction SQL, et les deux tirets font que tout ce qui suit est traité comme un commentaire.