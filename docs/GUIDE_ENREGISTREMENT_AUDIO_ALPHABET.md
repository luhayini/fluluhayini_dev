# Guide d'enregistrement audio — Module Alphabet du shikomori

**Projet luhayini · Campagne de collecte audio v1 · Mai 2026**

| | |
|---|---|
| **Document** | Protocole d'enregistrement audio — module alphabet |
| **Version** | 1.0 |
| **Périmètre** | 232 items : 56 symboles + 148 mots + 28 phrases |
| **Source des données** | `alphabet.module.json` v1.2.0 |
| **Destinataires** | Coordinateur de campagne + locuteurs natifs participants |
| **Licence** | CC-BY-SA 4.0 (mêmes termes que le module alphabet) |

---

## 0. À lire en premier (résumé d'une page)

Nous constituons une base de prononciations audio pour le module d'apprentissage de l'alphabet du shikomori. Chaque enregistrement sera **rattaché automatiquement** à un symbole, un mot ou une phrase déjà identifié dans notre base de données. Pour que ce rattachement fonctionne sans erreur, **le nom de chaque fichier doit suivre une convention stricte** et un fichier `manifest.csv` doit accompagner la livraison.

Le principe tient en cinq points :

1. Chaque item à enregistrer possède un **identifiant stable** (l'« ID ») défini dans le module alphabet — par exemple `sym_a` (le son « a »), `wrd_mwana` (le mot « enfant »), `phr_jeje` (la salutation « Jeje ! »). Cet ID ne change jamais et c'est lui qui relie un fichier audio à son entrée dans l'application.

2. Chaque locuteur enregistre **les 232 items**, dans **son propre dialecte**. Plusieurs locuteurs enregistrent les mêmes items : c'est voulu, cela donne une variété de voix et couvre les quatre parlers de l'archipel.

3. Chaque fichier livré est nommé selon la formule : `ID__dialecte__locuteur__prise.extension` — voir la section 7.

4. Deux versions de chaque enregistrement sont livrées : un fichier **WAV** (archive de qualité maximale) et un fichier **MP3** (version diffusée dans l'application).

5. La livraison comprend les fichiers audio **plus deux fichiers de métadonnées** : `manifest.csv` (un inventaire de tous les enregistrements) et `speakers.csv` (la fiche de chaque locuteur). Sans ces deux fichiers, les audios ne peuvent pas être intégrés.

Le reste du document détaille chacun de ces points. Le coordinateur de campagne lit l'intégralité du guide ; un locuteur peut se concentrer sur les sections 4 à 13.

---

## 1. Objectif et contexte

Le projet luhayini développe une plateforme pour la langue comorienne (shikomori). Le **module alphabet** enseigne les 56 unités graphiques de l'orthographe officielle (norme du décret présidentiel du 12/12/2009, version révisée 2019). Chaque unité est illustrée par des mots et des phrases d'exemple.

Aujourd'hui, le module est entièrement textuel. Cette campagne vise à lui ajouter la **dimension sonore** : permettre à un apprenant d'entendre la prononciation authentique de chaque lettre, de chaque mot et de chaque phrase, par des locuteurs natifs.

Les enregistrements ont deux usages :

- **Pédagogique** — un bouton « écouter » sur chaque symbole, mot et phrase de l'application.
- **Patrimonial et scientifique** — la constitution d'un corpus oral documenté du shikomori, exploitable pour la recherche linguistique et, à terme, l'entraînement d'outils de traitement automatique de la parole.

C'est pourquoi la qualité d'archive (fichiers WAV) compte autant que la version diffusée.

---

## 2. Ce que vous allez enregistrer

La campagne couvre l'**intégralité** du module, soit **232 items** répartis en trois catégories :

| Catégorie | Quantité | Préfixe d'ID | Exemple |
|---|---|---|---|
| **Symboles** (lettres et sons de l'alphabet) | 56 | `sym_` | `sym_a`, `sym_dr`, `sym_mb_implosive` |
| **Mots** d'exemple | 148 | `wrd_` | `wrd_mwana`, `wrd_papa_requin` |
| **Phrases** d'exemple | 28 | `phr_` | `phr_jeje`, `phr_proverb_maji_ya_jana` |

La liste exhaustive des 232 items, avec leur ID, leur forme écrite, leur transcription phonétique et leur traduction française, figure en **Annexe A**. C'est cette liste qui sert de feuille de route à chaque locuteur.

**Plusieurs voix par item.** Chaque locuteur du groupe enregistre la totalité des 232 items. Un même item — disons `wrd_mwana` — sera donc enregistré par plusieurs personnes. C'est l'objectif : la base de données accepte plusieurs enregistrements par item, et la diversité des voix (genres, âges, dialectes) enrichit autant l'apprentissage que le corpus.

---

## 3. Les deux rôles de la campagne

**Le coordinateur** (une personne de l'équipe luhayini) : recrute les locuteurs, leur attribue un identifiant (`speaker_slug`), leur transmet ce guide et la liste des items, prépare le `manifest.csv` pré-rempli, recueille et vérifie les livraisons, puis lance l'intégration en base de données. Le coordinateur lit tout le document.

**Le locuteur** : une personne dont le comorien est la langue maternelle (ou de très bon niveau natif), qui réalise les enregistrements dans son dialecte. Le locuteur lit les sections 4 à 13 et s'appuie sur l'Annexe A.

Un groupe de **2 à 6 locuteurs** est visé pour cette première campagne. L'idéal est d'avoir au moins un locuteur par dialecte représenté.

---

## 4. Avant de commencer : matériel et environnement

**Matériel.** Un enregistrement de bonne qualité ne demande pas de studio, mais quelques précautions :

- Un **micro externe** (micro-cravate USB, micro de podcast, ou casque-micro de qualité) est nettement préférable au micro intégré d'un ordinateur portable. Un smartphone récent tenu à 20–30 cm de la bouche donne aussi de bons résultats.
- Un logiciel d'enregistrement permettant d'**exporter en WAV et en MP3** : Audacity (gratuit, Windows/Mac/Linux) est recommandé. Sur smartphone, une application d'enregistrement « dictaphone » de qualité suffit pour le MP3 ; le WAV peut alors être généré par le coordinateur.

**Environnement.** La salle compte plus que le matériel :

- Choisir une pièce **calme et peu réverbérante** : éviter les pièces vides et carrelées (écho). Une chambre avec rideaux, tapis et lit absorbe bien le son.
- Couper toute source de bruit : ventilateur, climatisation, télévision, notifications du téléphone, fenêtre sur rue.
- Enregistrer **à distance constante** du micro (la garder identique pour tous les items).
- Faire un **test de 10 secondes** avant de commencer, l'écouter au casque, vérifier qu'il n'y a ni souffle excessif, ni écho, ni saturation.

---

## 5. Consentement et éthique

La voix est une donnée personnelle. Avant tout enregistrement, chaque locuteur doit donner un **consentement éclairé** : il accepte que ses enregistrements soient intégrés à la plateforme luhayini, diffusés publiquement dans un but pédagogique, et conservés dans un corpus sous licence **CC-BY-SA 4.0**.

Le coordinateur fait remplir et dater un formulaire de consentement (papier ou numérique) avant la campagne. La **date du consentement** est ensuite reportée dans le fichier `speakers.csv` (colonne `consent_given_at`). Un locuteur peut rester **anonyme** : il fournit alors un pseudonyme comme nom d'affichage, et aucune donnée identifiante n'est conservée.

Aucun enregistrement de **mineur** n'est intégré sans le consentement écrit d'un représentant légal.

---

## 6. Spécifications techniques des fichiers

Chaque item donne lieu à **deux fichiers** portant le même nom de base, l'un en `.wav`, l'autre en `.mp3`.

**Fichier WAV — archive de référence**

| Paramètre | Valeur |
|---|---|
| Format | WAV (PCM non compressé) |
| Fréquence d'échantillonnage | 48 000 Hz (48 kHz) — 44,1 kHz accepté |
| Profondeur | 24 bits (16 bits accepté) |
| Canaux | **Mono** (1 canal) |

**Fichier MP3 — version diffusée**

| Paramètre | Valeur |
|---|---|
| Format | MP3 |
| Débit | 192 kbit/s (CBR) |
| Fréquence d'échantillonnage | 48 kHz (identique au WAV) |
| Canaux | **Mono** (1 canal) |

**Règles communes à tous les enregistrements**

- **Mono obligatoire.** Une voix unique n'a pas besoin de stéréo, et le mono allège les fichiers.
- **Un item = un fichier.** Ne jamais regrouper plusieurs mots ou plusieurs symboles dans un même fichier.
- **Silence de cadrage.** Laisser environ **0,3 à 0,5 seconde de silence** au début et à la fin de chaque fichier — ni plus (le lecteur paraîtrait lent à démarrer), ni moins (le son serait coupé).
- **Niveau sonore.** Viser une crête entre **−6 et −3 dBFS**. Le signal doit être bien audible mais **jamais saturé** (pas de « clipping », pas de distorsion).
- **Pas de traitement.** Aucun ajout de musique, de réverbération, d'effet ou d'habillage. Un léger nettoyage du bruit de fond est toléré s'il ne dégrade pas la voix.
- **Durées indicatives** : un symbole 1 à 2 s, un mot 1 à 3 s, une phrase 2 à 6 s. Ce ne sont que des repères.

---

## 7. Convention de nommage des fichiers

C'est la règle **la plus importante** du guide. Le nom de fichier encode à lui seul tout ce dont le système a besoin pour rattacher l'audio au bon item.

### 7.1 La formule

```
{ID}__{dialecte}__{locuteur}__{prise}.{extension}
```

Les champs sont séparés par un **double tiret bas** (`__`, deux caractères `_`).

| Champ | Description | Valeurs |
|---|---|---|
| `ID` | L'identifiant exact de l'item, copié depuis l'Annexe A | `sym_a`, `wrd_mwana`, `phr_jeje`, ... |
| `dialecte` | Le code du dialecte du locuteur | `ng`, `nz`, `mw`, `ma` (voir section 12) |
| `locuteur` | Le `speaker_slug` attribué par le coordinateur | `spk_ahmed_001`, `spk_fatima_002`, ... |
| `prise` | Le numéro de prise, sur 2 chiffres | `01` (par défaut), `02`, `03`, ... |
| `extension` | Le format du fichier | `wav` ou `mp3` |

### 7.2 Exemples corrects

```
sym_a__ng__spk_ahmed_001__01.wav
sym_a__ng__spk_ahmed_001__01.mp3
sym_b_implosive__nz__spk_fatima_002__01.wav
wrd_mwana__mw__spk_ahmed_001__01.wav
phr_proverb_maji_ya_jana__ma__spk_said_003__02.mp3
```

Le fichier WAV et le fichier MP3 d'un même enregistrement ont **exactement le même nom de base** — seule l'extension diffère. C'est indispensable pour que le système les reconnaisse comme les deux versions d'une même prise.

### 7.3 Pourquoi le double tiret bas

Les identifiants contiennent eux-mêmes des tirets bas simples (`sym_b_implosive`, `wrd_papa_requin`, `phr_proverb_maji_ya_jana`). Le séparateur de champs est donc un **double** tiret bas : il reste sans ambiguïté. Pour lire un nom de fichier, on le découpe sur `__` et on obtient toujours exactement quatre champs.

### 7.4 Règles strictes

- **Tout en minuscules.** Pas de majuscules dans le nom de fichier.
- **Pas d'accents, pas d'espaces, pas de caractères spéciaux.** Uniquement des lettres non accentuées, des chiffres et le tiret bas.
- **Ne jamais modifier un ID.** L'ID est copié tel quel depuis l'Annexe A. Une faute de frappe dans l'ID rend l'enregistrement inutilisable.
- **Numéro de prise sur deux chiffres** : `01`, pas `1`.
- En cas de doute, le coordinateur fournit le `manifest.csv` **déjà pré-rempli** avec tous les noms de base attendus : il suffit alors de nommer les fichiers à l'identique.

### 7.5 Ce qu'il ne faut PAS faire

```
Sym_A__ng__spk_ahmed__01.wav      ← majuscules
wrd mwana_ng_ahmed_1.wav          ← espaces, séparateur simple, prise à 1 chiffre
phr_jeje-ng-ahmed-01.mp3          ← tirets simples au lieu de __
mwana.wav                         ← aucun ID, aucune métadonnée
sym_à__ng__spk_ahmed_001__01.wav  ← caractère accentué
```

---

## 8. Structure des dossiers à livrer

Chaque locuteur livre **un dossier unique** portant son `speaker_slug`, organisé ainsi :

```
spk_ahmed_001/
├── speaker_info.txt          (facultatif : notes libres du locuteur)
├── symbols/
│   ├── sym_a__ng__spk_ahmed_001__01.wav
│   ├── sym_a__ng__spk_ahmed_001__01.mp3
│   ├── sym_e__ng__spk_ahmed_001__01.wav
│   └── ... (56 symboles × 2 fichiers)
├── words/
│   ├── wrd_mwana__ng__spk_ahmed_001__01.wav
│   ├── wrd_mwana__ng__spk_ahmed_001__01.mp3
│   └── ... (148 mots × 2 fichiers)
└── phrases/
    ├── phr_jeje__ng__spk_ahmed_001__01.wav
    ├── phr_jeje__ng__spk_ahmed_001__01.mp3
    └── ... (28 phrases × 2 fichiers)
```

Le coordinateur rassemble ensuite les dossiers de tous les locuteurs, **à côté** des deux fichiers de métadonnées :

```
campagne_audio_v1/
├── manifest.csv              ← inventaire de TOUS les enregistrements
├── speakers.csv              ← fiche de TOUS les locuteurs
├── spk_ahmed_001/
├── spk_fatima_002/
└── spk_said_003/
```

Un locuteur complet livre donc 232 × 2 = **464 fichiers audio**. C'est normal.

---

## 9. Le manifeste — `manifest.csv`

Le `manifest.csv` est l'**inventaire** de la campagne : une ligne par enregistrement. Il sert de filet de sécurité (si un nom de fichier comporte une erreur, le manifeste fait foi) et porte les informations qu'un nom de fichier ne peut pas contenir (qualité, date, remarques).

Encodage **UTF-8**, séparateur **virgule**, première ligne = en-têtes.

| Colonne | Description | Exemple |
|---|---|---|
| `file_basename` | Nom du fichier **sans extension** (commun au WAV et au MP3) | `wrd_mwana__ng__spk_ahmed_001__01` |
| `target_type` | Type d'item : `SYMBOL`, `WORD` ou `PHRASE` | `WORD` |
| `target_id` | L'ID de l'item | `wrd_mwana` |
| `dialect` | Code dialecte | `ng` |
| `speaker_slug` | Identifiant du locuteur | `spk_ahmed_001` |
| `take` | Numéro de prise | `01` |
| `recording_quality` | Qualité auto-évaluée : `HIGH`, `MEDIUM` ou `LOW` | `HIGH` |
| `recorded_at` | Date d'enregistrement (AAAA-MM-JJ) | `2026-05-30` |
| `is_primary` | `true` si c'est la prise de référence à afficher par défaut pour cet item et ce dialecte, sinon `false` | `true` |
| `notes` | Texte libre : remarque, hésitation, particularité dialectale... | (vide) |

Exemple de contenu :

```csv
file_basename,target_type,target_id,dialect,speaker_slug,take,recording_quality,recorded_at,is_primary,notes
sym_a__ng__spk_ahmed_001__01,SYMBOL,sym_a,ng,spk_ahmed_001,01,HIGH,2026-05-30,true,
wrd_mwana__ng__spk_ahmed_001__01,WORD,wrd_mwana,ng,spk_ahmed_001,01,HIGH,2026-05-30,true,
phr_jeje__ng__spk_ahmed_001__01,PHRASE,phr_jeje,ng,spk_ahmed_001,01,MEDIUM,2026-05-30,true,leger bruit de fond
```

**En pratique**, le coordinateur fournit ce fichier **déjà pré-rempli** avec les colonnes `file_basename`, `target_type`, `target_id`, `dialect`, `speaker_slug` et `take`. Le locuteur (ou le coordinateur après écoute) ne complète plus que `recording_quality`, `recorded_at`, `is_primary` et `notes`.

---

## 10. La fiche locuteur — `speakers.csv`

Le `speakers.csv` décrit chaque locuteur. Une ligne par personne. Ces informations alimentent le profil de locuteur stocké en base de données et permettent de filtrer les audios (par dialecte, par genre, etc.).

Encodage **UTF-8**, séparateur **virgule**, première ligne = en-têtes.

| Colonne | Description | Valeurs |
|---|---|---|
| `speaker_slug` | Identifiant unique attribué par le coordinateur | `spk_<prenom>_<NNN>`, ex. `spk_ahmed_001` |
| `display_name` | Nom ou pseudonyme affiché publiquement | texte libre |
| `gender` | Genre auto-déclaré | `F`, `M`, `OTHER`, `UNSPECIFIED` |
| `age_range` | Tranche d'âge | `CHILD`, `TEEN`, `YOUNG_ADULT`, `ADULT`, `MIDDLE_AGED`, `SENIOR`, `UNSPECIFIED` |
| `primary_dialect` | Dialecte principal (celui des enregistrements) | `ng`, `nz`, `mw`, `ma` |
| `secondary_dialects` | Autres dialectes parlés, séparés par `;` | `nz;mw` ou vide |
| `is_native` | Le comorien est-il langue maternelle ? | `true` / `false` |
| `consent_given_at` | Date du consentement (AAAA-MM-JJ) | `2026-05-28` |
| `city` | Ville ou île d'origine (facultatif) | texte libre |
| `bio` | Courte présentation (facultatif) | texte libre |

Convention du `speaker_slug` : `spk_` + prénom en minuscules sans accent + `_` + numéro à 3 chiffres. C'est le **coordinateur** qui attribue ces identifiants, pour garantir leur unicité.

Exemple de contenu :

```csv
speaker_slug,display_name,gender,age_range,primary_dialect,secondary_dialects,is_native,consent_given_at,city,bio
spk_ahmed_001,Ahmed M.,M,ADULT,ng,nz,true,2026-05-28,Moroni,Enseignant
spk_fatima_002,Fatima,F,YOUNG_ADULT,nz,,true,2026-05-28,Mutsamudu,
spk_said_003,Saïd B.,M,SENIOR,ma,mw,true,2026-05-28,Mamoudzou,Conteur
```

---

## 11. Comment enregistrer : protocole item par item

### 11.1 Les symboles (les 56 sons de l'alphabet)

Pour un symbole, on enregistre **le son de la lettre** (le phonème), tel qu'on l'enseignerait à un enfant — et non le nom épelé de la lettre.

- **Voyelles** (`a, e, i, o, u` et leurs formes nasales) : tenir le son brièvement, environ une seconde, de façon claire et stable.
- **Consonnes simples, digraphes et mi-nasales** : prononcer le son aussi nettement que possible. Beaucoup de consonnes ne peuvent pas s'isoler parfaitement ; il est alors naturel de les appuyer sur la voyelle **« a »** (par exemple, pour le digraphe `dr`, dire « dra » ; pour la mi-nasale `mb`, dire « mba »). **Garder toujours la même voyelle d'appui « a »** pour la cohérence de la collection.
- La colonne « Indication de prononciation » de l'Annexe A donne, pour chaque symbole, un repère (souvent un mot français équivalent) et la transcription phonétique entre crochets.
- Attention aux symboles propres au shikomori : les **implosives** `ɓ` (`sym_b_implosive`) et `ɗ` (`sym_d_implosive`), les **voyelles nasales**, les **mi-nasales** (`mb`, `nd`, `ndr`...). En cas d'hésitation sur un son, se reporter au mot d'exemple associé.

### 11.2 Les mots

- Prononcer le mot **une fois**, à **débit naturel**, comme dans une conversation ordinaire — ni exagérément lent, ni précipité.
- Articuler clairement, sans détacher artificiellement les syllabes.
- Une prononciation **lente et détachée** peut être livrée en complément sous le numéro de prise `02` ; elle est facultative.
- Se fier à la **traduction française** de l'Annexe A pour lever toute ambiguïté : certains mots se ressemblent à l'écrit mais désignent des choses différentes.

### 11.3 Les phrases

- Prononcer la phrase **en entier**, d'un seul tenant, avec une **intonation naturelle**.
- Respecter la ponctuation : un point d'exclamation (« Jeje ! ») appelle un ton vif ; une question appelle une intonation montante.
- Pour les **proverbes** (`phr_proverb_...`), adopter le ton posé propre à la parole proverbiale.
- Ne pas marquer de pause exagérée entre les mots : c'est la phrase telle qu'on la dirait réellement.

### 11.4 Prises, reprises et constance

- **Une prise propre suffit** : c'est la prise `01`.
- En cas d'erreur, de toux, de bruit ou d'hésitation : **refaire**. Soit on remplace le fichier `01`, soit on garde la nouvelle version sous `02` et on indique dans le manifeste laquelle est `is_primary = true`.
- Garder une **voix, une distance au micro et un niveau constants** sur toute la session. Si possible, enregistrer les 232 items sur peu de séances rapprochées.
- Faire des **pauses** régulières : une voix fatiguée s'entend.

---

## 12. Conventions dialectales

Le shikomori se décline en quatre parlers principaux. Chaque locuteur enregistre dans **son** dialecte et l'indique par son **code à deux lettres** :

| Code | Dialecte | Île | Pays |
|---|---|---|---|
| `ng` | shiNgazidja | Grande Comore (Ngazidja) | Union des Comores |
| `nz` | shiNdzuani | Anjouan (Ndzuani) | Union des Comores |
| `mw` | shiMwali | Mohéli (Mwali) | Union des Comores |
| `ma` | shiMaore | Mayotte (Maore) | France |

Règles dialectales :

- **Chacun enregistre dans son parler natif.** Un locuteur ngazidja ne doit pas imiter un autre dialecte.
- L'ID de l'item **ne change jamais**, même si la forme prononcée varie d'un dialecte à l'autre. Si un mot se dit différemment dans votre parler (l'Annexe A signale beaucoup de ces variantes), prononcez **votre** forme et conservez l'ID indiqué — c'est précisément le code `dialecte` du nom de fichier qui enregistre cette variation.
- Certains items de l'Annexe A sont propres à un dialecte (par exemple une forme typiquement ngazidja ou typiquement maore). Si un item n'existe pas dans votre parler, **passez-le** et signalez-le dans la colonne `notes` du manifeste — ne forcez pas une prononciation artificielle.

---

## 13. Checklist qualité avant livraison

Avant de transmettre son dossier, chaque locuteur (puis le coordinateur) vérifie :

- [ ] Les **464 fichiers** sont présents : 232 items × 2 formats (WAV + MP3).
- [ ] Chaque nom de fichier suit **exactement** la convention de la section 7 (minuscules, `__`, ID exact, prise à 2 chiffres).
- [ ] Le WAV et le MP3 d'un même enregistrement portent le **même nom de base**.
- [ ] Les fichiers sont rangés dans les sous-dossiers `symbols/`, `words/`, `phrases/`.
- [ ] Tous les fichiers sont en **mono**.
- [ ] Aucun fichier n'est **saturé** ; aucun n'est quasi **silencieux**.
- [ ] Pas de bruit de fond gênant, pas d'écho marqué.
- [ ] Le silence de début/fin est court (0,3–0,5 s).
- [ ] Le `manifest.csv` couvre **toutes** les lignes et ne contient pas d'ID inconnu.
- [ ] Le `speakers.csv` contient une ligne par locuteur, avec une **date de consentement** renseignée.
- [ ] Écoute par sondage d'une dizaine de fichiers de chaque type : le bon son correspond au bon ID.

---

## 14. Ce qui se passe après la livraison

Une fois la livraison reçue, le coordinateur déclenche l'**intégration en base de données** (le « seed ») :

1. Le `speakers.csv` crée ou met à jour un **profil de locuteur** par ligne.
2. Le `manifest.csv` crée un **enregistrement audio** par ligne, rattaché à son symbole, mot ou phrase via le `target_id`, et à son locuteur via le `speaker_slug`.
3. Chaque audio entre avec le statut **« en attente de validation »** (`PENDING`).
4. Un locuteur **validateur** de confiance écoute les enregistrements et les fait passer à **« validé »** (`VALIDATED`) ou **« rejeté »** (`REJECTED`). Seuls les audios validés sont diffusés dans l'application.

Le processus est **idempotent** : relancer l'intégration ne crée pas de doublon. Une livraison corrigée peut donc être réintégrée sans risque.

---

## 15. Cas particuliers et FAQ

**Un mot se ressemble à un autre — lequel est-ce ?**
Toujours se fier à l'**ID** et à la **traduction française** de l'Annexe A, jamais à la seule graphie. Les identifiants comme `wrd_papa_requin` sont précisément conçus pour lever ces ambiguïtés.

**Je ne dis pas ce mot ainsi dans mon dialecte.**
Prononcez-le **à votre manière**. Conservez l'ID. Le code `dialecte` du nom de fichier documente la variante. Vous pouvez préciser la forme dans la colonne `notes`.

**Ce mot n'existe pas dans mon parler.**
Passez l'item et notez-le dans `notes`. Mieux vaut une absence qu'une prononciation artificielle.

**Puis-je livrer plusieurs prises d'un même item ?**
Oui : `__01`, `__02`, etc. Indiquez dans le manifeste laquelle est la prise de référence (`is_primary = true`).

**Je n'arrive à produire que le MP3, pas le WAV.**
Livrez le MP3 en respectant la convention de nommage, et signalez-le au coordinateur : il pourra générer le WAV ou enregistrer la prise comme étant en MP3 uniquement.

**Un fichier WAV est-il vraiment lourd ?**
Quelques secondes en mono ne pèsent que quelques centaines de kilo-octets. Au besoin, le WAV peut être livré en 16 bits plutôt qu'en 24 bits.

**Plusieurs locuteurs peuvent-ils partager un dossier ?**
Non. **Un dossier par locuteur**, nommé par son `speaker_slug`. Cela évite toute collision de noms de fichiers.

**Faut-il enregistrer dans l'ordre de l'Annexe A ?**
Non, l'ordre est libre. Mais cocher au fur et à mesure évite les oublis — d'où l'intérêt du `manifest.csv` pré-rempli comme feuille de route.

---

---

## Annexe A — Liste complète des 232 items à enregistrer

Chaque locuteur enregistre **tous** les items ci-dessous, dans son propre dialecte. La colonne **ID** est l'identifiant exact à reporter dans le nom de fichier et le manifeste — ne jamais le modifier.

### A.1 — Symboles (56)

#### Voyelles orales (5)

| # | ID | Lettre | API | Indication de prononciation |
|---|----|--------|-----|------------------------------|
| 1 | `sym_a` | A / a | [a] | Comme le « a » de papa, gras |
| 2 | `sym_e` | E / e | [e] | Se prononce « é » comme dans bébé, péché. Peut osciller entre « é » et « è » selon le contexte (notation de 1988). |
| 3 | `sym_i` | I / i | [i] | Comme le « i » de mini, lire |
| 4 | `sym_o` | O / o | [o] | Comme le « o » de moto, mot |
| 5 | `sym_u` | U / u | [u] | Se prononce « ou » comme dans pou, cou |

#### Voyelles nasales (5)

| # | ID | Lettre | API | Indication de prononciation |
|---|----|--------|-----|------------------------------|
| 1 | `sym_a_nasal` | Â / â | [ã] | Se prononce « an » comme dans bande, blanc |
| 2 | `sym_e_nasal` | Ê / ê | [ẽ] | Se prononce « ain » comme dans pain, main |
| 3 | `sym_i_nasal` | Î / î | [ĩ] | « i » nasalisé, comme dans îdî |
| 4 | `sym_o_nasal` | Ô / ô | [õ] | Se prononce « on » comme dans bon |
| 5 | `sym_u_nasal` | Û / û | [ũ] | « ou » nasalisé, comme dans ûdî |

#### Semi-voyelles (2)

| # | ID | Lettre | API | Indication de prononciation |
|---|----|--------|-----|------------------------------|
| 1 | `sym_w` | W / w | [w] | Comme dans oui, week-end |
| 2 | `sym_y` | Y / y | [j] | Comme dans yoyo, payer |

#### Consonnes simples (19)

| # | ID | Lettre | API | Indication de prononciation |
|---|----|--------|-----|------------------------------|
| 1 | `sym_b_implosive` | Ɓ / ɓ | [ɓ] | Consonne implosive bilabiale : on aspire l'air vers l'intérieur, contrairement au 'b' où l'air est expulsé. Inexistant en français. |
| 2 | `sym_b` | B / b | [b] | Comme en français : bébé, ballon |
| 3 | `sym_c` | C / c | [c] | Lettre rare à l'état isolé ; apparaît surtout dans la mi-nasale 'nc'. |
| 4 | `sym_d_implosive` | Ɗ / ɗ | [ɗ] | Consonne implosive dentale : on aspire l'air vers l'intérieur, contrairement au 'd' où l'air est expulsé. Inexistant en français. |
| 5 | `sym_d` | D / d | [d] | Comme en français : dans, dame |
| 6 | `sym_f` | F / f | [f] | Comme en français : feu, faim |
| 7 | `sym_g` | G / g | [g] | Toujours dur, comme dans gare, même devant 'e' ou 'i' |
| 8 | `sym_h` | H / h | [h] | Toujours expirée, comme dans l'interjection « hop ! » ou le 'h' anglais de 'hat' |
| 9 | `sym_j` | J / j | [ʒ] | Comme en français : je, jamais |
| 10 | `sym_k` | K / k | [k] | Comme en français : café, kilo |
| 11 | `sym_l` | L / l | [l] | Comme en français : la, lune |
| 12 | `sym_m` | M / m | [m] | Comme en français : maman, mère |
| 13 | `sym_n` | N / n | [n] | Comme en français : non, nuit |
| 14 | `sym_p` | P / p | [p] | Comme en français : papa, pain |
| 15 | `sym_r` | R / r | [r] | Toujours roulée, comme en espagnol ou en italien (« r » apical) |
| 16 | `sym_s` | S / s | [s] | Toujours sourde comme dans « ç » de leçon, même entre deux voyelles |
| 17 | `sym_t` | T / t | [t] | Comme en français : table, tante |
| 18 | `sym_v` | V / v | [v] | Comme en français : vous, vie |
| 19 | `sym_z` | Z / z | [z] | Comme en français : zoo, gazelle |

#### Digraphes (10)

| # | ID | Lettre | API | Indication de prononciation |
|---|----|--------|-----|------------------------------|
| 1 | `sym_dh` | DH / dh | [ð] | Comme le « th » anglais sonore de that, this — ou la lettre arabe ذ |
| 2 | `sym_dj` | DJ / dj | [dʒ] | Comme dans Djibouti — équivalent du 'j' anglais de John |
| 3 | `sym_dr` | DR / dr | [ɖ] | « d » à l'africaine : les deux lettres émises simultanément (rétroflexe). Inexistant en français. |
| 4 | `sym_dz` | DZ / dz | [dz] | Inexistant en français — version sonore de 'ts' |
| 5 | `sym_ny` | NY / ny | [ɲ] | Comme le « gn » français de pagne, signe |
| 6 | `sym_pv` | PV / pv | [β] | Comme le « v » espagnol de la vida — son bilabial fricatif |
| 7 | `sym_sh` | SH / sh | [ʃ] | Comme le « ch » français de chat ; identique au 'sh' anglais de she |
| 8 | `sym_th` | TH / th | [θ] | Comme le « th » anglais sourd de thing, three — ou la lettre arabe ث |
| 9 | `sym_tr` | TR / tr | [ʈ] | « t » à l'africaine — rétroflexe, les deux lettres émises simultanément. Inexistant en français. |
| 10 | `sym_ts` | TS / ts | [ts] | Comme dans « mouche tsé-tsé » — affriquée sourde |

#### Mi-nasales (15)

| # | ID | Lettre | API | Indication de prononciation |
|---|----|--------|-----|------------------------------|
| 1 | `sym_mb_implosive` | MƁ / mɓ | [mɓ] | Mi-nasale + implosive : pré-nasalisation suivie d'un 'ɓ' implosif |
| 2 | `sym_mb` | MB / mb | [mb] | Mi-nasale labiale : nasale + 'b' faible (souvent dans les emprunts) |
| 3 | `sym_mp` | MP / mp | [mp] | Mi-nasale labiale sourde |
| 4 | `sym_nc` | NC / nc | [nc] | Mi-nasale palatale |
| 5 | `sym_nd` | ND / nd | [nd] | Mi-nasale dentale sonore |
| 6 | `sym_ndj` | NDJ / ndj | [ndʒ] | Mi-nasale + 'dj' (affriquée sonore) |
| 7 | `sym_ndr` | NDR / ndr | [nɖ] | Mi-nasale + 'dr' rétroflexe |
| 8 | `sym_ndz` | NDZ / ndz | [ndz] | Mi-nasale + 'dz' (affriquée sonore) |
| 9 | `sym_nf` | NF / nf | [ɱf] | Mi-nasale labiodentale sourde |
| 10 | `sym_ng` | NG / ng | [ŋg] | Mi-nasale vélaire sonore — comme le 'ng' anglais suivi de 'g' |
| 11 | `sym_nk` | NK / nk | [ŋk] | Mi-nasale vélaire sourde |
| 12 | `sym_nt` | NT / nt | [nt] | Mi-nasale dentale sourde |
| 13 | `sym_ntr` | NTR / ntr | [nʈ] | Mi-nasale + 'tr' rétroflexe |
| 14 | `sym_nts` | NTS / nts | [nts] | Mi-nasale + 'ts' (affriquée sourde) |
| 15 | `sym_nv` | NV / nv | [ɱv] | Mi-nasale labiodentale sonore |

### A.2 — Mots (148)

| # | ID | Mot (forme) | API | Traduction FR | Dialecte de réf. |
|---|----|-------------|-----|---------------|-------------------|
| 1 | `wrd_papa_requin` | **papa** | [papa] | requin | shiMaore (ma) |
| 2 | `wrd_mwana` | **mwana** | [mwana] | un enfant | — toutes variantes |
| 3 | `wrd_mama` | **mama** | [mama] | maman | shiMaore (ma) |
| 4 | `wrd_maha` | **maha** | [maha] | années | — toutes variantes |
| 5 | `wrd_masiwa` | **masiwa** | [masiwa] | archipel | — toutes variantes |
| 6 | `wrd_mlozi` | **mlozi** | [mlozi] | un pêcheur | — toutes variantes |
| 7 | `wrd_jeje` | **jeje** | [ʒeʒe] | bonjour, comment ça va | shiMaore (ma) |
| 8 | `wrd_pelelo` | **pelelo** | [pelelo] | balai | — toutes variantes |
| 9 | `wrd_ewa` | **ewa** | [ewa] | oui | — toutes variantes |
| 10 | `wrd_fi` | **fi** | [fi] | poisson | shiMaore (ma) |
| 11 | `wrd_titi` | **titi** | [titi] | petit | shiMaore (ma) |
| 12 | `wrd_ziri` | **ziri** | [ziri] | des chaises | — toutes variantes |
| 13 | `wrd_kofia` | **kofia** | [kofia] | bonnet, chapeau | — toutes variantes |
| 14 | `wrd_ko` | **ko** | [ko] | viens ! | shiMaore (ma) |
| 15 | `wrd_ngozi` | **ngozi** | [ŋgozi] | peau | — toutes variantes |
| 16 | `wrd_ubu` | **ubu** | [ubu] | bouillie | — toutes variantes |
| 17 | `wrd_tu` | **tu** | [tu] | tout à fait | shiMaore (ma) |
| 18 | `wrd_jua` | **jua** | [ʒua] | soleil | — toutes variantes |
| 19 | `wrd_buyu` | **buyu** | [buju] | fruit du baobab | — toutes variantes |
| 20 | `wrd_mbuyu` | **mbuyu** | [mbuju] | baobab (l'arbre) | — toutes variantes |
| 21 | `wrd_haya` | **haya** | [haja] | allons ! | shiMaore (ma) |
| 22 | `wrd_aya` | **aya** | [aja] | verset | — toutes variantes |
| 23 | `wrd_aada` | **âda** | [ãda] | coutume | — toutes variantes |
| 24 | `wrd_ehe` | **êhê** | [ẽhẽ] | oui ! bien ! c'est ça ! | — toutes variantes |
| 25 | `wrd_idi` | **îdî** | [ĩdĩ] | fête | — toutes variantes |
| 26 | `wrd_bo` | **ɓô** | [ɓõ] | bon | — toutes variantes |
| 27 | `wrd_udi` | **ûdî** | [ũdĩ] | luth | — toutes variantes |
| 28 | `wrd_baba_papa` | **ɓaɓa** | [ɓaɓa] | papa | shiMaore (ma) |
| 29 | `wrd_banga` | **ɓanga** | [ɓaŋga] | cabane | — toutes variantes |
| 30 | `wrd_basi` | **ɓasi** | [ɓasi] | alors, eh bien | shiMaore (ma) |
| 31 | `wrd_bibiro` | **bibiro** | [bibiro] | biberon | shiMaore (ma) |
| 32 | `wrd_biro` | **biro** | [biro] | bureau | — toutes variantes |
| 33 | `wrd_daho` | **ɗaho** | [ɗaho] | maison | shiNdzuani (nz) |
| 34 | `wrd_dago` | **ɗago** | [ɗago] | maison | shiNgazidja (ng) |
| 35 | `wrd_de` | **ɗe** | [ɗe] | c'est | shiMaore (ma) |
| 36 | `wrd_dipe` | **dipe** | [dipe] | du pain | shiMaore (ma) |
| 37 | `wrd_fundi` | **fundi** | [fundi] | maître, artisan | — toutes variantes |
| 38 | `wrd_ndimu` | **ndimu** | [ndimu] | citron | — toutes variantes |
| 39 | `wrd_dhahabu` | **dhahabu** | [ðahabu] | or (métal) | — toutes variantes |
| 40 | `wrd_djahazi` | **djahazi** | [dʒahazi] | boutre (voilier traditionnel) | — toutes variantes |
| 41 | `wrd_ndjema` | **ndjema** | [ndʒema] | bonne, bien | — toutes variantes |
| 42 | `wrd_mgodro` | **mgodro** | [mgoɖo] | danse traditionnelle | shiNdzuani (nz) |
| 43 | `wrd_mirundra` | **mirundra** | [mirunɖa] | orangers | — toutes variantes |
| 44 | `wrd_ndrovi` | **ndrovi** | [nɖovi] | banane | shiNgazidja (ng) |
| 45 | `wrd_ntrovi` | **ntrovi** | [nʈovi] | banane | shiNdzuani (nz) |
| 46 | `wrd_dzina` | **dzina** | [dzina] | nom | — toutes variantes |
| 47 | `wrd_mwidzi` | **mwidzi** | [mwidzi] | un voleur | — toutes variantes |
| 48 | `wrd_ndzaya` | **ndzaya** | [ndzaja] | faim | — toutes variantes |
| 49 | `wrd_nyunyi` | **nyunyi** | [ɲuɲi] | oiseau | — toutes variantes |
| 50 | `wrd_nyungu` | **nyungu** | [ɲuŋgu] | marmite | — toutes variantes |
| 51 | `wrd_upvenya` | **upvenya** | [upβeɲa] | cligner des yeux | shiNgazidja (ng) |
| 52 | `wrd_shio` | **shio** | [ʃio] | livre | — toutes variantes |
| 53 | `wrd_vushe` | **vushe** | [vuʃe] | odeur | — toutes variantes |
| 54 | `wrd_thamani` | **thamani** | [θamani] | prix, valeur | — toutes variantes |
| 55 | `wrd_hutria` | **hutria** | [huʈia] | verser | — toutes variantes |
| 56 | `wrd_mndru_personne` | **mndru** | [mnɖu] | une personne | shiNgazidja (ng) |
| 57 | `wrd_mntru_personne` | **mntru** | [mnʈu] | une personne | shiNdzuani (nz) |
| 58 | `wrd_mutru_personne` | **mutru** | [muʈu] | une personne | shiMaore (ma) |
| 59 | `wrd_tsena` | **tsena** | [tsena] | encore, de nouveau | — toutes variantes |
| 60 | `wrd_ntsi` | **ntsi** | [ntsi] | pays | — toutes variantes |
| 61 | `wrd_gari` | **gari** | [gari] | voiture | shiMaore (ma) |
| 62 | `wrd_huhima` | **huhima** | [huhima] | se tenir debout | — toutes variantes |
| 63 | `wrd_husoma` | **husoma** | [husoma] | lire, étudier | — toutes variantes |
| 64 | `wrd_kalamu` | **kalamu** | [kalamu] | crayon, stylo | — toutes variantes |
| 65 | `wrd_lala` | **lala** | [lala] | dors ! | shiMaore (ma) |
| 66 | `wrd_na` | **na** | [na] | et, avec | shiMaore (ma) |
| 67 | `wrd_nazi` | **nazi** | [nazi] | noix de coco | — toutes variantes |
| 68 | `wrd_upepo` | **upepo** | [upepo] | vent léger, brise | — toutes variantes |
| 69 | `wrd_utiti` | **utiti** | [utiti] | petitesse | — toutes variantes |
| 70 | `wrd_vua` | **vua** | [vua] | pluie | shiMaore (ma) |
| 71 | `wrd_vao` | **vao** | [vao] | garde-robe, vêtements | — toutes variantes |
| 72 | `wrd_vavo` | **vavo** | [vavo] | là, ici | shiMaore (ma) |
| 73 | `wrd_nbuzi` | **mɓuzi** | [mɓuzi] | chèvre | — toutes variantes |
| 74 | `wrd_nfi` | **nfi** | [ɱfi] | poisson | shiNgazidja (ng) |
| 75 | `wrd_ntondoo` | **ntondoo** | [ntondoː] | morceau | shiNgazidja (ng) |
| 76 | `wrd_nkima` | **nkima** | [ŋkima] | singe | — toutes variantes |
| 77 | `wrd_bahari` | **bahari** | [bahari] | mer | — toutes variantes |
| 78 | `wrd_bingu` | **bingu** | [bingu] | ciel | — toutes variantes |
| 79 | `wrd_madji` | **madji** | [madji] | eau | shiNgazidja (ng) |
| 80 | `wrd_maji` | **maji** | [maji] | eau | shiMaore (ma) |
| 81 | `wrd_moro` | **moro** | [moro] | feu | — toutes variantes |
| 82 | `wrd_mdro` | **mdro** | [mdro] | feu | — toutes variantes |
| 83 | `wrd_juwa` | **juwa** | [juwa] | soleil | — toutes variantes |
| 84 | `wrd_mwezi` | **mwezi** | [mwezi] | lune, mois | — toutes variantes |
| 85 | `wrd_mlongo` | **mlongo** | [mlongo] | porte | — toutes variantes |
| 86 | `wrd_mlango` | **mlango** | [mlango] | porte | — toutes variantes |
| 87 | `wrd_shisiwa` | **shisiwa** | [shisiwa] | île | — toutes variantes |
| 88 | `wrd_mtsanga` | **mtsanga** | [mtsanga] | sable | — toutes variantes |
| 89 | `wrd_mbaba_papa` | **mbaɓa** | [mbaɓa] | papa | — toutes variantes |
| 90 | `wrd_mdrumume` | **mdrumume** | [mdrumume] | homme | — toutes variantes |
| 91 | `wrd_mdjeni` | **mdjeni** | [mdjeni] | étranger | — toutes variantes |
| 92 | `wrd_wandru` | **wandru** | [wandru] | des personnes | shiNgazidja (ng) |
| 93 | `wrd_shitswa` | **shitswa** | [shitswa] | tête | — toutes variantes |
| 94 | `wrd_dzitso` | **dzitso** | [dzitso] | œil | — toutes variantes |
| 95 | `wrd_dzinyo` | **dzinyo** | [dzinyo] | dent | — toutes variantes |
| 96 | `wrd_ilime` | **ilime** | [ilime] | langue (organe) | — toutes variantes |
| 97 | `wrd_ivuhu` | **ivuhu** | [ivuhu] | coude | — toutes variantes |
| 98 | `wrd_pua` | **pua** | [pua] | nez | — toutes variantes |
| 99 | `wrd_uso` | **uso** | [uso] | visage | — toutes variantes |
| 100 | `wrd_kio` | **kio** | [kio] | oreille | — toutes variantes |
| 101 | `wrd_kofu` | **kofu** | [kofu] | ongle | — toutes variantes |
| 102 | `wrd_shifuba` | **shifuba** | [shifuba] | poitrine | — toutes variantes |
| 103 | `wrd_bega` | **bega** | [bega] | épaule | — toutes variantes |
| 104 | `wrd_nyole` | **nyole** | [nyole] | cheveux | — toutes variantes |
| 105 | `wrd_roho` | **roho** | [roho] | cœur | — toutes variantes |
| 106 | `wrd_mundru` | **mundru** | [mundru] | pied, jambe | — toutes variantes |
| 107 | `wrd_moja` | **moja** | [moja] | un (1) | — toutes variantes |
| 108 | `wrd_mbili` | **mbili** | [mbili] | deux (2) | — toutes variantes |
| 109 | `wrd_traru` | **traru** | [traru] | trois (3) | — toutes variantes |
| 110 | `wrd_nne` | **nne** | [nne] | quatre (4) | — toutes variantes |
| 111 | `wrd_tsano` | **tsano** | [tsano] | cinq (5) | — toutes variantes |
| 112 | `wrd_sita` | **sita** | [sita] | six (6) | — toutes variantes |
| 113 | `wrd_saba` | **saba** | [saba] | sept (7) | — toutes variantes |
| 114 | `wrd_leo` | **leo** | [leo] | aujourd'hui | — toutes variantes |
| 115 | `wrd_meso` | **meso** | [meso] | demain | — toutes variantes |
| 116 | `wrd_vojana` | **vojana** | [vojana] | hier | — toutes variantes |
| 117 | `wrd_idjimwa` | **idjimwa** | [idjimwa] | vendredi | — toutes variantes |
| 118 | `wrd_hula` | **hula** | [hula] | manger | shiNgazidja (ng) |
| 119 | `wrd_ula` | **ula** | [ula] | manger | shiMaore (ma) |
| 120 | `wrd_hunwa` | **hunwa** | [hunwa] | boire | shiNgazidja (ng) |
| 121 | `wrd_unwa` | **unwa** | [unwa] | boire | shiMaore (ma) |
| 122 | `wrd_huona` | **huona** | [huona] | voir | shiNgazidja (ng) |
| 123 | `wrd_uona` | **uona** | [uona] | voir | shiMaore (ma) |
| 124 | `wrd_hwenda` | **hwenɗa** | [hwenɗa] | aller | shiNgazidja (ng) |
| 125 | `wrd_uendra` | **uendra** | [uendra] | aller | shiMaore (ma) |
| 126 | `wrd_dukutera` | **dukutera** | [dukutera] | docteur | — toutes variantes |
| 127 | `wrd_likoli` | **likoli** | [likoli] | école | — toutes variantes |
| 128 | `wrd_lapitali` | **lapitali** | [lapitali] | hôpital | — toutes variantes |
| 129 | `wrd_banki` | **banki** | [banki] | banque | — toutes variantes |
| 130 | `wrd_pasiporo` | **pasiporo** | [pasiporo] | passeport | — toutes variantes |
| 131 | `wrd_gato` | **gato** | [gato] | gâteau | — toutes variantes |
| 132 | `wrd_zalumeti` | **zalumeti** | [zalumeti] | allumettes | — toutes variantes |
| 133 | `wrd_karatasi` | **karatasi** | [karatasi] | papier, diplôme | — toutes variantes |
| 134 | `wrd_hazi` | **hazi** | [hazi] | travail | — toutes variantes |
| 135 | `wrd_nyama` | **nyama** | [nyama] | viande | — toutes variantes |
| 136 | `wrd_nadzi` | **nadzi** | [nadzi] | noix de coco | — toutes variantes |
| 137 | `wrd_trovi` | **trovi** | [trovi] | banane verte | — toutes variantes |
| 138 | `wrd_ndjeu` | **ndjeu** | [ndjeu] | blanc | — toutes variantes |
| 139 | `wrd_ndzidu` | **ndzidu** | [ndzidu] | noir | — toutes variantes |
| 140 | `wrd_kwezi` | **kwezi** | [kwezi] | bonjour respectueux (à un aîné) | — toutes variantes |
| 141 | `wrd_hodi` | **hodi** | [hodi] | puis-je entrer ? | — toutes variantes |
| 142 | `wrd_uhuru` | **uhuru** | [uhuru] | liberté, indépendance | — toutes variantes |
| 143 | `wrd_nvuu` | **nvuu** | [nvuu] | force | shiNgazidja (ng) |
| 144 | `wrd_mpira` | **mpira** | [mpira] | ballon | — toutes variantes |
| 145 | `wrd_nyumba` | **nyumba** | [nyumba] | maison | — toutes variantes |
| 146 | `wrd_marahaba` | **marahaba** | [marahaba] | merci, hommage | — toutes variantes |
| 147 | `wrd_kwaheri` | **kwaheri** | [kwaheri] | au revoir | — toutes variantes |
| 148 | `wrd_karibu` | **karibu** | [karibu] | bienvenue | — toutes variantes |

### A.3 — Phrases (28)

| # | ID | Phrase | Traduction FR | Contexte | Dialecte de réf. |
|---|----|--------|---------------|----------|-------------------|
| 1 | `phr_jeje` | **Jeje !** | Bonjour ! / Comment ça va ? | salutation | shiMaore (ma) |
| 2 | `phr_lala` | **Lala !** | Dors ! | imperative_command | shiMaore (ma) |
| 3 | `phr_ko` | **Ko !** | Viens ! | imperative_command | shiMaore (ma) |
| 4 | `phr_haya` | **Haya !** | Allons ! / On y va ! | interjection | shiMaore (ma) |
| 5 | `phr_ehe` | **Êhê !** | Oui ! Bien ! C'est ça ! | interjection | — toutes variantes |
| 6 | `phr_ziri_zititi` | **ziri zititi** | petites chaises | noun_phrase | — toutes variantes |
| 7 | `phr_ye_mwana` | **ye mwana** | l'enfant | noun_phrase | — toutes variantes |
| 8 | `phr_mwaha_uwo` | **mwaha uwo** | cette année | demonstrative_noun_phrase | — toutes variantes |
| 9 | `phr_nemwana` | **n'emwana** | et l'enfant | elision_example | — toutes variantes |
| 10 | `phr_ngarisomao` | **ngarisomao** | nous lisons | verb_form | shiNgazidja (ng) |
| 11 | `phr_nisila` | **Nisila** | Je mange | verb_conjugation_present | shiMaore (ma) |
| 12 | `phr_tsisila` | **Tsisila** | Je ne mange pas | verb_conjugation_negative | shiMaore (ma) |
| 13 | `phr_jeje_wanyu` | **Jeje wanyu !** | Bonjour à vous (groupe ou pluriel poli) | salutation_group | shiMaore (ma) |
| 14 | `phr_kwezi` | **Kwezi !** | Bonjour respectueux (à un aîné) | salutation_to_elder | — toutes variantes |
| 15 | `phr_wa_fetre` | **Wa fetre ?** | Ça va ? | wellbeing_question | shiMaore (ma) |
| 16 | `phr_tsa_fetre` | **Tsa fetre** | Ça va bien | wellbeing_answer | shiMaore (ma) |
| 17 | `phr_marahaba` | **Marahaba !** | Merci ! | gratitude | — toutes variantes |
| 18 | `phr_kwaheri` | **Kwaheri !** | Au revoir ! | leave_taking | — toutes variantes |
| 19 | `phr_hodi` | **Hodi !** | Puis-je entrer ? | request_entry | — toutes variantes |
| 20 | `phr_karibu` | **Karibu !** | Bienvenue ! | welcome_response | — toutes variantes |
| 21 | `phr_ya_hali` | **Ya hali !** | C'est cher ! | exclamation_price | shiMaore (ma) |
| 22 | `phr_de_waja` | **De waja** | D'accord | agreement | shiMaore (ma) |
| 23 | `phr_tsilemewa` | **Tsilemewa** | Je suis fatigué(e) | feeling_tired | shiMaore (ma) |
| 24 | `phr_nisihu_vendza` | **Nisihu vendza** | Je t'aime | emotion_love | shiMaore (ma) |
| 25 | `phr_proverb_maji_ya_jana` | **Maji ya jana tsi maji ya leo** | L'eau d'hier n'est pas celle d'aujourd'hui (autres temps, autres mœurs) | wisdom_change | — toutes variantes |
| 26 | `phr_proverb_hasira_hasara` | **Hasira hasara** | La colère est une perte (mauvaise conseillère) | wisdom_anger | — toutes variantes |
| 27 | `phr_proverb_kula_ndrege` | **Kula ndrege na mabawa zahe** | Chaque oiseau vole avec ses propres ailes (chacun avec ses moyens) | wisdom_self_reliance | — toutes variantes |
| 28 | `phr_proverb_puhu_djumbe` | **Puhu lendjia djumbe kalitsoka mfaume** | Quand un rat entre dans un palais, il ne devient pas sultan (l'origine ne change pas) | wisdom_origin | — toutes variantes |

---

## Annexe B — Pour l'équipe technique : du fichier à la base de données

Cette annexe documente la correspondance entre les livrables de la campagne et le modèle de données du backend (module alphabet v3).

**Profil de locuteur** — chaque ligne de `speakers.csv` alimente un enregistrement de locuteur, identifié de façon stable par son `speaker_slug`. Les colonnes se mappent directement : `display_name`, `gender`, `age_range`, dialecte principal et dialectes secondaires (résolus en identifiants de dialectes), `is_native`, `consent_given_at`. Les champs annexes (`city`, `bio`) vont dans les métadonnées libres.

**Enregistrement audio** — chaque ligne de `manifest.csv` alimente un *audio asset* polymorphe. Le `target_type` (`SYMBOL` / `WORD` / `PHRASE`) et le `target_id` déterminent à quelle entité l'audio se rattache : l'ID du manifeste est résolu vers la clé primaire de l'entité correspondante via son identifiant stable (`slug`). Le `speaker_slug` est résolu vers le locuteur, et le code `dialect` vers le dialecte.

**Gestion WAV / MP3** — le modèle stocke un format par enregistrement audio. La recommandation est d'**intégrer le MP3 comme média diffusable** et de **conserver le WAV en archive froide**, hors application. Le `file_basename` du manifeste permet de retrouver les deux versions. Si l'on souhaite tout de même indexer le WAV, on crée un second *audio asset* pour le même item.

**Chemin de stockage** — convention proposée pour le chemin du fichier diffusé :
`alphabet/v3/{symbols|words|phrases}/{target_id}/{file_basename}.mp3`
soit, par exemple : `alphabet/v3/words/wrd_mwana/wrd_mwana__ng__spk_ahmed_001__01.mp3`.

**Statut et validation** — tout audio intégré démarre au statut `PENDING`. Un locuteur validateur de niveau suffisant le fait passer à `VALIDATED` ou `REJECTED` ; chaque décision est tracée. L'intégration est idempotente : la clé `(target_id, speaker_slug, take, format)` identifie un enregistrement de manière unique, donc une réexécution met à jour sans dupliquer.

**Contrôles à l'intégration** — avant d'insérer, le script vérifie : que le `target_id` existe bien dans le module alphabet ; que le `target_type` correspond au préfixe de l'ID (`sym_`/`wrd_`/`phr_`) ; que le `speaker_slug` figure dans `speakers.csv` ; que le code dialecte est l'un des quatre admis ; et que les fichiers annoncés sont physiquement présents. Toute ligne en échec est rapportée sans interrompre le reste de l'intégration.

---

