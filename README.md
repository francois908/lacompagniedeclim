# La Compagnie de Clim — page d'attente

Page temporaire en attendant le site complet. Un seul fichier, `index.html`, sans étape de compilation : chaque `push` sur `main` est déployé tel quel par Vercel.

## Ce qu'on risque de vouloir changer

Tout se trouve dans le `<script>` à la fin de `index.html`.

| Quoi | Où |
| --- | --- |
| Date visée par le décompte | `CIBLE` (présentement le début du printemps, 20 mars 2027) |
| Adresse qui reçoit les inscriptions | `COURRIEL` |
| Service de formulaire | `SERVICE` (présentement FormSubmit) |

## Formulaire

Les inscriptions passent par [FormSubmit](https://formsubmit.co), qui les transmet par courriel à l'adresse `COURRIEL`.

- **Activation** : la toute première inscription envoyée depuis l'adresse en ligne déclenche un courriel d'activation de FormSubmit. Tant que le lien n'est pas cliqué, les visiteurs voient le message d'échec.
- **Si l'envoi échoue** : la page propose d'ouvrir un courriel prérempli ou de copier le message, pour ne pas perdre l'inscription.
- **Antipourriel** : un champ piège invisible (`_honey`); s'il est rempli, rien n'est envoyé.
