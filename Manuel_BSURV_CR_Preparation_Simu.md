# Manuel de préparation Basic Surveillance — Rôle CR
*Construit à partir des Livrets 1 à 10 (BSURV 2.0, ENAC-ATM Department). Secteur RS/RU, FL285–FL660.*

> **Note méthodologique** : ce manuel s'appuie strictement sur le contenu des 10 livrets fournis, relu intégralement pour ce document. Chaque règle importante indique le livret source entre crochets, ex. **[L3]**. Quand une information n'apparaît dans aucun livret, c'est signalé **[Non couvert par les sources]** plutôt qu'inventé. Les ajouts pédagogiques (mnémotechniques, formulations d'automatismes) sont signalés **[Conseil pédagogique]**.
>
> Ce manuel est le pendant du *Manuel CO* déjà produit. Il reprend la même architecture en 16 parties mais est **entièrement recentré sur les responsabilités, réflexes et automatismes du CR** — le contrôleur qui parle aux pilotes, résout les conflits, et exécute physiquement la séparation.

---

## SOMMAIRE

- Partie I — Fondamentaux
- Partie II — Méthodes (fiches détaillées CR)
- Partie III — Surveillance et circuits visuels
- Partie IV — Anticipation
- Partie V — Gestion des conflits et séparations
- Partie VI — Communications
- Partie VII — Priorisation et charge mentale
- Partie VIII — Situations complexes
- Partie IX — Erreurs et pièges
- Partie X — Scénarios d'entraînement personnalisés (3 niveaux + pièges)
- Partie XI — Banque de questions (+ corrigés séparés)
- Partie XII — Automatismes (arbres décisionnels compacts)
- Partie XIII — Checklists mentales
- Partie XIV — Fiche de survie CR
- Partie XV — Plan de révision priorisé
- Partie XVI — Mode entraînement interactif (simu / test blanc)

---

# PARTIE I — FONDAMENTAUX

## 1.1 Le CR dans le binôme

Le CR (Radar Controller) est, avec le CO (Planning Controller), l'un des deux contrôleurs qui gèrent une UCE. Les deux se vérifient réciproquement et communiquent de façon claire et précise **[L1]**.

**Répartition des responsabilités — ce qui définit le CR :**
- Le CR **ne modifie jamais la ligne 3** de l'étiquette (XPT, XFL, PFL, NS) : elle est du ressort exclusif du CO, qui organise les conditions de sortie **[L1]**.
- Le CR s'intéresse néanmoins pleinement à la ligne 3 (« bien au contraire ! »), tout comme le CO s'intéresse aux lignes 0–2 **[L1]**.
- Le CR est celui qui **parle aux pilotes**, exécute les résolutions (guidage, vitesse, niveau), et **assure la séparation effective** en temps réel.
- **Il relève du contrôleur (CR) d'assurer la séparation entre aéronefs** — c'est une responsabilité active, pas seulement une détection **[L9]**.

## 1.2 Sources d'information

Identiques au CO : image radar, écran secondaire (infos secteur + SEL), FDW, IHM **CHEER** (Manuel CHEER-IHM sur E-Campus pour détail exhaustif) **[L1]**.

**À RETENIR** : les outils électroniques (STCA, alarmes, DB) se nourrissent des données saisies. Une saisie fausse ou incomplète les rend inutilisables, voire dangereux **[L1]**. Le CR doit donc renseigner rigoureusement son IHM à chaque action (cap, vitesse, CFL...).

## 1.3 L'étiquette côté CR

- **Ligne 2** : AFL/CFL — le CR met à jour le **CFL** à chaque clairance délivrée. Si le vol est encore Avancé/Assumable, ce champ montre l'**EFL** (= XFL du secteur précédent), qui devient CFL à l'assume **[L1]**.
- **Ligne 3** : lue et surveillée par le CR, mais jamais modifiée par lui.
- **Ligne 4** : cap, SFL, vitesse IAS/Mach — essentielle pour le CR : c'est là qu'il consulte le cap avant tout guidage.
- **Concaténation étiquette réduite** (rappel utile au CR pour son suivi rapide) **[L2]** :

| Condition | Affichage réduit |
|---|---|
| AFL = CFL = XFL | AFL seul |
| AFL ≠ CFL | AFL + tendance + CFL (le CR doit encore surveiller l'évolution) |
| AFL/CFL ≠ EFL | AFL (+tendance) + EFL |
| AFL/CFL ≠ XFL | XFL affiché (reste une évolution à donner avant sortie) |

- **Champs h/s/r** : rappellent au CR lui-même qu'un cap (h), une vitesse (s) ou un taux (r) a été assigné par ses soins — outil de mémoire de ses propres actions **[L2]**.
- **Particularisés** utiles au CR : Vz, indicatif, XPT, XFL, Mode S (partagés avec le CO) ; ACFT, ADES, CFL, PFL, secteur suivant (locaux) **[L2]**.

## 1.4 États du vol — ce qu'ils signifient pour le CR **[L1]**

| État | Signification pour le CR |
|---|---|
| Pas concerné | Rien à faire |
| Avancé | Le CO travaille son intégration ; le CR **attend** le marqueur |
| Assumable | Vol transféré par le secteur précédent (interopérable) — pas encore à moi |
| **Assumé** | **Le vol est sur ma fréquence — je lui parle, je le contrôle** |
| Transférable | Éléments envoyés au secteur suivant |
| Transféré | Vol proposé en transfert (interopérable) |
| Assumé secteur suivant | Le vol n'est plus le mien |

## 1.5 Coordination — ce que le CR doit savoir sans l'exécuter lui-même

Deux types : **automatique** (radar, ~10 min avant entrée) et **téléphonique** (proposée/demandée) **[L1]**. Secteurs interopérables (français) : saisie immédiate visible des deux côtés. Non-interopérables (**G2 Genève, M2 Milan**) : chaque CO saisit sur sa propre interface **[L1]**.

**Règle absolue que le CR doit connaître pour savoir ce qu'il peut faire seul ou non** **[L3]** :
- **Secteur suivant a déjà reçu les éléments (XPT moutarde)** : tout changement de XFL/XPT, ou tout écart >5NM entre trajectoire et PDR prévue (ex. après un guidage) **doit être coordonné** par le CO. → **Le CR qui vient de tourner un avion doit donc vérifier si les éléments sont déjà passés, et si oui, demander au CO de coordonner avant la sortie.**
- **Secteur suivant n'a pas encore reçu les éléments** : changement de XFL possible sans coordination ; changement de XPT ou écart >5NM doit quand même être coordonné.

## 1.6 L'Agenda / Data-Blocks — l'outil de mémoire du CR

Le DB (2 à 6 vols) donne une vision chronologique des situations à venir. Le survol de l'étiquette d'un vol en DB affiche automatiquement **vecteurs vitesse et halos bleus** — cela permet au CR de **réévaluer sa résolution à chaque passage** sans tout recalculer de zéro **[L1][L3]**.

## 1.7 Vue d'ensemble : le travail du CR dans le cycle global

1. **1ère analyse CR** — démarre uniquement une fois le **marqueur CO acquitté** (jamais avant : les éléments du vol pourraient encore changer) **[L2]**.
2. **Suivi du vol** — cycle continu intégration → détection → résolution → configuration de sortie, répété à chaque retour d'attention sur le vol **[L1]**.
3. Le CR est celui qui **exécute** : phraséologie, clairances, guidage, verrouillage, transferts de fréquence.

---

# PARTIE II — MÉTHODES (fiches détaillées, côté CR)

## FICHE MÉTHODE 1 — Méthode de Travail du CR (1ère analyse et affinement)

### Objectif
Affiner et confirmer l'analyse du CO, puis prendre la responsabilité complète de la séparation active sur le vol.

### Quand l'utiliser
Dès que le marqueur de fin de 1ère analyse du CO est acquitté sur un vol **[L2][L4]**.

### Procédure détaillée (identique dans sa structure à celle du CO, mais avec un contenu spécifique CR) **[L4][L6][L8][L9]**

**Étape 1 — INTÉGRATION**
- Comme le CO, lire entièrement l'étiquette dès l'apparition en rose (ou dès que le marqueur CO est acquitté) pour prendre connaissance de toutes les informations **[L4]**.
- Pour un vol évolutif entrant : vérifier la parité du niveau demandé/prévu.

**Étape 2 — DÉTECTION (affinée)**
- Le CR **confirme et affine** la détection du CO — il ne se contente pas de la valider aveuglément.
- **Vérifier que deux avions au même FL respectent le minimum de 5NM.** Rappel : ce minimum est permis par le traitement multi-radar mono-pulse à l'ENAC ; attention à ne pas confondre le **plot (RPS)** et la **position physique réelle** — à cause de l'imprécision des systèmes, le minimum doit toujours être scrupuleusement respecté **[L4]**.
- **Cas particulier vols évolutifs** : le CR est responsable de la détection sur **TOUS les FL intermédiaires** entre le FL d'entrée (EFL) et le FL de sortie (XFL) — le CO, lui, ne détecte qu'au FL plancher **[L8][L9]**.
- **Cas particulier révision de niveau** : détecter à **chaque FL traversé** par l'évolution demandée, pas seulement au FL final **[L10]**.

**Étape 3 — CONFIGURATION DE SORTIE**
- Confirmer ou infirmer l'analyse du CO.
- Pour un vol évolutif : vérifier qu'aucun autre avion ne sort par la même route au niveau demandé.

**Étape 4 — RÉSOLUTION** *(le cœur du travail du CR — détaillée en Fiche 2)*

**Étape 5 — SUIVI DU VOL**
- Surveillance continue jusqu'au transfert, avec mise à jour régulière : « la seule façon de ne rien oublier en tant que CR est de faire son suivi de vol de façon régulière » **[L8]**.

### Points clés
- Ne jamais démarrer avant le marqueur CO acquitté.
- Toujours confirmer *soi-même* la détection, même si le CO l'a déjà faite — le CR affine, il ne recopie pas.
- Pour tout vol évolutif, penser systématiquement à étendre la détection à tous les niveaux traversés.

### Réflexe CR
**« Marqueur CO acquitté → j'intègre, je confirme/affine la détection à TOUS les niveaux concernés, j'étudie la sortie, je résous, je suis. »**

---

## FICHE MÉTHODE 2 — Résolution CR (conflits entre vols stables convergents)

### Objectif
Déterminer et exécuter la bonne solution de séparation pour deux avions stables sur routes convergentes — c'est le seul type de conflit résolu **par guidage** en BSURV **[L5]**.

### Procédure détaillée — 7 sous-étapes **[L5]**

1. **Déterminer le point de croisement.**
2. **Estimer qui arrive premier** au point de croisement et la **distance minimale de séparation**, en fonction des vitesses des avions et de l'angle des routes.
   - Méthode de calcul : mesurer la distance de chacun au point de croisement → calculer la différence → **corriger cette valeur en fonction du différentiel de vitesse** (NM gagnés/perdus par minute, multiplié par le temps restant avant le croisement) **[L3][L6]**.
   - Le point de plus grande proximité se situe **après** que le premier a franchi le point de croisement, mais **avant** que le second ne l'atteigne. Le rapprochement résiduel dépend de l'angle des routes après le croisement (plus l'angle est fermé, plus le rapprochement continue) **[L3]**.
   - **Vocabulaire : Dmini** = distance minimale de séparation **[L3]**.
3. **Déterminer le cas et le type de résolution :**

| Distance minimale estimée | Résolution |
|---|---|
| **> 15NM** | Surveillance seule |
| **Entre 5 et 15NM (certain)** | Verrouillage des caps des deux avions (sans les tourner) |
| **< 5NM ou incertitude** | Guidage : altérer le cap d'un avion + verrouiller le second (ou altérer les deux) |

4. **Élaborer la solution** à partir de l'analyse des positions/trajectoires.
5. **Décider du moment** et **exécuter** — « il n'existe pas de moment exact ni de cap parfait » ; l'essentiel est d'**anticiper** suffisamment pour avoir le temps de vérifier et corriger si besoin **[L5]**.
6. **Vérifier que la solution résout bien le conflit** (vecteurs vitesse, typiquement à 3 minutes, pour visualiser la position au point de plus grande proximité).
7. **Déverrouiller les caps** en fin de guidage, une fois l'éloignement confirmé (la distance recommence à **augmenter**, pas seulement cesse de diminuer).

### Choix de l'avion à tourner et de la direction **[L6]**
- Privilégier de tourner l'avion **en retard** au point de croisement, pour **rallonger sa trajectoire** — c'est souvent la solution la moins pénalisante.
- Choisir le sens en cohérence avec la route ultérieure de l'avion (ex. s'il tourne de toute façon à gauche plus loin sur sa route, le guider à gauche évite de lui faire perdre du temps).
- **Avion rapide vs avion lent** : à un instant donné, un **avion rapide s'écarte plus vite** de sa trajectoire initiale pour une même altération de cap qu'un avion lent. **Conséquence pratique :**
  - Tourner le **rapide** → **altération plus faible** suffit (ex. 20° au lieu de 30°) MAIS **verrouillage à maintenir plus longtemps**, sinon il risque de rattraper le lent en cas de remise en navigation trop précoce.
  - Tourner le **lent** → altération plus forte nécessaire, mais déverrouillage possible plus tôt.

### Exécution — séquence type
1. **Consultation du cap actuel** avant toute instruction : « Consultation du cap de [indicatif] : @h[XXX] ».
2. **Message de guidage** (voir Partie VI pour la phraséologie exacte).
3. **Saisie IHM en même temps que le message délivré** (cap absolu dans le menu HDG, ou « continue » via double-clic pour verrouiller sans tourner).
4. Le champ **« h »** apparaît en ligne 1 de l'étiquette, rappel visuel de l'action en cours.
5. **Vérification** : suivre que l'avion tourné suit bien l'instruction, puis que l'altération donnée est suffisante (vecteurs vitesse à ~3 min = position approximative au point de plus grande proximité).
6. **Déverrouillage** dès confirmation de l'éloignement : « resume own navigation direct [balise] » — idéalement la **balise la moins pénalisante** de la route restante.

### Contraintes vis-à-vis des secteurs adjacents **[L5]**
- Le plot d'un avion guidé **ne doit jamais s'approcher à moins de 2,5NM** (moitié du minimum radar) des frontières de secteur sans coordination préalable — si c'est le cas, demander au CO une coordination avec le secteur concerné.
- Un guidage anticipé (avion demandé tôt en fréquence) est parfois nécessaire lorsque le conflit sera trop proche de la frontière pour être résolu à temps une fois l'avion réellement entré — voir §2 « Anticipation forte » ci-dessous.

### Cas d'anticipation forte (conflit quasi-simultané) **[L6]**
Quand la différence de vitesse compense presque toute la différence de distance, les deux avions arrivent au point de croisement quasiment en même temps. Il faut alors :
- Demander l'avion **tôt en fréquence** au secteur transféreur, en précisant qu'il sera « released for [left/right] turn » dès son entrée.
- Informer immédiatement le CO pour qu'il gère la demande de transfert anticipé auprès du secteur transféreur.
- Toute modification de trajectoire à l'extérieur de RS/RU passe obligatoirement par une coordination du CO **[L5]**.

### Erreurs fréquentes
- Tourner sans consulter le cap actuel au préalable.
- Résoudre trop tard (juste avant le croisement, sans marge de vérification).
- Déverrouiller avant confirmation réelle de l'éloignement.
- Oublier de vérifier l'écart par rapport aux frontières adjacentes pendant le guidage.

### Réflexe CR
**« Croisement → qui premier / distance mini corrigée vitesse → cas (15/5NM) → agir tôt → consulter cap → instruire → saisir IHM → vérifier → déverrouiller à l'éloignement confirmé. »**

---

## FICHE MÉTHODE 3 — Résolution CR par séparation verticale (vols évolutifs)

### Objectif
Assurer la séparation entre un vol évolutif (montée/descente) et un ou plusieurs vols du secteur, **sans jamais recourir au guidage** sur le vol évolutif en BSURV **[L8]**.

### Principe
- Le CR maintient une **séparation verticale** (typiquement 1000ft, cf. Partie V) jusqu'à ce que les deux plots se soient croisés et éloignés (souvent 5NM), puis autorise la poursuite de l'évolution.
- Le choix entre anticiper une descente/montée légèrement en avance (« 2000ft en dessous/au-dessus ») ou attendre est laissé à la convenance du contrôleur : cela peut être **moins pénalisant** qu'un palier prolongé **[L9]**.

### Procédure détaillée — départ (entrant par le plancher) **[L8]**
1. Vérifier la détection du CO (limitée au FL plancher) et **étendre systématiquement la détection à tous les FL intermédiaires** jusqu'au FL de sortie prévu.
2. Étudier la configuration de sortie (aucun autre avion au même FL/route en sortie ?).
3. Clairer initialement au niveau immédiatement inférieur au trafic gênant (ex. FL280 belowFL290) tant que le conflit n'est pas résolu, en précisant la raison (« due to traffic »).
4. Si l'avion doit stabiliser un certain temps dans le secteur du dessous (RM) : demander au CO de prévenir ce secteur (palier + jusqu'à quand).
5. Une fois les plots croisés et 5NM en éloignement : autoriser la poursuite de la montée.
6. Nettoyer le DB.

### Procédure détaillée — arrivée (sortant par le plancher, LIML) **[L9]**
1. Détecter sur **tous les FL intermédiaires** entre EFL et XFL (responsabilité propre au CR).
2. **Règle du transfert avant palier** : transférer l'avion en descente **au plus tard en passant le FL310** (2000ft au-dessus du plancher FL290), pour éviter un palier lié à un changement de fréquence tardif.
3. Si un palier est malgré tout inévitable : demander au CO d'appeler **RM pour une délégation de niveau** (via la fonction IHM **« FL ? »**, après s'être assuré que RM a bien reçu les éléments — sinon utiliser **« MVT »** pour forcer l'envoi).
4. Clairer initialement 1000ft au-dessus du trafic gênant.
5. Une fois croisés et 5NM en éloignement : poursuivre la descente.
6. **RÈGLE DE SÉCURITÉ ABSOLUE : ne jamais cumuler une clairance de niveau et un transfert de fréquence dans le même message** — si le pilote comprend mal et quitte immédiatement la fréquence, aucune correction rapide n'est possible **[L9]**.
7. Transférer une fois l'avion n'interfère plus avec aucun trafic du secteur.

### FL refuge — rôle du CR **[L8]**
Quand le CO a déterminé un FL refuge (particularisé sur le XFL), le CR affine à l'appel du vol selon 3 cas :
- **Sortie > 20NM** : pas de TR, pas de FL refuge utilisé — le niveau demandé peut être donné.
- **Sortie 10-20NM, vitesses compatibles (V1≥V2)** : créer un TR par verrouillage des vitesses, pas de FL refuge utilisé.
- **Sortie < 10NM et/ou vitesses incompatibles** : **maintenir l'avion au FL refuge** ; informer le CO (qui retire le particularisé et fait la MOD nécessaire).

**Anticipation du niveau au 1er contact** : préparer mentalement, avant l'appel du pilote, le niveau qu'on lui donnera (le plus haut disponible compte tenu du trafic prévu) — à réactualiser en fonction du trafic à venir **[L8]**.

### Réaction à un nouveau vol apparaissant en cours de gestion **[L9]**
Un nouveau vol qui apparaît doit **toujours** déclencher une remise à jour complète de l'analyse déjà faite (même si un conflit semblait écarté) — appliquer de nouveau sa méthode de travail : « l'apparition d'un nouveau vol peut tout changer ! »

### Réflexe CR — vols évolutifs
**« Je détecte à TOUS les niveaux intermédiaires. Jamais de guidage sur un évolutif — que de la séparation verticale. Transfert avant FL310 en descente. Jamais clairance + fréquence dans le même message. »**

---

## FICHE MÉTHODE 4 — Exécution du Transfert sous Séparation Radar (TR)

### Objectif
Transférer deux avions suivant la même route/FL en garantissant une séparation par vitesse plutôt que par une nouvelle analyse complète côté secteur suivant.

### Deux cas **[L7]**
1. **> 20NM au transfert** : « séparation réduite » — pas de verrouillage vitesse obligatoire, pas de coordination téléphonique nécessaire (selon LOA).
2. **< 20NM** : **transfert sous séparation radar**. Condition impérative : **verrouillage des vitesses**, avec **V(1er) ≥ V(2ème)**. Transferts de communication effectués « de façon rapprochée ».

### LOA à connaître **[L7]**
| Secteur adjacent | Modalités | Séparation min. |
|---|---|---|
| Genève (G2/LSAG) | Coordination téléphonique obligatoire | 10NM |
| Milan (M2/LIMM) | Coordination téléphonique obligatoire | 10NM |
| Bordeaux (LFBB) | Transfert radar silencieux | 10NM |
| Même centre (ENAC) | Transfert radar silencieux | 10NM |

### Procédure d'exécution CR
1. Détecter deux avions sur même route/FL, mesurer la distance.
2. **Vérifier/obtenir les points de Mach** des deux avions — demander en fréquence si besoin : *« [indicatif], what would be your Mach number at requested FL? »*.
3. Vérifier **V1 ≥ V2** et la distance requise par la LOA du secteur suivant.
4. Selon interopérabilité :
   - **Secteur interopérable et silencieux** (LFBB ou intra-ENAC) : exécuter directement le verrouillage.
   - **Secteur non-interopérable (G2/M2)** ou coordination requise : demander au CO d'appeler, en lui transmettant **indicatifs, position, FL, distance entre les deux, points de Mach**.
5. Une fois l'accord obtenu (ou si silencieux d'emblée) : **verrouiller les vitesses des deux avions**, mettre à jour le champ **S** de l'étiquette en même temps que le message.
6. **Transfert de communication rapproché** entre les deux avions (l'un juste après l'autre).
7. En sortie, **lever la restriction de vitesse** dès que la configuration le permet (ex. divergence de route confirmée) — bouton RESUME dans le menu Speed.
8. Transférer chaque avion en fréquence après collationnement correct.

