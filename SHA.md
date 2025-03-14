# hashage de type SHA 

| Algorithme | Taille du hachage | Sécurité | Utilisation | Remarques |nb caractère|
|------------|-------------------|----------|-------------|-----------|------------|
| SHA-1  | 160 bits          | Faible   | Obsolète, déconseillé | Vulnérable aux collisions |40|
| SHA-224| 224 bits          | Moyenne  | Utilisation limitée | Version réduite de SHA-256 |56|
| SHA-256| 256 bits          | Haute    | Très courant (certificats, signatures, blockchain) | Sécurité solide, bonne performance |64|
| SHA-384| 384 bits          | Très haute | Pour des besoins de sécurité élevés | Sécurité accrue mais plus lent |96|
| SHA-512| 512 bits          | Très haute | Applications hautement sécurisées | Très sécurisé mais plus lent |128|

le plus gros inconvénian d'un cryptage de type SHA c'est que quand tu va Hasher un mot il donneras toujours le meme resultat 

## le salage 

rajouter des élément au mot de passe aléatoire pour permettre un hashage plus sécrutiser
 pour les mot de passe il y a des salage et hashage itératif come ses trois 
```
bcrypt
PBKDF2
scrypt
```
Il faut se renseigner sur les trois la c'est interessant.