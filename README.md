<div align="center">

# 🔗 Cloudflare Single Redirect

### UNE REDIRECTION. UNE CONFIGURATION. C'EST TOUT.

Un service de redirection léger, hébergé sur Cloudflare Pages et configurable depuis une interface Web.

<br>

![Cloudflare Pages](https://img.shields.io/badge/Cloudflare-Pages-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)
![Workers](https://img.shields.io/badge/Cloudflare-Workers-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)
![KV](https://img.shields.io/badge/Storage-KV-2563EB?style=for-the-badge)
![Language](https://img.shields.io/badge/Interface-Fran%C3%A7aise-334155?style=for-the-badge)

<br>

**Pas de configuration à modifier dans le code.**  
**Pas d'interface inutile. Juste ce qu'il faut.**

</div>

---

## 🖥️ L'interface

Une destination à configurer, quelques paramètres à choisir, et la redirection est prête.

<div align="center">

<img width="922" alt="Page affichée lorsque la redirection n'est pas configurée" src="https://github.com/user-attachments/assets/bbe84551-eea6-4dc9-80cb-8f4baedc07e4" />

<br>

<sub>La page affichée lorsque la redirection n'est pas encore configurée.</sub>

</div>

---

## ⚡ Ce que le projet propose

<table>
<tr>
<td width="50%">

### 🔗 Destination unique

Définissez l'URL vers laquelle vos visiteurs seront redirigés.

</td>
<td width="50%">

### ⏱️ Délai personnalisable

Choisissez un délai de 0 à 300 secondes avant la redirection.

</td>
</tr>
<tr>
<td width="50%">

### ✅ Confirmation facultative

Laissez le visiteur confirmer avant d'accéder à la destination.

</td>
<td width="50%">

### 🔐 Administration protégée

Gérez vos paramètres depuis une interface protégée par mot de passe.

</td>
</tr>
<tr>
<td colspan="2">

### 🛠️ Des erreurs expliquées directement sur le Web

Un problème de configuration ? L'application affiche un message dans le navigateur pour vous indiquer ce qu'il faut vérifier, notamment si un binding KV ou un secret est manquant.

</td>
</tr>
</table>

---

## 📸 Aperçu de l'application

<div align="center">

### 🔐 Connexion à l'administration

<img width="1153" alt="Page de connexion à l'administration" src="https://github.com/user-attachments/assets/340b1047-a055-4b17-8d43-a25041898267" />

<br>

<sub>Une page de connexion pour accéder aux paramètres de la redirection.</sub>

<br><br>

### ⚙️ Configuration de la redirection

<img width="1065" alt="Page de configuration de la redirection" src="https://github.com/user-attachments/assets/7cd4f3b5-3580-4163-b4db-2a4452d8af85" />

<br>

<sub>Configurez la destination et les options directement depuis votre navigateur.</sub>

</div>

---

## 🚀 Installation

### 01 — Télécharger

Récupérez l'archive ZIP depuis la section **Releases** du dépôt GitHub, puis décompressez-la.

### 02 — Déployer sur Cloudflare

Créez un projet Cloudflare Pages et déployez `_worker.js` avec le mode **Workers (Advanced Mode)**.

### 03 — Ajouter le stockage KV

Dans les paramètres du projet, ouvrez **Settings → Bindings** et ajoutez un binding KV.

| Paramètre | Valeur |
|:--|:--|
| Type | KV namespace |
| Nom du binding | `LINKS` |

Le nom doit être exactement `LINKS`.

### 04 — Configurer les secrets

Dans **Settings → Variables and Secrets**, ajoutez les deux secrets suivants :

| Secret | Rôle |
|:--|:--|
| `ADMIN_PASSWORD` | Mot de passe de l'administration |
| `SESSION_SECRET` | Clé secrète aléatoire d'au moins 32 caractères |

Ne publiez jamais ces valeurs sur GitHub.

### 05 — Configurer la redirection

Redéployez le projet, puis ouvrez :

`https://votre-domaine/admin`

Remplacez `votre-domaine` par le domaine de votre site.

Connectez-vous et définissez votre destination, le délai et l'éventuelle confirmation.

**C'est prêt.**

---

## 🛠️ Un problème ? Le site vous guide.

Pas besoin de commencer par chercher dans le code.

| Problème | Vérification |
|:--|:--|
| Configuration incomplète | Vérifiez les secrets et le binding KV dans Cloudflare |
| Enregistrement impossible | Vérifiez que le binding s'appelle bien `LINKS` |
| Destination absente | Configurez une URL depuis `/admin` |
| Connexion refusée | Vérifiez le mot de passe configuré |

Si le problème persiste, les journaux Cloudflare permettent d'obtenir davantage de détails techniques.

---

## ☁️ Une infrastructure Cloudflare

<div align="center">

| SERVICE | UTILITÉ |
|:--|:--|
| **Pages** | Hébergement |
| **Workers** | Exécution du code |
| **KV** | Stockage des paramètres |

</div>

Consultez la documentation officielle pour en savoir plus sur les quotas et les tarifs :

[Cloudflare Pages](https://developers.cloudflare.com/pages/) · [Workers](https://developers.cloudflare.com/workers/) · [KV](https://developers.cloudflare.com/kv/)

---

## 🔒 Sécurité

- Administration protégée par mot de passe.
- Session limitée dans le temps.
- Cookies de session configurés avec des attributs de sécurité.
- Secrets conservés dans la configuration Cloudflare.

Gardez vos identifiants confidentiels et utilisez un mot de passe robuste.

---

## 🐛 Signaler un problème

Vous avez trouvé un bug ou rencontré un problème pendant l'installation ?

Ouvrez une **Issue** sur le dépôt GitHub en précisant le message affiché et les étapes permettant de reproduire le problème.

Pensez à masquer les mots de passe, les secrets et les informations sensibles dans vos captures d'écran.

---

<div align="center">

### 🔗 Cloudflare Single Redirect

**Une seule redirection. Rien de superflu.**

<sub>Hébergé sur Cloudflare · Configuré depuis le Web</sub>

</div>