### Cas particulier : révision de niveau créant un TR **[L7]**
Si une demande de montée/descente rapproche un avion à <20NM d'un autre déjà transféré : informer le CO, qui coordonne en précisant que l'évolution **crée** un TR (même silencieux).

### Refus obligatoire **[L7]**
Pour une demande de changement de FL à l'intérieur de RS/RU : si la vitesse du second avion serait supérieure à celle du premier, **ou** si la distance ne respecte pas la LOA, **le CR doit refuser** la demande.

### Erreurs fréquentes
- Accepter un TR sans avoir vérifié V1≥V2.
- Oublier de mettre à jour le champ S en même temps que le message.
- Lever la restriction de vitesse trop tôt, avant divergence confirmée.
- Transférer sans vérifier que la distance en sortie respecte toujours la LOA du secteur suivant (après un guidage ou une évolution).

### Réflexe CR — TR
**« <20NM ? → V1≥V2 ? → interopérable/silencieux ? sinon coordonner via mon CO → verrouiller + S à jour → transfert rapproché → lever dès divergence confirmée. »**

---

# PARTIE III — SURVEILLANCE ET CIRCUITS VISUELS (côté CR)

## 3.1 Principe
Chaque étape de la méthode a son propre circuit visuel **[L2]** ; le CR applique les mêmes circuits que le CO pour intégrer/détecter/étudier la sortie, puis y ajoute le circuit de **vérification d'exécution** propre à la résolution.

