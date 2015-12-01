# Exemple de load balancing avec docker, haproxy et des serveur web

J'ai placé un haProxy en front qui reference les serveurs web nginx de mannière a acceder a un serveur deux fois plus qu'a un autre.

Pour l'instant j'utilise des images standard et je pose des acces au volumes pour acceder à la configuration et aux fichiers sources

```shell
curl -i [adresse ip envirronement docker]
```

L'acces à la console d'admin est bindé sur le port 9000


---

La configuration haproxy inclus maintenant une redirection d'url. Quand le serveur reçoit une url commençant par ng, la requête est redirigé vers le serveur nginx3 à la racine.
