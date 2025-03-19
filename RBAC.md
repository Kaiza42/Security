# atrribution des role avec RBAC 

| Rôle        | Lire              | Écrire          | Modifier                | Supprimer         |
|------------|-------------------------|-----------------------|----------------------------------|--------------------------|
| **Utilisateur** | ✅ Voir son profil       | ❌                     | ❌                                | ❌                        |
| **Éditeur**    | ✅ Voir tous les articles | ✅ Ajouter un article  | ✅ Modifier ses propres articles | ❌                        |
| **Modérateur** | ✅ Voir tous les commentaires | ❌                 | ✅ Modifier tous les commentaires | ❌                        |
| **Admin**      | ✅ Tout voir              | ✅                     | ✅                                | ✅ Supprimer tout        |