| Étape | Circuit visuel |
|---|---|
| Intégration | Lecture complète étiquette + FDW |
| Détection | Balayage **latéral et longitudinal** des flux — **étendu à tous les FL intermédiaires pour un vol évolutif** |
| Configuration de sortie | Remontée des flux convergents depuis le XPT |
| **Résolution (spécifique CR)** | Vérification post-action : cap suivi ? altération suffisante ? distance qui évolue comme prévu (vecteurs vitesse) ? |

## 3.2 Zones de travail RS/RU (mêmes repères que le CO) **[L3]**
1. **LTP** — partie est.
2. **GRENA-BOSUA** — point de conflit + interface M2.
3. **MTL** — point de conflit + partie sud.
4. **MEN** — partie ouest.
5. **MINDI** — nord-ouest.
6. **LSE** — point de conflit + partie nord.

Points de conflit principaux : **MTL, GRENA, LSE** **[L2]**.

## 3.3 Cycle continu de suivi — vu côté CR

Le circuit est **continu** : une fois terminé, il reprend automatiquement depuis le début **[L3]**. Pour le CR, les questions typiques par état de vol :

| État du vol | Questions CR |
|---|---|
| **En fréquence (blanc)** | Le vol évolue-t-il comme prévu ? Est-ce que je dois coordonner ou faire une MOD ? Quand ? |
| **Proche de sortie (blanc/moutarde)** | Le contrat de sortie sera-t-il rempli ? Stable ? Établi sur son XPT ? À moins de 5NM de la route ? Coordination nécessaire ? |

**Rappel automatique via DB** : survol de l'étiquette → vecteurs vitesse + halos bleus des vols concernés, permettant de réévaluer sans tout recalculer **[L3]**.

## 3.4 Surveillance active pendant l'exécution
- **Vérifier constamment** que les avions suivent la navigation autorisée. Écart constaté → *« [indicatif], you are to the left/right of your track, resume navigation direct [balise] »* **[L6][L10]**.
- Une étiquette avec **CFL ≠ XFL persistant** signale qu'une action reste due (MOD ou nouvelle clairance). **Au moment du transfert de communication, il faut toujours avoir XFL = CFL** **[L8]**.
- **La seule façon de ne rien oublier en tant que CR est de faire son suivi de vol de façon régulière** — ne pas se fier uniquement à la mémoire d'un conflit isolé **[L8]**.

---

# PARTIE IV — ANTICIPATION (côté CR)

## 4.1 Principes extraits des sources

