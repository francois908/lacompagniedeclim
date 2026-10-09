# La Compagnie de Clim — page d'attente

Page temporaire en attendant le site complet. Un seul fichier, `index.html`, sans étape de compilation : chaque `push` sur `main` est déployé tel quel par Vercel.

## Ce qu'on risque de vouloir changer

Tout se trouve dans le `<script>` à la fin de `index.html`.

| Quoi | Où |
| --- | --- |
| Date visée par le décompte | `CIBLE` (présentement le début du printemps, 20 mars 2027) |
| Adresse qui reçoit les inscriptions | `COURRIEL` |
| Service qui envoie le courriel | `SERVICE` (présentement FormSubmit) |
| Google Sheet des prospects | `FEUILLE` (adresse du script Google Apps Script, finit par `/exec`) |

## Formulaire

Chaque inscription part à deux endroits en même temps :

1. [FormSubmit](https://formsubmit.co) la transmet par courriel à l'adresse `COURRIEL`.
2. Un script Google Apps Script (`FEUILLE`) l'ajoute comme nouvelle ligne dans le Google Sheet des prospects.

Le visiteur voit la confirmation dès que l'un des deux réussit.

- **Activation** : la toute première inscription envoyée depuis l'adresse en ligne déclenche un courriel d'activation de FormSubmit. Tant que le lien n'est pas cliqué, les visiteurs voient le message d'échec.
- **Si les deux envois échouent** : la page propose d'ouvrir un courriel prérempli ou de copier le message, pour ne pas perdre l'inscription.
- **Antipourriel** : un champ piège invisible (`_honey`); s'il est rempli, rien n'est envoyé.
- **Script du Google Sheet** : il vit dans la feuille (Extensions → Apps Script). Si on modifie son code, il faut le redéployer (Déployer → Gérer les déploiements → modifier → nouvelle version) pour garder la même adresse.