- **Anticiper la mise en œuvre d'une résolution** pour avoir le temps de vérifier son efficacité et corriger si besoin — pas de « moment exact » ni de « cap parfait » **[L5]**.
- **Anticiper les demandes pilotes** (niveau de croisière probable) : préparer mentalement la réponse avant même l'appel **[L8]**.
- **Anticiper un conflit trop proche de la frontière** : demander l'avion tôt en fréquence dès que l'on sait qu'il faudra agir avant l'entrée réelle **[L6]**.
- **Anticiper où se trouvent les points de conflit connus** (zones de travail) pour diriger l'attention avant qu'un problème n'apparaisse **[L3]**.
- **Réviser en continu** le niveau prévu pour un vol maintenu à un FL intermédiaire, à chaque nouvel avion apparaissant **[L9]**.
- **Anticiper le point de descente probable** des arrivées LIML : « aux environs de MTL » (les pilotes restent maîtres de leur profil de descente en BSURV, donc cette anticipation reste approximative) **[L9]**.

## 4.2 Exemple simple
Deux avions convergent vers GRENA, vitesses proches ; dès l'intégration, le CR calcule (distance + petit différentiel de vitesse) qu'ils passeront à quelques NM l'un de l'autre — décision de verrouillage anticipée avant même que les vecteurs vitesse ne rendent la proximité visuellement évidente.

## 4.3 Exemple complexe
Un vol en résolution verticale (arrivée LIML en descente contrainte) approche du moment de reprise de descente ; simultanément, un nouvel avion apparaît sur une route qui pourrait interférer une fois la descente reprise. Le CR doit anticiper : (1) le moment exact où le premier conflit sera résolu (croisement + 5NM), (2) si le FL initialement prévu pour la reprise de descente est toujours valable compte tenu du nouvel arrivant, (3) ajuster mentalement la suite de la clairance à donner **[L9, principe de remise à jour systématique]**.

---

# PARTIE V — GESTION DES CONFLITS ET DES SÉPARATIONS (côté CR)

## 5.1 Séparations verticales **[L3]**
- Classe C au-dessus du FL195 (France).
- **FL290–FL410 inclus : RVSM**. Minimum équipé/équipé = **1000ft**. Non équipé vs tout autre = **2000ft**.
- **Au-dessus du FL410** : 2000ft pour tous. FL pairs utilisables : 430, 450, 470, 490…
- **exW (exempté RVSM)** : halo cyan sur le RPS, confirmé en FDW. **Le CR ne doit jamais transférer un vol exW sans s'être assuré que la coordination de sortie a bien été faite** (par le CO) **[L3][L10]**.

## 5.2 Séparations horizontales **[L2][L4]**
- Minimum radar : **5NM**.
- Seuil opérationnel de détection : **<15NM** au point le plus proche = conflit à traiter (seuil empirique, non réglementaire).
- Attention plot (RPS) vs position physique réelle : toujours respecter scrupuleusement le minimum, l'imprécision système impose une marge de prudence **[L4]**.

## 5.3 Table de décision — résolution (rappel)
| Distance mini estimée | Action CR |
|---|---|
| >15NM | Surveillance |
| 5–15NM (certain) | Verrouillage caps des deux |
| <5NM ou incertitude | Guidage (tourner + verrouiller) |

## 5.4 Contraintes géographiques du guidage **[L5]**
- Le plot d'un avion guidé ne doit jamais s'approcher à **moins de 2,5NM** des frontières de secteur sans coordination.
- Toute modification de trajectoire extérieure à RS/RU passe par une coordination du CO.

## 5.5 Séparation verticale (vols évolutifs) — rappel **[L8][L9]**
- Aucun guidage sur un vol évolutif en BSURV — résolution uniquement par maintien à un FL intermédiaire jusqu'au croisement + éloignement (souvent 5NM).
- Anticiper une évolution légère (2000ft) peut être moins pénalisant qu'un guidage qui allongerait la trajectoire.

## 5.6 Urgence — STCA **[L10]**

Si le STCA (Short Term Conflict Alert) se déclenche (minimum 5NM sur le point d'être franchi, <2 min) — typiquement parce qu'une résolution planifiée n'a pas été exécutée à temps :
- **Réaction immédiate, priorité absolue sur tout le reste.**
- **Altérations de cap fortes (minimum 30°)** aux deux avions, phraséologie d'urgence :
  > *« [indicatif], immediately, turn right immediately 30° to avoid traffic »*
- Compléter avec info trafic si possible :
  > *« [indicatif], traffic 11 o'clock, 5NM »*
- Une fois la situation stabilisée : remettre chaque avion en direct sur le prochain point non pénalisant de sa route.

**Ce que ça signale** : le STCA est un filet de sauvegarde ; sa survenue trahit une résolution oubliée en amont (le plus souvent parce que l'attention était totalement absorbée par un autre conflit ou une autre surveillance) — voir Partie VII.

## 5.7 Consultation Mach et vitesse
Toujours **consulter/demander** le point de Mach avant d'imposer une contrainte de vitesse dans un TR — ne jamais supposer une valeur **[L7]**.

---

# PARTIE VI — COMMUNICATIONS (spécificités CR)

## 6.1 Principes généraux
- Le CR est le contrôleur qui **parle directement aux pilotes**. Phraséologie claire et concise ; le collationnement confirme la bonne compréhension **[L5]**.
- Les pilotes doivent collationner toute « clairance » : niveau, route/cap, transpondeur, vitesse, fréquence **[L5]**.
- **Écouter attentivement chaque collationnement** et corriger si besoin — un pilote peut se tromper de fréquence ou de niveau sans que ce soit une erreur du contrôleur **[L5]**.
- Correction : *« Negative [indicatif], contact ENAC [fréquence] »*.

## 6.2 Bibliothèque de messages CR

**Premier contact**
> PIL : « ENAC, [indicatif], good morning, [FL], [Mach] »
> CR : « [indicatif], ENAC, good morning, maintain [FL], route [X-Y], maintain Mach [.XX] or greater/less »

**Réponse temporisée (le temps de faire sa méthode)**
> CR : « Roger, I'll call you back, [indicatif] » / « Stand by… »

**Consultation de cap** (systématique avant tout guidage)
> « Consultation du cap de [indicatif] : @h[XXX] »

**Guidage**
> CR : « [indicatif], turn left/right heading [XXX] for spacing »
> CR : « [indicatif], continue present heading for spacing » *(verrouillage sans virage)*

**Déverrouillage**
> CR : « [indicatif], resume own navigation direct [balise] »

**TR — imposition de vitesse**
> CR : « [indicatif], maintain Mach [.XX] or greater/less »
> CR : « [indicatif], what would be your Mach number at requested FL? »

**Levée de restriction de vitesse**
> CR : « [indicatif], no more speed restriction »

**Vol évolutif — descente/montée contrainte**
> CR : « [indicatif], descend/climb initially [FL], due to [converging/opposite] traffic, I call you back »
> puis : CR : « [indicatif], descend/climb [FL] »
> **Jamais cumulé avec un transfert de fréquence dans le même message.**

**Transfert de fréquence** (après vérification étiquette nettoyée)
> CR : « [indicatif], contact ENAC [fréquence] »
> (radar handover) CR : « [indicatif], report Mach number to [centre] [fréquence] »

**Refus de niveau (parité)**
> CR : « [indicatif], this level is not available on your route, you must choose an odd/even level »
> ou : « would you prefer 37 or 39? » — **éviter d'énoncer les trois chiffres complets d'un niveau dans une contre-proposition** pour ne pas laisser croire à une clairance **[L10]**.

**Urgence STCA**
> CR : « [indicatif], immediately, turn right immediately 30° to avoid traffic »
> CR : « [indicatif], traffic 11 o'clock, 5NM »

**Écart de trajectoire**
> CR : « [indicatif], you are to the left/right of your track, resume navigation direct [balise] »

## 6.3 Communications CR → CO
- Informer systématiquement après toute action significative :
  > CR → CO : « [indicatif A] est en conflit à [balise] avec [indicatif B] au FL[XXX] »
- Demander une coordination externe nécessaire :
  > CR → CO : « Ask N3 if [indicatif] can climb FL[XXX]. This creates a RH with [indicatif2] [X]NM ahead, they would both be at Mach [.XX] »
- Demander un transfert anticipé :
  > CR → CO : « RS/RU. Request early transfer for [indicatif], released for left/right turn »
- Signaler un exW à coordonner en sortie, un écart de route à coordonner après guidage, une délégation de niveau nécessaire (« demande à RM un niveau plus bas dans son secteur pour [indicatif] »).

## 6.4 Préparation mentale avant de parler
- Le **cap actuel** (jamais de guidage sans consultation préalable).
- Le **niveau qu'on va donner** (anticipé avant l'appel).
- La **raison** à donner si niveau intermédiaire (« due to traffic »).
- Si une réponse doit être temporisée (« I'll call you back ») tant que la méthode n'est pas terminée.

## 6.5 Erreurs à éviter
- Répondre définitivement avant d'avoir fini sa méthode.
- Cumuler clairance + transfert de fréquence.
- Ne pas écouter le collationnement.
- Énoncer un niveau complet en trois chiffres dans une simple proposition.
- Guider sans avoir consulté le cap actuel.

---

# PARTIE VII — PRIORISATION ET CHARGE MENTALE (côté CR)

## 7.1 Principes des sources

- **Ne jamais s'arrêter au premier conflit détecté** — un conflit peut en cacher un autre **[L4]**.
- **Le suivi régulier est la seule protection contre l'oubli** : « la seule façon de ne rien oublier en tant que CR est de faire son suivi de vol de façon régulière » **[L8]**.
- **Priorité absolue à la sécurité immédiate** en cas de STCA **[L10]**.
- **Toute nouvelle apparition de vol** déclenche une remise à jour complète de l'analyse, via la méthode, par les deux contrôleurs **[L9]**.
- **Le DB est l'outil dédié** pour ne pas perdre le fil d'un conflit en cours pendant qu'on traite autre chose **[L1][L3]**.
- **Faire un tour de suivi général** avant de revenir vérifier un guidage en cours — ne pas rester focalisé sur un seul avion **[L5]**.

## 7.2 Hiérarchie pratique des priorités (CR)

1. **Sécurité immédiate** — STCA, conflit à <5NM imminent, écart de trajectoire dangereux.
2. **Exécution des résolutions déjà décidées** (guidage/verrouillage en attente d'action) — ne pas laisser une résolution planifiée non exécutée.
3. **Vérification des résolutions en cours** (le cap est-il suivi ? l'altération est-elle suffisante ?).
4. **Suivi régulier de l'ensemble du secteur** par zones de travail, y compris pendant la gestion d'un conflit ponctuel.
5. **Nettoyage des étiquettes** avant chaque transfert.

## 7.3 Revenir à une vision globale en surcharge
**[Conseil pédagogique cohérent avec les sources]** :
- Utiliser les zones de travail comme grille de balayage périodique plutôt que de rester fixé sur un avion.
- S'appuyer sur les marquages CHEER (DB, halos, Vz, particularisés, h/s/r) comme mémoire externe.
- Informer systématiquement le CO à voix haute — l'ancrage verbal renforce l'ancrage mental et partage la charge.
- Terminer une résolution engagée avant d'en démarrer une nouvelle autant que possible.

---

# PARTIE VIII — SITUATIONS COMPLEXES (côté CR)

## 8.1 Vol déjà en fréquence qui demande un changement **[L6]**
1. **Ne jamais répondre immédiatement** : « [indicatif], I'll call you back. »
2. Reprendre la méthode complète : intégrer (parité), détecter (éléments existants), étudier la sortie (MOD/coordination nécessaire ?), résoudre (accorder ou retarder), suivre.
3. Si éléments déjà passés à un secteur non-interopérable pour la sortie : le CR demande au CO une coordination téléphonique avant toute modification du XFL (alarme REV jaune tant que non acquittée).

## 8.2 Étiquette « nettoyée » avant transfert **[L5]**
Vérifier l'absence de tout marquage résiduel avant de transférer : XFL affiché en réduit (vol pas encore à son niveau de sortie), particularisés, W électroniques actifs, DB partagé, champs h/s/r actifs — **chacun signale une action encore due**.

## 8.3 Fonctions IHM utiles au CR
- **MVT** : force l'envoi des éléments à un secteur qui ne les a pas encore reçus (avant coordination/appel) **[L7][L9]**.
- **FL ?** : affiche « FL ? » chez le secteur suivant interopérable pour préparer sa réponse à une demande de délégation de niveau **[L9]**.
- **NOTEPAD** : post-it partagé (consignes ponctuelles, ex. attente ouverte) **[L10]**.

## 8.4 Relève (Handover) **[L10]**
Le CR relevé doit être capable de transmettre précisément :
- **(RS/RU)** Regroupement de secteurs.
- **État des moyens techniques** (radio, téléphone, radar — « RAS » si tout va bien).
- **Consignes/informations particulières** (ex. report de turbulence, attente à Milan).
- **Gestion du trafic** : éléments importants, conflits en cours, avions sous surveillance, avions en guidage, TR en cours, évolutions verticales à venir.
- S'assurer de l'**acceptation** de la relève par le contrôleur entrant, qui doit lui-même vérifier avoir tous les éléments avant d'accepter la responsabilité.

## 8.5 Information du Chef de Salle (CDS) **[L10]**
Une information externe (ex. ouverture d'attente) est transmise par le CO au CR via un post-it partagé. Le CR informe les pilotes concernés (« Expect hold in Milano ») ; les pilotes peuvent réduire leur vitesse par anticipation, mais aucune autre action n'est requise à cette distance.

---

# PARTIE IX — ERREURS ET PIÈGES (côté CR)

| Catégorie | Erreur | Conséquence | Comment la détecter | Comment l'éviter | Automatisme |
|---|---|---|---|---|---|
| Méthode | Démarrer sa 1ère analyse avant le marqueur CO acquitté | Travailler sur des données susceptibles de changer | Vérifier le marqueur avant de commencer | Toujours attendre le marqueur | « Marqueur coché = je peux commencer » |
| Surveillance | Ne détecter qu'au niveau final pour un vol évolutif | Conflit manqué à un niveau intermédiaire | Repasser tous les FL entre EFL et XFL | Détecter systématiquement tous les FL traversés | « Évolutif = tous les niveaux » |
| Résolution | Guider sans consulter le cap actuel | Instruction incohérente ou redondante | Comparer le cap donné au cap réel affiché | Toujours consulter avant d'instruire | « Consultation avant instruction » |
| Résolution | Déverrouiller trop tôt | Rapprochement dangereux à la remise en navigation | Vérifier que la distance **augmente**, pas seulement cesse de diminuer | Attendre confirmation nette de l'éloignement | « Éloignement confirmé, pas juste stable » |
| Communication | Cumuler clairance + transfert fréquence | Risque de perte de contrôle en cas de mauvaise compréhension | Relire son message avant de le donner | Toujours séparer les deux instructions | « Une clairance, un message » |
| Communication | Ne pas écouter le collationnement | Erreur de fréquence/niveau non corrigée | Comparer collationnement à l'instruction | Écoute active systématique + Negative si besoin | « J'écoute chaque collationnement » |
| TR | Accorder un TR sans vérifier V1≥V2 | Risque de rattrapage entre les deux avions | Vérifier les points de Mach avant d'accepter | Toujours demander/consulter le Mach | « Vitesse vérifiée avant TR » |
| Priorisation | Rester focalisé sur un guidage en cours sans tour de suivi général | Oubli d'un autre conflit, d'un transfert | Depuis quand n'ai-je pas balayé tout le secteur ? | Refaire un tour complet avant de revenir au guidage | « Guidage en cours ≠ secteur en pause » |
| Coordination | Transférer un avion exW sans confirmation de coordination | Le secteur suivant refuse ou n'est pas informé | Vérifier avant transfert : avion exW ? | Toujours vérifier avant chaque transfert exW | « exW = coordination confirmée avant transfert » |
| Oubli d'étape | Transférer sans nettoyer l'étiquette | Danger potentiel pour le secteur suivant | Repasser : W off ? DB supprimé ? XFL=CFL ? h/s/r ? | Checklist pré-transfert systématique | « Étiquette propre avant transfert » |
| Stress/surcharge | Oublier une résolution planifiée jusqu'au STCA | Urgence, guidage brutal à 30° | STCA se déclenche | S'appuyer systématiquement sur le DB comme rappel | « Le DB porte ma mémoire, pas moi seul » |
| Frontières | Laisser un plot guidé s'approcher à moins de 2,5NM d'une frontière sans coordination | Conflit potentiel avec le secteur adjacent | Mesurer la distance du plot à la frontière pendant le guidage | Vérifier systématiquement pendant tout guidage proche d'une limite | « 2,5NM = seuil de coordination frontière » |

---

# PARTIE X — SCÉNARIOS D'ENTRAÎNEMENT PERSONNALISÉS (côté CR)

## Niveau 1 — Fondamentaux (une seule difficulté à la fois)

### Scénario 1.1 — Résolution simple par verrouillage
**Situation** : Vous êtes CR. Le CO vous informe qu'un conflit <15NM existe entre deux avions stables convergents ; vous estimez la distance minimale à 10NM.
**Ce que vous devez faire** : simplement verrouiller les caps des deux avions (« continue present heading for spacing » sur chacun), sans les tourner. Vérifier avec les vecteurs vitesse. Déverrouiller dès l'éloignement confirmé.
**Piège** : tourner un avion alors qu'un simple verrouillage suffisait — résolution disproportionnée, pénalise inutilement le vol.

### Scénario 1.2 — Vol en fréquence demandant un changement
**Situation** : Vous êtes CR. DAH452, déjà en fréquence, demande un changement de FL.
**Ce que vous devez faire** : répondre « I'll call you back », reprendre entièrement la méthode (intégrer/parité, détecter, étudier sortie, résoudre), puis répondre définitivement.
**Piège** : accorder la demande immédiatement sans reprendre la méthode complète.

### Scénario 1.3 — TR simple silencieux
**Situation** : Vous êtes CR. RAM151 et TAP826 volent sur la même route au même FL, à 11NM de distance ; le secteur suivant est intra-ENAC.
**Ce que vous devez faire** : vérifier les points de Mach, condition V1≥V2, verrouiller les vitesses directement (transfert silencieux, pas de coordination téléphonique requise), transférer en fréquence rapprochée.
**Piège** : oublier de mettre à jour le champ S de l'étiquette en même temps que le message.

## Niveau 2 — Intermédiaire (plusieurs éléments simultanés)

### Scénario 2.1 — Guidage avec fort différentiel de vitesse et frontière proche
**Situation** : Vous êtes CR. TAR156 (rapide, venant de loin) et FGCAD (lent, venant de MAJOR) convergent à MTL avec une différence de distance de 23NM presque entièrement compensée par le différentiel de vitesse — arrivée quasi simultanée.
**Ce que vous devez détecter** : la nécessité d'agir avant l'entrée réelle de FGCAD dans le secteur.
**Ce que vous devez faire** : demander au CO un transfert anticipé de FGCAD (« released for left turn »), puis guider FGCAD à gauche (cohérent avec sa route ultérieure vers MINDI/CFA).
**Variante** : et si vous choisissiez de tourner TAR156 (le rapide) à droite pour passer derrière FGCAD ? Réponse attendue : altération plus faible nécessaire (20° au lieu de 30°), mais verrouillage à maintenir plus longtemps pour éviter le rattrapage du lent à la remise en navigation.

### Scénario 2.2 — Descente contrainte + délégation de niveau
**Situation** : Vous êtes CR. Une arrivée LIML (ITY318) demande sa descente ; un trafic FGRCD au FL290 croise sa route à moins de 15NM.
**Ce que vous devez faire** : clairer initialement 1000ft au-dessus du trafic gênant (« descend initially FL300, due to converging traffic, I call you back »), puis, une fois croisés et 5NM en éloignement, poursuivre la descente. Si un deuxième palier menace, demander au CO une délégation de niveau à RM (fonction « FL ? »).
**Piège** : cumuler dans un même message la poursuite de descente et le transfert de fréquence.

### Scénario 2.3 — Vol évolutif + FL refuge
**Situation** : Vous êtes CR. ITY6478 (départ, montée demandée FL310) présente un risque de sortie <10NM avec RAM152 sur la même route/FL.
**Ce que vous devez détecter** : cas c) — distance <10NM → pas de TR, utiliser le FL refuge déterminé par le CO.
**Ce que vous devez faire** : clairer ITY6478 au FL refuge, informer le CO pour qu'il retire le particularisé et ajuste le XFL le cas échéant.
**Piège** : accorder directement le niveau demandé sans vérifier que la distance de sortie reste bien <10NM.

## Niveau 3 — Simulation test (charge élevée, événements simultanés)

### Scénario 3.1 — Conflit vertical en cours + second conflit oublié + STCA
**Situation** : Vous êtes CR. Une arrivée LIML (ITY363) est en descente contrainte par BAW451 (FL310) ; vous surveillez le moment propice pour reprendre la descente (5NM en éloignement). Simultanément, le CO vous a signalé un second conflit à MTL (EZY3203/CTM005, FL360), W électroniques activés, DB partagé.
**Évolution** : absorbé par la surveillance du premier conflit, vous oubliez de mettre en place la résolution du second. Le STCA se déclenche.
**Ce que vous devez faire** : réagir immédiatement avec des altérations de cap fortes (minimum 30°) sur les deux avions du second conflit, phraséologie d'urgence complète (« immediately, turn right immediately 30° to avoid traffic » + info trafic), puis reprendre le suivi normal, remettre chaque avion en direct sur le point non pénalisant de sa route.
**Pourquoi le piège s'est produit** : concentration excessive sur un seul conflit visuellement captivant au détriment du suivi périodique de l'ensemble du secteur.
**Variante** : et si le second conflit n'avait pas été partagé en DB ? Le risque d'oubli devient encore plus grand — d'où l'importance du DB comme filet de mémoire externe systématique.

### Scénario 3.2 — TR en cascade + demande en fréquence simultanée
**Situation** : Vous êtes CR. RAM151 apparaît, TAP826 déjà présent à 11NM sur la même route/FL — TR potentiel. Simultanément, DAH452 (déjà en fréquence) demande un changement de FL.
**Ce que vous devez faire** :
1. Répondre à DAH452 par « I'll call you back » et reprendre la méthode complète pour lui pendant que le TR se met en place.
2. Pour le TR : vérifier les points de Mach, condition V1≥V2, informer le CO de la nécessité de coordonner en sortie (secteur non-interopérable) avec les éléments requis.
3. Traiter la demande de DAH452 en parallèle sans perdre le fil du TR.
**Piège** : traiter les deux demandes dans le désordre, ou oublier l'une pendant que l'autre progresse.

### Scénario 3.3 — Sortie de crise + relève imminente
**Situation** : Vous venez de gérer un STCA (résolu). Il reste des directs à redonner, des W électroniques et DB à nettoyer sur les deux vols concernés. Une relève est prévue dans quelques minutes.
**Ce que vous devez faire** : (1) sécuriser complètement la situation (directs redonnés, DB supprimé, W désactivés), (2) reprendre une vision globale par un tour de suivi zone par zone, (3) préparer les éléments de relève, en incluant explicitement le fait qu'un STCA vient de se produire, (4) s'assurer de l'acceptation de la relève par le contrôleur entrant.
**Pourquoi c'est un piège fréquent** : la tentation de passer la main trop vite sans transmettre l'historique récent d'un événement de sécurité.

---

# PARTIE XI — BANQUE DE QUESTIONS (côté CR)

## Questions de connaissance
1. Quelles sont les 7 sous-étapes de la Résolution CR pour un conflit entre vols stables convergents ?
2. Quel est le critère de distance qui détermine le passage de la surveillance au verrouillage, puis au guidage ?
3. Pourquoi le minimum radar de 5NM est-il applicable à l'ENAC ?
4. Que doit toujours respecter la vitesse relative des deux avions dans un TR ?
5. Quelles sont les LOA de transfert sous séparation radar avec Genève, Milan, Bordeaux, et intra-ENAC ?
6. À quel FL un avion en descente doit-il être transféré au plus tard pour éviter un palier lié à un changement de fréquence tardif ?
7. Dans quel cas le CR maintient-il un avion évolutif au FL refuge plutôt que de créer un TR ?
8. Quelle distance minimale un plot guidé doit-il respecter par rapport à une frontière de secteur sans coordination ?
9. Que doit faire le CR en cas de déclenchement du STCA ?
10. Quel champ de l'étiquette le CR met-il à jour lors du verrouillage d'une vitesse dans un TR ?

## Questions de compréhension
11. Pourquoi le CR doit-il détecter sur tous les FL intermédiaires pour un vol évolutif, alors que le CO ne détecte qu'au FL plancher ?
12. Pourquoi le CR ne doit-il jamais cumuler clairance de niveau et transfert de fréquence dans un même message ?
13. Pourquoi tourner un avion rapide nécessite-t-il une altération de cap plus faible qu'un avion lent, et pourquoi le verrouillage doit-il pourtant durer plus longtemps dans ce cas ?
14. Pourquoi le CR doit-il attendre le marqueur de fin de 1ère analyse du CO avant de démarrer la sienne ?
15. Pourquoi ne peut-on déverrouiller un guidage que lorsque la distance recommence réellement à augmenter (et non simplement cesse de diminuer) ?

## Questions d'application
16. Vous êtes CR, vous estimez une distance minimale de séparation de 4NM entre deux avions convergents dans 6 minutes. Décrivez toute votre séquence d'action.
17. Vous êtes CR, une arrivée LIML doit descendre mais un trafic au FL plancher croise sa route à moins de 15NM. Décrivez votre séquence complète.
18. Vous êtes CR, deux avions à 11NM sur la même route/FL sortent vers un secteur non-interopérable (M2). Décrivez toute la procédure de TR.
19. Vous êtes CR, un vol déjà en fréquence demande un changement de FL. Que répondez-vous et que faites-vous ensuite ?
20. Le STCA se déclenche sur deux avions que vous suiviez sans résolution en place. Décrivez votre réaction immédiate et complète.

## Questions pièges
21. Vous venez de verrouiller les caps de deux avions ; la distance entre eux a cessé de diminuer. Pouvez-vous déjà déverrouiller ?
22. Un pilote collationne une fréquence légèrement différente de celle donnée. Est-ce forcément une erreur du contrôleur ?
23. Un TR silencieux (intra-ENAC) est en cours ; l'un des deux avions demande à changer de vitesse. Devez-vous vérifier quelque chose avant d'accorder ?
24. Un vol évolutif entre dans le secteur ; le CO n'a détecté aucun conflit au FL plancher. Pouvez-vous en conclure qu'aucune détection supplémentaire n'est nécessaire de votre côté ?
25. Lors d'une résolution par guidage, l'avion tourné s'approche à 3NM de la frontière du secteur adjacent. Est-ce acceptable sans action ?

## Questions type oral
26. Expliquez la différence entre « surveillance », « verrouillage » et « guidage » selon la distance minimale estimée.
27. Expliquez pourquoi V1 ≥ V2 est une condition impérative d'un TR.
28. Expliquez le rôle du champ « h » sur l'étiquette pour le CR.
29. Expliquez la règle du transfert avant FL310 pour une arrivée LIML.
30. Expliquez pourquoi le CR ne modifie jamais la ligne 3 de l'étiquette.

## Questions type simu
31. Vous êtes CR, un guidage est en cours sur un avion proche d'une frontière de secteur ; vous constatez que le plot est descendu à 2,3NM de la frontière. Que faites-vous immédiatement ?
32. Vous êtes CR, un TR est en cours et l'un des deux avions demande une descente qui le rapprocherait à moins de 20NM d'un troisième avion déjà transféré. Que faites-vous ?
33. Vous êtes CR, vous devez transférer un avion exW à un secteur adjacent. Décrivez toutes les vérifications à faire avant le transfert.

---

# CORRIGÉS — PARTIE XI

**1.** (1) Déterminer le point de croisement ; (2) estimer qui arrive premier et la distance minimale ; (3) déterminer le cas et le type de résolution ; (4) élaborer la solution ; (5) décider du moment et agir ; (6) vérifier que la solution résout le conflit ; (7) déverrouiller en fin de guidage **[L5]**.

**2.** >15NM = surveillance ; entre 5 et 15NM (certain) = verrouillage des deux caps ; <5NM ou incertitude = guidage **[L5]**.

**3.** Grâce au traitement multi-radar mono-pulse et au traitement des informations radar par le système à l'ENAC **[L4]**.

**4.** La vitesse du premier avion doit toujours être supérieure ou égale à celle du second (V1≥V2) **[L7]**.

**5.** Genève (G2) : coordination téléphonique obligatoire, 10NM. Milan (M2) : coordination téléphonique obligatoire, 10NM. Bordeaux (LFBB) : transfert radar silencieux, 10NM. Intra-ENAC : transfert radar silencieux, 10NM **[L7]**.

**6.** FL310 (2000ft au-dessus du FL plancher FL290) **[L9]**.

**7.** Quand la distance en sortie sera inférieure à 10NM et/ou que les vitesses ne sont pas compatibles (vitesse du second supérieure à celle du premier) **[L8]**.

**8.** 2,5NM (la moitié du minimum de séparation radar) **[L5]**.

**9.** Réagir immédiatement : altération de cap forte (minimum 30°) sur les deux avions, phraséologie d'urgence, information de trafic si possible, puis remise en direct une fois la situation stabilisée **[L10]**.

**10.** Le champ **S** (vitesse assignée) **[L7]**.

**11.** Parce que le CO ne détecte qu'au FL plancher lors de la 1ère analyse ; c'est au CR qu'il revient de couvrir l'ensemble du profil vertical de montée/descente, du FL d'entrée (EFL) au FL de sortie (XFL) **[L8][L9]**.

**12.** Parce que si le pilote comprend mal la clairance puis quitte immédiatement la fréquence, aucune correction rapide n'est possible — risque potentiellement extrêmement dangereux **[L9]**.

**13.** Un avion rapide s'écarte plus vite de sa trajectoire pour une même altération de cap donnée à un instant donné (moins d'altération nécessaire) ; mais étant rapide, il risque de rattraper l'avion lent une fois remis en navigation directe — d'où un verrouillage prolongé **[L6]**.

**14.** Parce que l'analyse du CO peut encore modifier des éléments du vol (ex. changement d'EFL) ; le CR ne doit pas travailler sur des données susceptibles de changer **[L2]**.

**15.** Parce qu'une distance qui a simplement cessé de diminuer ne garantit pas encore un éloignement net — un déverrouillage prématuré pourrait laisser les avions se rapprocher à nouveau si l'un d'eux tournait brutalement **[L5]**.

**16.** Confirmer le cas <5NM → choisir quel avion tourner (celui en retard, cohérence avec sa route) → consulter son cap actuel → délivrer l'instruction de guidage + verrouiller le second → saisir l'IHM en même temps → vérifier via vecteurs vitesse (~3 min) → attendre confirmation de l'éloignement net → déverrouiller les deux, remettre en direct sur la balise la moins pénalisante **[L5][L6]**.

**17.** Clairer initialement 1000ft au-dessus du trafic gênant (« descend initially FL[X], due to converging traffic, I call you back ») → surveiller le croisement → une fois croisés et 5NM en éloignement, poursuivre la descente (message séparé, jamais cumulé avec transfert fréquence) → si palier menace, demander au CO une délégation de niveau à RM (« FL ? ») → transférer au plus tard en passant FL310 **[L9]**.

**18.** Vérifier les points de Mach des deux avions, condition V1≥V2, distance suffisante selon la LOA (10NM avec M2) → informer le CO pour qu'il coordonne (indicatifs, FL, distance, Mach) car secteur non-interopérable → une fois l'accord obtenu, verrouiller les vitesses (champ S) → transfert de communication rapproché → lever la restriction dès divergence confirmée **[L7]**.

**19.** Répondre « I'll call you back » (jamais de réponse immédiate) → reprendre la méthode complète : intégrer (vérifier parité), détecter (compte tenu des éléments existants), étudier la sortie (MOD/coordination nécessaire), résoudre (accorder ou retarder selon le résultat) → répondre définitivement au pilote **[L6]**.

**20.** Réagir immédiatement, priorité absolue : altérations de cap fortes (minimum 30°) aux deux avions avec phraséologie d'urgence complète (« immediately, turn right immediately 30° to avoid traffic »), information de trafic si possible (« traffic 11 o'clock, 5NM »), puis remise en direct sur le point non pénalisant une fois la situation stabilisée **[L10]**.

**21.** Non — il faut attendre que la distance **recommence à augmenter** (éloignement net confirmé), pas simplement qu'elle ait cessé de diminuer **[L4][L5]**.

**22.** Non — ce n'est pas forcément une erreur du contrôleur ; le pilote peut avoir mal collationné. D'où l'importance d'écouter attentivement chaque collationnement et de corriger via « Negative » si besoin **[L5]**.

**23.** Oui — vérifier que le changement de vitesse ne casse pas la condition V1≥V2 imposée par le TR en cours ; sinon, refuser ou ajuster **[L7]**.

**24.** Non — le CO ne détecte qu'au FL plancher ; c'est le **CR** qui est responsable de la détection sur **tous les FL intermédiaires** entre l'entrée et la sortie **[L8][L9]**.

**25.** Non — le plot ne doit jamais s'approcher à moins de 2,5NM des frontières sans coordination préalable avec le secteur concerné **[L5]**.

**26.** Surveillance = >15NM, aucune action, juste vérifier régulièrement. Verrouillage = 5-15NM certain, on fixe les caps existants sans tourner. Guidage = <5NM ou incertitude, on altère activement le cap d'au moins un avion **[L5]**.

**27.** Pour garantir que le premier avion ne soit jamais rattrapé par le second pendant le maintien de la séparation par vitesse — condition impérative des LOA de transfert sous séparation radar **[L7]**.

**28.** Il rappelle visuellement au contrôleur (et à son collègue) qu'une action de cap (heading), vitesse (speed) ou taux (rate) a été assignée sur ce vol **[L2]**.

**29.** Un avion en descente doit être transféré au plus tard en passant le FL310 (2000ft au-dessus du plancher FL290) pour éviter qu'un changement de fréquence tardif ne provoque un palier inutile **[L9]**.

**30.** Parce que la ligne 3 (conditions de sortie) est la responsabilité exclusive du CO, qui organise ces conditions ; le CR s'y intéresse mais ne la modifie jamais **[L1]**.

**31.** Demander immédiatement au CO une coordination avec le secteur adjacent concerné, car 2,3NM est en dessous du seuil de 2,5NM **[L5]**.

**32.** Refuser la descente si elle romprait la condition de distance/vitesse du TR en cours, ou en informer le CO pour qu'il coordonne cette évolution comme créant potentiellement un nouveau TR **[L7]**.

**33.** Vérifier/confirmer que la coordination téléphonique obligatoire de sortie a bien été faite par le CO (car exW) avant tout transfert — ne jamais transférer un vol exW sans cette confirmation **[L3][L10]**.

---

# PARTIE XII — AUTOMATISMES CR (arbres décisionnels compacts)

**1ère analyse CR**
> Marqueur CO acquitté ? → NON : attendre / OUI : intégrer → détecter (affiner, tous les FL si évolutif) → étudier sortie → résoudre → suivre.

**Résolution vols stables convergents**
> Point de croisement → qui premier / distance mini corrigée vitesse → >15NM : surveillance / 5-15NM : verrouillage double / <5NM : guidage → choisir qui tourner (en retard, cohérent avec sa route, rapide=faible altération+verrouillage long / lent=forte altération+déverrouillage plus tôt) → consulter cap → instruire → saisir IHM → vérifier (VV 3min) → distance augmente ? NON : attendre / OUI : déverrouiller + nettoyer.

**Vol évolutif**
> Je détecte SUR TOUS les FL intermédiaires (jamais seulement le final) → conflit à un niveau ? → séparation verticale (jamais de guidage) → croisés + 5NM éloignement ? → NON : maintenir / OUI : autoriser poursuite → transfert en descente avant FL310 → jamais clairance+fréquence ensemble.

**TR**
> Même route/FL, distance mesurée → >20NM ? OUI : rien à faire / NON (<20NM) : Mach vérifié, V1≥V2 ? NON : refuser ou ajuster / OUI : interopérable silencieux ? OUI : verrouiller directement / NON : CO coordonne → verrouiller (S à jour) → transfert rapproché → lever dès divergence confirmée.

**Urgence STCA**
> STCA se déclenche → STOP tout le reste → 30° minimum sur les deux avions, phraséologie d'urgence → info trafic → stabilisé ? NON : surveiller intensément / OUI : remise en direct → reprendre suivi normal.

**Avant tout transfert**
> Étiquette nettoyée (W off, DB supprimé, XFL=CFL, pas de h/s/r résiduel) ? → coordination due (exW, écart>5NM après guidage) déjà faite ? → OUI aux deux : transférer / NON : compléter d'abord.

**Frontière pendant un guidage**
> Distance plot-frontière < 2,5NM ? → OUI : coordination immédiate via le CO / NON : continuer à surveiller.

---

# PARTIE XIII — CHECKLISTS MENTALES (CR)

## Checklist mentale courte (avant simu)
- [ ] Ne jamais démarrer avant le marqueur CO acquitté.
- [ ] Toujours consulter le cap actuel avant tout guidage.
- [ ] <5/5-15/>15NM = guidage/verrouillage/surveillance.
- [ ] Vol évolutif = détection sur tous les FL intermédiaires, jamais de guidage, séparation verticale uniquement.
- [ ] Jamais clairance + transfert fréquence dans le même message.
- [ ] TR : toujours vérifier V1≥V2 avant d'accorder.
- [ ] Déverrouiller seulement à l'éloignement net confirmé.
- [ ] 2,5NM = seuil de coordination frontière pendant un guidage.
- [ ] Étiquette nettoyée avant chaque transfert.
- [ ] Informer systématiquement mon CO après chaque action significative.

## « Les 30 secondes avant la simu »
1. Table de résolution en tête : >15 surveillance / 5-15 verrouillage / <5 guidage.
2. Rapide=faible altération+verrouillage long ; lent=forte altération+déverrouillage rapide.
3. TR : V1≥V2, toujours.
4. Vol évolutif = jamais de guidage, toujours séparation verticale, jamais clairance+fréquence ensemble.

## « Quand je commence à être débordé »
1. **Sécurité d'abord** : STCA ou situation <5NM imminente ? Traiter en priorité absolue.
2. Revenir aux zones de travail une par une plutôt que de sauter d'un avion à l'autre.
3. Utiliser le DB comme mémoire externe.
4. Informer mon CO à voix haute de ce qui est en cours.
5. Terminer une résolution engagée avant d'en commencer une nouvelle autant que possible.

---

# PARTIE XIV — FICHE DE SURVIE CR

**Résolution (vols stables)** : point croisement → qui premier/distance mini corrigée vitesse → >15 surveillance / 5-15 verrouillage / <5 guidage → consulter cap → instruire → saisir IHM → vérifier (VV 3min) → déverrouiller à l'éloignement net confirmé.

**Choix avion à tourner** : celui en retard, cohérent avec sa route ultérieure ; rapide = altération faible mais verrouillage long ; lent = altération forte mais déverrouillage plus tôt.

**Vols évolutifs** : je détecte SUR TOUS LES FL intermédiaires (EFL→XFL) ; JAMAIS de guidage, uniquement séparation verticale ; transfert en descente avant FL310 ; FL refuge si sortie <10NM ou vitesses incompatibles ; JAMAIS clairance+fréquence dans le même message.

**TR** : <20NM → verrouiller vitesses, V1≥V2 obligatoire ; LOA G2/M2 coordination tel. 10NM ; LFBB/intra-ENAC silencieux 10NM ; champ S à jour.

**Séparations** : radar 5NM · conflit à traiter <15NM · RVSM 1000ft (équipé/équipé) sinon 2000ft · au-dessus FL410 2000ft · frontière secteur 2,5NM pendant un guidage.

**Communication** : jamais clairance+transfert ensemble · toujours écouter collationnement · consulter cap avant instruction · informer systématiquement le CO.

**Urgence STCA** : stop tout → 30° mini sur les deux avions → info trafic → remise en direct après stabilisation.

**Avant transfert** : étiquette nettoyée (W off, DB supprimé, XFL=CFL, pas de h/s/r) + coordinations dues (exW, écart>5NM) confirmées.

**Réflexe ultime** : « J'assure la séparation, activement. Le DB porte ma mémoire. Le marqueur CO avant tout. Jamais de guidage sur un évolutif. »

---

# PARTIE XV — PLAN DE RÉVISION (CR)

## Priorité 1 — À maîtriser absolument
- Résolution en 7 sous-étapes + table de décision (>15/5-15/<5NM).
- Logique du calcul du point de croisement et du différentiel de vitesse.
- Choix de l'avion à tourner (rapide vs lent) et gestion du verrouillage/déverrouillage.
- Vols évolutifs : détection sur tous les FL intermédiaires, résolution uniquement verticale, jamais clairance+fréquence ensemble.
- Réaction STCA.
*À comprendre → à mémoriser → à pratiquer (scénarios niveau 1-2) → à automatiser (phraséologie + calculs mentaux de croisement).*

## Priorité 2 — À très bien connaître
- Conditions et LOA de TR (G2/M2/LFBB/intra-ENAC), condition V1≥V2.
- FL refuge et les 3 cas de distance de sortie.
- Règle du transfert avant FL310 pour les arrivées LIML.
- Seuil de 2,5NM aux frontières pendant un guidage.
- exW et coordination de sortie obligatoire.
*À comprendre → à mémoriser → à pratiquer (scénarios niveau 2-3).*

## Priorité 3 — À connaître, moins critique en pression immédiate
- Zones de travail précises et balises secondaires.
- Détails de relève (handover).
- Fonctions IHM secondaires (MVT, FL?, NOTEPAD).
*À comprendre → à mémoriser.*

---

# PARTIE XVI — MODE ENTRAÎNEMENT INTERACTIF (CR)

**« Lance-moi une simu »** — je vous donnerai une situation de contrôle réaliste côté CR (basée sur les scénarios de la Partie X et leurs variantes), sans révéler la solution ; vous prendrez vos décisions de résolution et de phraséologie ; je ferai évoluer le trafic en fonction de vos réponses, introduirai progressivement de la charge et des événements inattendus (demandes pilotes, TR imprévu, révision de secteur adjacent, éventuellement un STCA si une résolution est oubliée), puis j'évaluerai vos décisions et expliquerai ce qui était correct ou non, en citant la règle source.

**« Fais-moi passer un test blanc »** — un test mélangeant connaissances, méthodes, situations, pièges, anticipation, priorisation et récupération après erreur, spécifiquement centré sur le rôle CR, sans réponses données en cours de route ; à la fin : score, erreurs, notions mal maîtrisées, méthodes à retravailler, niveau de préparation estimé, recommandations ciblées sur la Partie XV.

---

# CONTRÔLE QUALITÉ FINAL

- Les 10 livrets ont été relus avec un filtre spécifique CR : tout ce qui concerne l'exécution, la résolution, la phraséologie, le guidage, les TR et la séparation active a été extrait et mis en avant.
- Les responsabilités propres au CR (détection sur tous les FL intermédiaires pour les évolutifs, exécution des 7 sous-étapes de résolution, jamais de modification de la ligne 3) sont clairement distinguées de celles du CO.
- Les nuances et cas particuliers (FL refuge, 3 cas de distance TR, différentiel de vitesse en guidage, seuil de 2,5NM aux frontières, règle du FL310) sont conservés sans simplification.
- Ce manuel est complémentaire du Manuel CO déjà produit ; les deux peuvent être utilisés ensemble pour s'entraîner en binôme ou alterner de perspective.
