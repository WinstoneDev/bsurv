# Manuel de préparation Basic Surveillance — Rôle CO
*Construit à partir des Livrets 1 à 10 (BSURV 2.0, ENAC-ATM Department). Secteur RS/RU, FL285–FL660.*

> **Note méthodologique** : ce manuel s'appuie strictement sur le contenu des 10 livrets fournis. Chaque règle importante indique le livret source entre crochets, ex. **[L3]**. Quand une information demandée par la trame de préparation n'apparaît dans aucun livret (ex. détail réglementaire hors BSURV, retours d'expérience d'instructeurs), c'est signalé explicitement par **[Non couvert par les sources]** plutôt qu'inventé. Les conseils pédagogiques que j'ajoute pour faciliter la mémorisation (mnémotechniques, formulations d'automatismes) sont signalés par **[Conseil pédagogique]**.

---

## SOMMAIRE

- Partie I — Fondamentaux
- Partie II — Méthodes (fiches détaillées CO et CR)
- Partie III — Surveillance et circuits visuels
- Partie IV — Anticipation
- Partie V — Gestion des conflits et séparations
- Partie VI — Communications
- Partie VII — Priorisation et charge mentale
- Partie VIII — Situations complexes (vols évolutifs, TR, relève, urgence)
- Partie IX — Erreurs et pièges
- Partie X — Scénarios d'entraînement personnalisés (3 niveaux + pièges)
- Partie XI — Banque de questions (+ corrigés séparés)
- Partie XII — Automatismes (arbres décisionnels compacts)
- Partie XIII — Checklists mentales
- Partie XIV — Fiche de survie CO
- Partie XV — Plan de révision priorisé
- Partie XVI — Mode entraînement interactif (simu / test blanc)

---

# PARTIE I — FONDAMENTAUX

## 1.1 L'UCE et le binôme

En BSURV, vous gérez le secteur RS/RU (FL285 à FL660), au sein d'une Unité de Contrôle Espace (UCE) gérée par un binôme : **CO (Contrôleur Organique / Planning Controller)** et **CR (Contrôleur Radar / Radar Controller)** **[L1]**. Les deux contrôleurs vérifient réciproquement leur travail et communiquent de façon claire et précise **[L1]**.

**Répartition CO / CR — à RETENIR :**
- **CO** : ligne 3 de l'étiquette (conditions de sortie : XPT, XFL, PFL, NS). Le CO organise les conditions de sortie ; le CR ne doit jamais modifier les champs de cette ligne **[L1]**.
- Cela ne veut pas dire que le CO ignore les lignes 0–2, ni que le CR ignore la ligne 3 : chacun s'y intéresse, mais la responsabilité de saisie appartient au rôle indiqué **[L1]**.
- **IMPORTANT** : en lisant l'étiquette, le CO doit détecter et corriger toute incohérence (route, parité, équipement, secteur suivant…) **[L1]**.

## 1.2 Sources d'information sur la position

- Image radar (un écran par contrôleur).
- Écran secondaire à deux fenêtres dynamiques : en haut, infos secteur (vents en altitude — absents en BSURV —, activité militaire — absente en BSURV —, METAR/SIGMET, QFU) ; en bas, la SEL (SEctor List) = liste des vols prévus/présents **[L1]**.
- FDW (Flight Data Window) : infos complémentaires par vol.
- L'IHM s'appelle **CHEER**, identique sur tous les degrés en-route ENAC ; description exhaustive dans le Manuel CHEER-IHM sur E-Campus **[L1]**.

**À RETENIR** : « Un des objectifs de formation est de savoir détecter efficacement mais aussi de renseigner le système rigoureusement. » Tous les outils électroniques se nourrissent des données saisies : des données fausses ou incomplètes rendent les outils/alarmes inutilisables, voire dangereux **[L1]**.

## 1.3 L'étiquette (label)

- **Ligne 0** : case marqueur de 1ère analyse CO (à cocher) ; alarmes (REV, SHOW…) ; Vz automatique si montée/descente (+/- centaines de ft/min).
- **Ligne 2** : AFL (Actual FL) et CFL (Cleared FL) — *sauf* si état Avancé/Assumable (rose ou blanc/rose), où ce champ montre l'**EFL** (Entry FL = XFL du secteur précédent). L'EFL devient CFL à l'assume (blanc) **[L1]**.
- **Ligne 3** (CO) : **XPT** (point de sortie), **XFL** (niveau de sortie), **PFL** (niveau le plus haut planifié dans le groupe de secteurs interopérables, 2 digits), **NS** (Next Sector) **[L3]**.
- **Ligne 4** (étiquette développée) : cap, SFL (niveau sélecté pilote), vitesse IAS/Mach **[L3]**.
- **EFL vs CFL** : EFL = FL d'entrée dans le secteur ; CFL = FL clairé (remplace l'EFL lors de l'assume) **[L1]**.

**Étiquette réduite — logique de concaténation (aide-mémoire automatique CHEER)** **[L2]** :
| Condition | Ce qui s'affiche |
|---|---|
| AFL = CFL = XFL | AFL seul (rien à faire en altitude) |
| AFL ≠ CFL | AFL + barre de tendance + CFL |
| AFL/CFL ≠ EFL | AFL (+ barre tendance) + EFL |
| AFL/CFL ≠ XFL | XFL affiché (reste une évolution à donner avant la sortie) |

**Champs « h s r »** (ligne 2, étiquette réduite) : rappellent qu'un cap (h), une vitesse (s) ou un taux (r) a été assigné **[L2]**.

**Particularisation (highlight)** — clic (M) sur le champ **[L2]** :
- Partagée (visible du binôme) : Vz, Indicatif, XPT, XFL, champs Mode S.
- Locale : ACFT, ADES, CFL, PFL, Secteur suivant.

## 1.4 États du vol (chronologiques) **[L1]**

1. **Pas concerné (Unconcerned)** — éléments non reçus.
2. **Avancé (Advanced)** — éléments reçus (c'est seulement dans cet état que la méthode de travail démarre).
3. **Assumable** — avion transféré par le secteur précédent (uniquement secteurs interopérables).
4. **Assumé (Assumed)** — avion sur ma fréquence.
5. **Transférable** — éléments envoyés au secteur suivant.
6. **Transféré** — avion proposé en transfert au secteur suivant (interopérable uniquement).
7. **Assumé secteur suivant** — avion assumé par le secteur suivant.
8. **Unconcerned** (sortie) — avion sorti de la zone d'intérêt.

Ce code couleur est repris identiquement dans la SEL et la FDW **[L1]**.

**Assumable vs Avancé** : *Assumable* = le secteur précédent interopérable a transféré le vol ; *Avancé* = pas encore transféré **[L1]**.

## 1.5 Coordination — deux types **[L1]**

1. **Automatique** (via l'écran radar) : le secteur recevant visualise automatiquement les éléments ~10 min avant l'entrée.
2. **Téléphonique** : le CO donnant propose (ou le CO recevant demande) une modification, par téléphone.

- **Interopérables** (tous les secteurs français adjacents à RS/RU) : la modification est saisie côté donnant et immédiatement visible côté recevant.
- **Non-interopérables** (secteurs de centres étrangers — **G2 Genève, M2 Milan** sont les secteurs adjacents non-interopérables **[L1]**) : chaque CO doit saisir sur sa propre interface.

**Règle absolue de coordination** **[L3]** :
- **a) Secteur suivant a déjà reçu les éléments (XPT moutarde)** : tout changement de XFL et/ou XPT et/ou tout écart >5NM entre trajectoire et PDR prévue **doit être coordonné** entre le PC (CO) donnant et le CO recevant.
- **b) Secteur suivant n'a pas encore reçu les éléments** : changement de XFL possible **sans coordination** ; changement de XPT et/ou écart >5NM **doit être coordonné**.
- NB : une coordination est une négociation — le secteur suivant peut refuser.

## 1.6 L'Agenda / Data-Blocks (DB)

Outil pour marquer les conflits et ordonner chronologiquement les actions. Un DB regroupe 2 à 6 vols et donne une vision chronologique des situations à venir et des vols concernés **[L1]**.

## 1.7 Vue d'ensemble : Méthode de Travail (2 phases) **[L1]**

1. **1ère analyse** — dès l'apparition en rose du vol. Se termine par le marquage de fin de 1ère analyse.
2. **Suivi du vol** — répétitions du cycle **intégration → détection → résolution → configuration de sortie**, plus courtes car il s'agit de réactiver et mettre à jour des éléments déjà mémorisés.

**Marqueurs de fin de 1ère analyse** **[L2]** :
- Côté CO : case vide en début de ligne 0, à cocher — visible côté CR.
- Côté CR : police en gras avant marquage → normale après (« dégraissée »).
- **Pourquoi le CR attend le marqueur CO** : l'analyse du CO peut encore modifier des éléments du vol (ex. changement d'EFL) — le CR ne doit pas commencer sur des données susceptibles de changer **[L2]**.

---

# PARTIE II — MÉTHODES (fiches détaillées)

## FICHE MÉTHODE 1 — Méthode de Travail du CO (1ère analyse)

### Objectif
Prendre en charge un nouveau vol de façon fiable et exhaustive, avant qu'il ne devienne un problème de sécurité.

### Quand l'utiliser
Dès l'apparition en rose (état Avancé) d'un vol sur l'écran radar **[L1][L2]**.

### Procédure détaillée (5 étapes) **[L2][L3][L4]**

**Étape 1 — INTÉGRATION**
- Lecture complète de l'étiquette, de gauche à droite, ligne par ligne.
- Vérification cohérence position courante/ADES et route graphique.
- Vérification de la parité de l'EFL proposé par rapport à la route à suivre.
- Vérification cohérence XFL/ADES.
- **Mémorisation** : indicatif, routes et FL empruntés dans mon secteur, ACFT particulièrement lent/rapide, évolutions verticales à prévoir, actions à entreprendre durant la prise en charge **[L2]**.
- 3 mots-clés : **Lire, vérifier, mémoriser** **[L2]**.
- Aides : IHM (étiquette réduite, particularisés) + circuit visuel systématique.

**Étape 2 — DÉTECTION (des conflits)**
- Définition d'un conflit : le CO/CR estime, sur la base des éléments en sa possession, que sans action la séparation entre 2 aéronefs risque de descendre sous le minimum réglementaire **[L2]**.
- **Critère opérationnel BSURV : estimer si la distance minimale entre 2 avions sera < ou > 15NM** au point le plus proche. Si < 15NM → conflit (risque de non-respect du 5NM radar) **[L2]**.
- **NB : le seuil de 15NM n'a pas de fondement réglementaire — il est empirique et peut varier selon centre/secteur [L2].**
- Ne pas détecter systématiquement tous les vols : inutile entre routes qui ne se croisent pas, ou entre vols stables à des FL différents (sans projet de changement) **[L2]**.
- **Circuit visuel de détection : balayage latéral ET longitudinal des flux d'intérêt du vol étudié** — ne pas négliger son propre flux (rattrapage) **[L2][L3]**.
- **On ne détecte qu'avec des vols dont le marqueur de 1ère analyse est déjà acquitté** — dangereux de faire une 1ère analyse simultanée sur deux vols **[L2]**.
- **PIÈGE classique : un conflit peut en cacher un autre.** Ne jamais arrêter la détection au premier vol conflictuel rencontré **[L4]**.

**Étape 3 — CONFIGURATION DE SORTIE**
- Question à se poser : « Ce vol peut-il être transféré au secteur suivant sans conflit et en respectant les termes de la LOA ? » **[L2]**.
- Circuit visuel : **remontée des flux convergents en sortie**, du XPT vers l'entrée du secteur, pour chaque flux convergent **[L2][L8]**.

**Étape 4 — MARQUAGE DE FIN DE 1ère ANALYSE**
- Cocher le marqueur (case ligne 0) — signale au CR que l'analyse CO est terminée et stable **[L1][L2]**.

**Étape 5 — (implicite, développée davantage côté CR) — SUIVI DU VOL**
- Cycle répété intégration-détection-résolution-configuration de sortie à chaque fois que l'attention revient sur le vol **[L1]**.

*(NB : le livret 3 évoque une « 5ème étape » de la méthode CO sans donner explicitement son nom dans le texte extrait — probablement le suivi du vol / flight follow-up, cohérent avec L1 et le déroulé général.)*

### Points clés (automatismes à développer)
- Ne jamais accepter un vol sans avoir vérifié la parité FL/route.
- Toujours confirmer XFL/ADES cohérents.
- Toujours partager un DB dès qu'un conflit potentiel <15NM est détecté, même sans danger immédiat (ex. avions autorisés à des niveaux différents) **[L9]**.

### Erreurs fréquentes
- S'arrêter au premier vol en conflit détecté sans poursuivre le balayage.
- Oublier d'informer le CR oralement après détection/actions.
- Laisser un marquage résiduel avant transfert (voir Partie IX).

### Réflexe CO
**« Lire, vérifier, mémoriser — balayer large — informer mon CR. »**

---

## FICHE MÉTHODE 2 — Méthode de Travail du CR (Résolution)

### Objectif
Affiner l'analyse du CO, confirmer/infirmer les conflits, et **résoudre** effectivement les situations conflictuelles.

### Procédure détaillée (5 étapes reprises + détail Résolution en 7 sous-étapes) **[L4][L5]**

1. **Intégration** : comme le CO à l'apparition du rose, lire entièrement l'étiquette **[L4]**.
2. **Détection** : vérifier que deux avions au même FL respectent le 5NM. *Pourquoi 5NM ?* Le traitement multi-radar mono-pulse et le traitement système à l'ENAC autorisent une séparation radar de 5NM — attention à ne pas confondre le plot (RPS) et la position physique réelle de l'avion ; à cause de l'imprécision des systèmes, le minimum doit toujours être scrupuleusement respecté **[L4]**.
3. **Configuration de sortie** : confirme/infirme l'analyse CO.
4. **Résolution** — méthode en 7 sous-étapes **[L5]** :
   1. Déterminer le point de croisement.
   2. Estimer qui arrive premier au point de croisement et la distance minimale de séparation (fonction vitesses + angle des routes).
   3. Déterminer le cas et en déduire le type de résolution :
      - **< 5NM (ou doute)** → guidage : altération de cap d'un avion + verrouillage du second (ou altération des deux).
      - **Entre 5 et 15NM** → verrouillage des caps des deux avions (sans les tourner).
      - **> 15NM** → surveillance seule.
   4. Élaborer la solution (analyse position/trajectoires).
   5. Décider **quand** résoudre, et le faire.
   6. Vérifier que la solution résout bien le conflit.
   7. Déverrouiller les caps en fin de guidage.

### Logique / raisonnement du calcul de croisement **[L3][L6]**
- Mesurer la distance de chacun des avions au point de croisement.
- Calculer la différence entre les deux distances.
- **Corriger cette valeur selon le différentiel de vitesse** (NM/min gagné ou perdu, fonction du temps restant avant le point de croisement).
- Le point de plus grande proximité se situe **après** que le premier avion a franchi le point de croisement, mais **avant** que le second ne l'atteigne **[L3]**.
- Plus l'angle des routes est fermé après le point de croisement, plus le rapprochement résiduel est important **[L3]**.
- Vocabulaire : **Dmini** = distance minimale de séparation = plus petite distance entre les deux avions **[L3]**.

### Choix de l'avion à tourner et du sens **[L6]**
- Tourner de préférence l'avion **le plus en retard** au point de croisement pour **rallonger sa trajectoire** (le tourner vers le côté qui l'éloigne, ex. « à gauche » selon géométrie).
- **Avion rapide vs avion lent** : pour une même altération de cap, un avion rapide s'écarte de sa trajectoire plus vite qu'un avion lent (ex. 20° donnés à un rapide ≈ 30° donnés à un lent pour un effet équivalent à un instant donné). **Conséquence pratique : altération plus faible nécessaire sur l'avion rapide, MAIS verrouillage à conserver plus longtemps pour éviter qu'il ne rattrape le lent à la remise en navigation [L6].**
- Toujours consulter le cap actuel avant de donner l'instruction (« Consultation du cap : @hXXX »), puis délivrer le message, puis saisir l'IHM en même temps que le message **[L5][L6]**.

### Vérification et déverrouillage
- Utiliser les vecteurs vitesse (typiquement 3 min) pour visualiser la position au point de plus grande proximité et confirmer que le minimum sera respecté **[L5][L6]**.
- Déverrouiller dès que la séparation recommence à augmenter (les pistes s'éloignent) **[L4][L5][L6]**.
- Toujours vérifier, avant de remettre un avion en navigation directe, que la remise ne créera pas un nouvel écart >5NM de la route en sortie sans coordination (voir §1.5) **[L5]**.
- **Respect des secteurs adjacents pendant le guidage** : le plot d'un avion guidé ne doit jamais s'approcher à moins de **2,5NM** (moitié du minimum radar) des frontières de secteur sans coordination préalable **[L5]**.

### Signaux d'alerte
- Un vol qui rattrape un autre plus vite que prévu.
- Un déverrouillage donné trop tôt (les pistes ne sont pas encore éloignées).
- Oubli du suivi général (autres vols) pendant qu'on est concentré sur une résolution — **toujours faire un tour de suivi de vol** avant de revenir vérifier un guidage en cours **[L5]**.

### Erreurs fréquentes
- Tourner l'avion sans consulter son cap actuel au préalable.
- Verrouiller sans informer le CO (le CO doit tenir l'IHM à jour, ex. XFL, coordinations).
- Oublier de coordonner un avion qui, après guidage, sortirait à plus de 5NM de sa route prévue.

### Réflexe CR
**« Point de croisement → qui est premier ? → quel cas (5/15NM) ? → agir tôt → vérifier → déverrouiller au bon moment. »**

---

## FICHE MÉTHODE 3 — Transfert sous séparation radar (Radar Handover, RH/TR)

### Objectif
Transférer deux avions suivant la même route au même niveau, en toute sécurité, sous une séparation assurée par les vitesses plutôt que par une nouvelle analyse complète du secteur suivant.

### Deux cas de figure **[L7]**
1. **> 20NM au moment du transfert de contrôle** : « séparation réduite » — pas de verrouillage de vitesse obligatoire, pas de coordination téléphonique nécessaire (selon LOA) **[L7]**.
2. **< 20NM** : **transfert sous séparation radar**, procédures décrites dans les LOA entre centres. Condition impérative : **verrouillage des vitesses des deux avions**, avec **V(1er) ≥ V(2ème)**. Transferts de communication effectués « de façon rapprochée » **[L7]**.

### LOA connues (valeurs BSURV) **[L7]**
| Secteur adjacent | Modalités | Séparation minimale |
|---|---|---|
| Genève (LSAG / G2) | Coordination téléphonique obligatoire | 10NM |
| Milan (LIMM / M2) | Coordination téléphonique obligatoire | 10NM |
| Bordeaux (LFBB) | Transfert radar silencieux | 10NM |
| Secteurs du même centre ENAC | Transfert radar silencieux | 10NM |

- NB : une **coordination**, contrairement à une **notification**, peut être refusée **[L7]**.
- **Silencieux** = pas d'appel téléphonique requis, la coordination est implicite si les conditions LOA sont respectées.

### Procédure détaillée
1. Le CR détecte deux vols au même FL, même route, distance mesurée.
2. Vérifier/obtenir les points de Mach des deux avions (consultation en fréquence si besoin : « What would be your Mach number at requested FL? »).
3. Vérifier condition **V1 ≥ V2** et la distance minimale requise (LOA).
4. Selon interopérabilité :
   - Si secteur **interopérable** silencieux : le CR peut réaliser directement le transfert en verrouillant les vitesses (S field mis à jour).
   - Si secteur **non-interopérable** (G2/M2) ou coordination requise : le CO doit appeler et transmettre indicatifs, position, FL, distance entre les deux, points de Mach **[L7]**.
5. Une fois l'accord obtenu, verrouiller les vitesses des deux avions, mettre à jour le champ S de l'étiquette en même temps que le message.
6. Transfert de communication rapproché entre les deux avions.
7. En sortie, lever la restriction de vitesse dès que la configuration le permet (ex. après divergence de route) via RESUME dans le menu Speed.

### Cas particulier : révision de niveau créant un TR
Si une demande de montée/descente d'un avion crée un rapprochement <20NM avec un autre déjà transféré : le CR informe le CO, qui coordonne avec le secteur suivant en précisant que l'évolution crée un TR (même silencieux) **[L7]**.

### Refus obligatoire
Lors d'une demande de changement de FL à l'intérieur de RS/RU : si la vitesse du second avion est supérieure à celle du premier, **ou** si la distance ne respecte pas la LOA, **le CR doit refuser** la demande **[L7]**.

### Réflexe CR/CO
**« 20NM ou moins ? → verrouiller si <20NM (V1≥V2) → interopérable ? → sinon coordonner (indicatifs/FL/distance/Mach) → transfert rapproché → lever restriction dès divergence. »**

---

## FICHE MÉTHODE 4 — Vols évolutifs entrant/sortant par le plancher (LIML)

### Contexte BSURV **[L8][L9]**
- RS/RU s'étend de FL285 à FL660 ; le secteur adjacent en-dessous est **RM**.
- **Départs LIML (Milan)** : LIMM (tour/approche Milan) autorise au FL250, transfert à RM qui monte vers FL280 avant transfert à RS. **Limite de transfert de contrôle entrée = FL285** **[L8]**.
- **Arrivées LIML** : ENAC ACC / Milan ACC prévoient un transfert des arrivées Milan au secteur M2, autorisées en descente vers FL260. RS/RU initie la descente vers FL290 puis transfère à RM, qui poursuit vers FL260 avant transfert à M2 **[L9]**.

### A) Méthode CO pour un DÉPART LIML (entrant par le plancher) **[L8]**
1. **Intégration** : lecture étiquette — AFL/EFL indiquent une entrée par le plancher ; FDW confirme ADEP=LIML ; vérifier cohérence route/ADES et **parité du XFL** (FL impair pour un départ LIML orienté JUVEN/GAI, par exemple).
2. **Détection** : *ne concerne que les avions volant au FL plancher du secteur (FL290 dans RS)*. Question : « Un avion au FL290 croise-t-il ce départ à moins de 15NM ? »
   - Si conflit détecté mais niveaux d'autorisation différents (départ encore en dessous) : **pas de danger immédiat → pas de W électroniques**, mais **créer un DB partagé** pour que le CR n'oublie pas ce conflit potentiel.
3. **Configuration de sortie** : vérifier qu'aucun autre avion ne sort par la même route/niveau prévu.
4. **Résolution** : dans tous les cas, **c'est le CR qui résout** un conflit entre un vol évolutif et un vol du secteur.
5. **Informer le CR** de la situation, y compris si le départ doit stabiliser un moment au FL280 dans le secteur RM avant d'entrer (dans ce cas, demander au CO d'appeler RM pour prévenir du palier, en précisant jusqu'à quand).

### B) Méthode CR pour un DÉPART LIML **[L8]**
1. Intégrer les infos transmises par le CO.
2. **Détecter sur TOUS les FL intermédiaires jusqu'au FL de sortie prévu** (le CO ne détecte qu'au FL plancher — le CR élargit).
3. Étudier la configuration de sortie (pas d'autre avion au même FL/route en sortie).
4. **Résolution par séparation verticale** (pas de guidage sur un vol évolutif en BSURV) : maintenir la séparation verticale jusqu'à ce que les avions se soient croisés et éloignés (souvent 5NM), puis autoriser la poursuite de la montée.
5. Une fois la montée reprise et confirmée, supprimer le DB.

**FL refuge (safe FL)** — cas d'un conflit en sortie pour un vol évolutif **[L8]** :
- Le CO détermine un **FL refuge** = premier FL libre en dessous du FL demandé, respectant la parité, si la distance de sortie est susceptible d'être <20NM avec un trafic de même route/FL proche en vitesse. Il **particularise le XFL** du vol concerné pour matérialiser cette situation, et informe le CR.
- Le CR affine à l'appel du vol, selon 3 cas :
  - **a) Distance sortie > 20NM** : pas de TR, pas de FL refuge utilisé.
  - **b) Distance sortie entre 10 et 20NM, vitesses compatibles (V1≥V2)** : création TR par verrouillage des vitesses, pas de FL refuge utilisé.
  - **c) Distance sortie < 10NM et/ou vitesses non compatibles** : pas de TR, **le CR maintient l'avion au FL refuge**. Le CR informe le CO, qui retire le particularisé et ajuste (MOD si besoin).
- **Anticipation du niveau au 1er contact** : le contrôleur doit préparer mentalement, avant même l'appel du pilote, le niveau qu'il donnera (le plus haut disponible compte tenu du trafic à venir) **[L8]**.

### C) Méthode CO pour une ARRIVÉE LIML (sortant par le plancher) **[L9]**
1. **Intégration** : ADES=LIML → « cet avion descendra et sortira par le plancher » (aide mémoire IHM : XFL affiché « x29 » en étiquette réduite dès que EFL/CFL ≠ XFL). Vérifier parité EFL.
2. **Détection** (question type) : « Cet avion peut-il traverser mon secteur sans problème à son niveau en entrée ? » → recherche de conflit avec un **vol stable au même FL** croisant sa route (balayage latéral/longitudinal classique).
3. **Configuration de sortie** (question type) : « Cet avion peut-il sortir de mon secteur sans problème ? » → détecter tout conflit entre l'arrivée LIML et un avion volant au **FL plancher** (FL290) qui retarderait la descente. **Informer le CR et créer un DB partagé** pour tout avion FL290 croisant à moins de 15NM.
4. Le **CR** est responsable de la détection sur **tous les FL intermédiaires** entre EFL et XFL.

### D) Méthode CR pour une ARRIVÉE LIML **[L9]**
- Objectif : fournir une **séparation verticale** pour tout avion à destination/départ de LIML.
- **Règle du transfert avant palier** : un avion en descente doit être transféré **au plus tard en passant le FL310** (2000ft au-dessus du plancher FL290), pour éviter un palier lié à un changement de fréquence tardif.
- Si un palier est inévitable : le CR demande au CO d'appeler **RM pour une délégation de niveau** (demande de FL dans le secteur RM) — via la fonction IHM **« FL ? »** dans le menu indicatif de l'étiquette (après s'être assuré que RM a bien reçu les éléments, sinon utiliser **« MVT »** pour forcer l'envoi).
- Une fois le FL délégué obtenu, le CO modifie le XFL et informe oralement le CR du niveau donné.
- **Séquence type de descente contrainte** : clairer initialement 1000ft au-dessus du trafic gênant → une fois les avions croisés et 5NM en éloignement → poursuivre la descente.
- **RÈGLE DE SÉCURITÉ CRITIQUE** : ne **jamais cumuler une clairance de niveau et un transfert de fréquence dans le même message** — si le pilote comprend mal et quitte la fréquence, aucune correction rapide n'est possible **[L9]**.
- Un nouvel avion qui apparaît doit toujours déclencher une remise à jour complète de l'analyse de situation, même si un conflit précédent semblait écarté (« l'apparition d'un nouveau vol peut tout changer ! ») **[L9]**.

### Réflexe CO / vols évolutifs
**« Départ = je détecte seulement au plancher, je délègue la résolution au CR. Arrivée = je détecte en entrée + je vérifie la sortie au plancher. Le CR, lui, détecte TOUS les niveaux intermédiaires. »**

---

## FICHE MÉTHODE 5 — Révision de niveau demandée par un secteur adjacent (entrée)

### Contexte **[L10]**
Un secteur voisin (ex. S2) appelle pour demander l'acceptation d'un changement de niveau sur un vol déjà prévu stable et sans conflit dans votre secteur.

### Procédure CO
1. **Intégrer** l'information, **détecter les conflits**, **étudier la configuration de sortie** — dans cet ordre.
2. **Détection pour un avion révisé en entrée** : identifier **tous les FL traversés** par l'évolution (ex. montée FL320→FL340 : détecter à FL330 ET FL340).
3. **Critère d'acceptation** : pour chaque FL traversé, évaluer si un autre avion interfère à moins de 15NM (calcul point de croisement classique).
4. **Si conflit détecté à un des FL** : **refuser l'évolution**, maintenir séparation verticale (« Négatif pour le niveau demandé, [callsign] FL[X] comme prévu initialement, il montera plus tard dans mon secteur »). Le secteur demandeur ne fait alors pas de MOD.
5. **Si pas de conflit détecté** : accepter, modifier le XFL en conséquence, informer le CR oralement. Le CR (comme pour tout vol évolutif) attendra le croisement effectif avant d'autoriser le niveau final.
6. **Toujours enchaîner sur l'étude de sortie** même après acceptation en entrée : un conflit en entrée peut être absent mais un problème de sortie subsister, ou l'inverse.

### Cas secteur non-interopérable qui demande un niveau non desservi par le prochain secteur
- Utiliser la fonction IHM **« MONTRER » (SHOW)** pour forcer la visualisation d'un vol sur un secteur interopérable normalement non-concerné par ce vol (ligne 0 : mention SHOW) **[L10]**.
- Puis coordination téléphonique avec le secteur réellement concerné (ex. I3 au lieu de I2), qui peut accepter un niveau intermédiaire différent du niveau final demandé.

### Réflexe
**« Révision = je détecte à CHAQUE FL traversé, pas seulement à l'arrivée. »**

---

# PARTIE III — SURVEILLANCE ET CIRCUITS VISUELS

## 3.1 Principe

Le circuit visuel dirige non seulement le regard mais **l'attention** vers les éléments permettant de prendre en compte le vol étudié. **Chaque étape de la Méthode a son propre circuit visuel [L2].**

| Étape | Circuit visuel |
|---|---|
| Intégration | Lecture complète étiquette + FDW + route graphique au survol |
| Détection | Balayage **latéral et longitudinal** des flux d'intérêt |
| Configuration de sortie | **Remontée** des flux convergents depuis le XPT vers l'entrée du secteur |

## 3.2 Zones de travail RS/RU **[L3]**

L'ENAC demande de procéder par « zones de travail » (dépend en réalité de la structure du secteur, des flux, de la culture du centre) :
1. **LTP** — toute la partie **est** du secteur.
2. **GRENA-BOSUA** — ce point de conflit + interface avec **M2**.
3. **MTL** — ce point de conflit + toute la partie **sud** du secteur.
4. **MEN** — toute la partie **ouest** du secteur.
5. **MINDI** — le **nord-ouest** du secteur.
6. **LSE** — ce point de conflit + toute la partie **nord** du secteur.

## 3.3 Points de conflit connus **[L2][L3]**
- **RS/RU** : MTL, GRENA, LSE.
- Autres balises citées en configuration de sortie/circuits : FREDI, SANTO, LANZA, MOZAO, SPIDY, BOSUA.
- Interface avec sortie plancher : SPIDY (flux MAJOR→MTL→CFA / MAJOR→MTL→LTP→MOZAO→SPIDY).

## 3.4 Cycle continu de suivi **[L3]**

Le processus de suivi (le « circuit ») est **continu** : quand il est terminé, il doit automatiquement reprendre depuis le début. Le contrôleur revient sur chaque vol de la zone, met à jour sa connaissance, se pose les bonnes questions selon l'état/position du vol :

| État du vol | Questions à se poser |
|---|---|
| **Pas en fréquence (rose)** | Réactivation et actualisation de l'intégration |
| **En fréquence (blanc)** | Le vol évolue-t-il comme prévu ? Quel est le plan du CR ? De quoi aurais-je besoin à sa place ? Coordination ou MOD nécessaire ? Quand ? |
| **Proche de la sortie (blanc/moutarde)** | Contrat de sortie rempli ? Vol stable ? Établi sur son XPT ? À moins de 5NM de la route ? Coordination nécessaire ? Quand ? |

**Aide au rappel automatique** : en cas de DB, le survol de l'étiquette affiche automatiquement Vecteurs Vitesse et halos bleus des vols concernés — permet de réévaluer à chaque passage **[L3]**.

## 3.5 Surveillance active pendant le suivi
- Vérifier en permanence que les avions suivent la navigation autorisée. Écart constaté → **« [Indicatif], you are to the left/right of your track, resume navigation direct [balise] »** **[L6][L10]**.
- Lecture d'étiquette : si CFL ≠ XFL persistant, cela signale qu'une MOD ou une nouvelle clairance est nécessaire ; **au moment du transfert de communication, il faut toujours avoir XFL = CFL** **[L8]**.

---

# PARTIE IV — ANTICIPATION

## 4.1 Principes d'anticipation extraits des sources

- **Anticiper la mise en œuvre d'une résolution** pour avoir le temps d'en vérifier l'efficacité et de la corriger si besoin — il n'existe pas de « moment exact » ni de « cap parfait » ; l'essentiel est d'agir assez tôt **[L5]**.
- **Anticiper les demandes des pilotes** (ex. niveau de croisière) pour ne pas subir la situation : préparer mentalement le niveau qu'on donnera avant même l'appel **[L8]**.
- **Anticiper les rappels de secteur** : demander un avion tôt en fréquence lorsque le conflit devra être résolu avant l'entrée réelle dans le secteur (ex. Situation 3 — TAR156/FGCAD, croisement quasi-immédiat) **[L6]**.
- **Anticiper les prochains points de conflit connus du secteur** en connaissant les zones de travail (LTP, GRENA-BOSUA, MTL, MEN, MINDI, LSE) — cela dirige où porter l'attention avant même l'apparition d'un problème **[L3]**.
- **Réviser en continu le niveau prévu** pour un vol maintenu à un FL intermédiaire, à chaque nouvel avion apparaissant dans le secteur **[L9]**.

## 4.2 Exemple simple
Un vol stable croise un point de conflit connu (MTL) dans 8 minutes ; dès l'intégration, en l'absence de tout autre trafic visible sur les vecteurs vitesse courts, le contrôleur calcule déjà mentalement l'écart prévisible en utilisant la méthode distance/différentiel de vitesse, avant même qu'un DB soit nécessaire.

## 4.3 Exemple complexe
Une arrivée LIML est en descente contrainte par un trafic croisé à un niveau intermédiaire (résolution verticale en cours). Un nouveau vol apparaît en rose, destiné au même secteur, sur une route qui croisera potentiellement la trajectoire de descente une fois celle-ci reprise. Le contrôleur doit : (1) terminer son intégration/détection du nouveau vol sans perdre le fil du conflit vertical en cours, (2) réévaluer si le FL initialement prévu pour la reprise de descente est toujours valide compte tenu du nouvel arrivant, (3) ajuster mentalement le niveau à donner au prochain appel **[L9, principe « l'apparition d'un nouveau vol peut tout changer »]**.

---

# PARTIE V — GESTION DES CONFLITS ET DES SÉPARATIONS

## 5.1 Séparations verticales **[L3]**
- Au-dessus du FL195 : espace de classe C (France).
- **FL290 à FL410 inclus** : espace **RVSM**. Minimum entre 2 avions équipés RVSM = **1000ft**. Entre un avion non équipé et tout autre (équipé ou non) = **2000ft**.
- **Au-dessus du FL410** : minimum 2000ft pour tous. FL utilisables pairs : 430, 450, 470, 490…
- **Parité des routes** : respecter la parité allouée limite le nombre de conflits et évite les face-à-face au même FL — fait partie de la stratégie du réseau de routes/secteurs **[L2][L3]**.
- **exW (exempté RVSM)** : détectable par un **halo cyan** autour du RPS, confirmé en FDW. Tout avion non équipé RVSM doit faire l'objet d'une **coordination téléphonique obligatoire** de sortie pour s'assurer de l'acceptation du secteur suivant. Le CR ne doit jamais transférer un vol exW sans confirmation de cette coordination **[L3][L10]**.

## 5.2 Séparations horizontales **[L2][L3][L4]**
- **Minimum radar** : 5NM (permis par le traitement multi-radar mono-pulse ENAC).
- **Critère opérationnel de détection** : <15NM au point le plus proche = conflit potentiel à traiter.
- Attention à la distinction plot (RPS) / position physique réelle — imprécision des systèmes → toujours respecter scrupuleusement le minimum **[L4]**.

## 5.3 Table de décision résolution CR **[L5]**
| Distance minimale estimée | Action |
|---|---|
| > 15NM | Surveillance seule |
| Entre 5 et 15NM (certain) | Verrouillage des caps des deux avions (sans les tourner) |
| < 5NM ou incertitude | Guidage : tourner au moins un avion (altération de cap) + verrouiller l'autre |

## 5.4 Séquence de résolution par guidage (rappel condensé)
1. Point de croisement.
2. Qui arrive premier / distance minimale corrigée du différentiel de vitesse.
3. Cas (tableau ci-dessus).
4. Choisir quel avion tourner (généralement celui en retard, ou celui dont l'altération est cohérente avec sa route ultérieure pour ne pas le pénaliser — cf. exemple FGCAD tourné à gauche car sa route tourne ensuite à gauche vers MINDI/CFA **[L6]**).
5. Décider du moment et agir (consultation cap → instruction → saisie IHM simultanée).
6. Vérifier via vecteurs vitesse (3 min) que le minimum sera respecté.
7. Déverrouiller dès l'éloignement confirmé, remettre en direct sur la balise la moins pénalisante.

## 5.5 Résolution par séparation verticale (vols évolutifs) **[L8][L9]**
- En BSURV, **aucun guidage n'est appliqué à un vol évolutif** : la résolution se fait uniquement par séparation verticale (maintien à un FL intermédiaire jusqu'au croisement + éloignement, typiquement 5NM).
- Anticiper une descente légèrement en avance (« 2000ft en dessous ») peut être moins pénalisant qu'un guidage qui allongerait la trajectoire — le choix de résolution reste à la convenance du contrôleur **[L9]**.

## 5.6 Situation d'urgence — filet de sauvegarde STCA **[L10]**
Si la résolution nécessaire a été oubliée (ex. absorption par une autre surveillance) et que le **STCA (Short Term Conflict Alert)** se déclenche (minimum radar 5NM sur le point d'être franchi, <2 min) :
- **Réaction immédiate obligatoire.**
- Donner de **fortes altérations de cap (minimum 30°)** aux deux avions avec la phraséologie d'urgence :
  > *« [Indicatif], immediately, turn right immediately 30° to avoid traffic »*
- Compléter si possible avec une information de trafic :
  > *« [Indicatif], traffic 11 o'clock, 5NM »*
- Une fois la situation résolue, remettre chaque avion en direct sur le prochain point non pénalisant de sa route.

**AUTOMATISME CRITIQUE** : le STCA est un filet de sauvegarde, pas un outil de travail normal — sa survenue signale une **erreur de méthode ou de surveillance** en amont (détection non poursuivie, résolution non exécutée, ou attention totalement absorbée ailleurs).

## 5.7 Ouverture d'attente / info Chef de Salle (CDS) **[L10]**
Le Chef de Salle transmet des informations externes (ex. ouverture d'une attente à destination). Le CO :
1. Accuse réception (« Hold open at Milan, roger »).
2. Crée un **post-it (NOTEPAD)** partagé avec le CR (« LIML hold open »).
3. Le CR informe les pilotes concernés (« Expect hold in Milano »).
4. Aucune autre action requise à cette distance ; les pilotes peuvent réduire leur vitesse par anticipation.

---

# PARTIE VI — COMMUNICATIONS

## 6.1 Principes généraux
- La phraséologie vise à être **claire et concise** ; le collationnement sert à s'assurer que le message a bien été entendu et compris **[L5]**.
- Les pilotes doivent collationner **tout ce qui constitue une clairance** : niveau, route/cap, code transpondeur, restriction de vitesse, fréquence, etc. **[L5]**.
- **Écouter attentivement les collationnements** et les corriger si besoin — un pilote peut collationner une fréquence ou un niveau erroné sans que ce soit une erreur de frappe **[L5]**.
- Correction : le message commence par **« Negative »** :
  > *CR : « Negative [indicatif], contact ENAC 125.830 »*

## 6.2 Structure des principaux messages

**Prise de contact / clairance initiale**
> PIL : « ENAC, [indicatif], bonjour/good morning, [niveau], [Mach] »
> CR : « [indicatif], ENAC, good morning, maintain [FL], route [X-Y], maintain [Mach] or greater/less »

**Consultation de cap avant guidage** (toujours faire avant de donner une instruction)
> « Consultation du cap de [indicatif] : @h[XXX] »

**Guidage (vectoring)**
> CR : « [indicatif], turn left/right heading [XXX] for spacing »
> CR : « [indicatif], continue present heading for spacing » (si on ne tourne pas mais qu'on verrouille)

**Déverrouillage**
> CR : « [indicatif], resume own navigation direct [balise] »

**Transfert sous séparation radar — vitesse imposée**
> CR : « [indicatif], maintain Mach [.XX] or greater/less »

**Levée de restriction de vitesse**
> CR : « [indicatif], no more speed restriction »

**Descente/montée contrainte (vol évolutif)**
> CR : « [indicatif], descend/climb initially [FL], due to [converging/opposite] traffic, I call you back »
> (plus tard) CR : « [indicatif], descend/climb [FL] »
> **Ne jamais cumuler clairance de niveau + transfert de fréquence dans le même message [L9].**

**Transfert de fréquence** (toujours après vérification qu'il n'y a plus d'instruction à donner et étiquette « nettoyée »)
> CR : « [indicatif], contact ENAC [fréquence] »
> (radar handover) CR : « [indicatif], report Mach number to [centre] [fréquence] »

**Refus de niveau (mauvaise parité)**
> CR : « [indicatif], this level is not available on your route, you must choose an odd/even level »
> ou (proposition) : « would you prefer 37 or 39? » — **éviter d'énoncer les trois chiffres complets d'un niveau dans une contre-proposition, pour ne pas laisser croire à une clairance [L10].**

**Urgence / STCA**
> CR : « [indicatif], immediately, turn right immediately 30° to avoid traffic »
> CR : « [indicatif], traffic 11 o'clock, 5NM »

**Écart de trajectoire non autorisé**
> CR : « [indicatif], you are to the left/right of your track, resume navigation direct [balise] »

## 6.3 Communications entre CO et CR (intra-binôme)
- Après toute détection/action significative, **informer systématiquement son collègue** oralement, ex. :
  > CO → CR : « [indicatif A] est en conflit à [balise] avec [indicatif B] au FL[XXX] »
  > CR → CO : « Roger, thank you » / « Reçu, merci »
- Demandes CR → CO (coordination externe nécessaire) :
  > CR → CO : « Ask N3 if [indicatif] can climb FL[XXX]. This creates a RH with [indicatif2] [X]NM ahead, they would both be at Mach [.XX] »
- Demandes CO → CR (situation à traiter) :
  > CO → CR : « RS/RU. Request early transfer for [indicatif], released for left/right turn »

## 6.4 Ce qu'il faut préparer mentalement avant de parler
- Le **cap actuel** (consultation avant instruction).
- Le **niveau qu'on va donner** (anticipé avant l'appel, cf. §4.1).
- La **raison à donner au pilote** si le niveau est intermédiaire (« due to traffic »).
- Si une coordination est nécessaire **avant** de répondre au pilote (« I call you back » / « Stand by » en attendant).

## 6.5 Erreurs à éviter en communication
- Répondre définitivement avant d'avoir terminé la méthode (toujours utiliser « I'll call you back » / « Stand by » si la résolution n'est pas encore décidée).
- Cumuler clairance + transfert fréquence.
- Oublier d'écouter le collationnement.
- Donner un niveau complet en trois chiffres dans une simple proposition de choix.

---

# PARTIE VII — PRIORISATION ET CHARGE MENTALE

## 7.1 Principes issus des sources

- **La détection ne s'arrête jamais au premier conflit trouvé** — un conflit peut en cacher un autre, particulièrement en charge élevée avec de nombreux vols **[L4]**.
- **Le suivi de vol est un cycle continu et systématique** (zones de travail), pas une réaction ponctuelle — la seule façon de ne rien oublier en tant que CR est de faire son suivi de vol **de façon régulière** **[L8]**.
- **Priorité à la sécurité immédiate** : en cas de STCA, réaction immédiate avant toute autre tâche **[L10]**.
- **L'apparition d'un nouveau vol doit systématiquement déclencher une remise à jour de l'analyse générale**, par les deux contrôleurs, via leurs méthodes respectives **[L9]**.
- **Rôle du DB/Agenda** : outil dédié pour ne pas perdre le fil d'un conflit en cours pendant qu'on traite autre chose (rappel automatique via survol au CHEER) **[L1][L3]**.

## 7.2 Hiérarchie pratique des priorités (déduite des sources)

1. **Sécurité immédiate** — STCA, conflit à très courte échéance (<5NM estimé), avion s'écartant dangereusement de sa route.
2. **Marquage de fin de 1ère analyse et communication au binôme** — pour ne pas bloquer le CR ou laisser un doute sur qui gère quoi.
3. **Poursuite de la détection exhaustive** avant de considérer un vol comme « traité ».
4. **Suivi régulier de l'ensemble du secteur (par zones de travail)**, y compris pendant qu'on gère un conflit ponctuel — « faire un tour de suivi des vols » avant de revenir vérifier un guidage en cours **[L5]**.
5. **Nettoyage des étiquettes** avant transfert (voir Partie IX) — tâche de fin de cycle, jamais oubliée avant un transfert de fréquence.

## 7.3 Comment revenir à une vision globale en cas de surcharge
**[Conseil pédagogique, cohérent avec les principes des sources]** :
- Utiliser systématiquement les **zones de travail** (LTP, GRENA-BOSUA, MTL, MEN, MINDI, LSE) comme grille de balayage périodique — repartir de zone en zone plutôt que de rester fixé sur un seul avion.
- S'appuyer sur les **DB et les marquages automatiques CHEER** (halos, Vz, particularisés, h/s/r) : ce sont des externalisations de mémoire conçues précisément pour réduire la charge cognitive — les utiliser systématiquement au lieu de tout retenir mentalement.
- Revenir au marqueur de fin de 1ère analyse comme point de contrôle : tant qu'il n'est pas coché, le vol n'est pas « acquis » et mérite l'attention prioritaire.

---

# PARTIE VIII — SITUATIONS COMPLEXES

## 8.1 Vol déjà en fréquence qui demande un changement (Méthode CR appliquée en cours de vol) **[L6]**

Quand un vol en fréquence demande un changement (ex. FL) :
1. **Ne jamais répondre immédiatement** : « [indicatif], I'll call you back. »
2. Reprendre la méthode complète : intégrer (vérifier parité), détecter (compte tenu des éléments existants), étudier la sortie (MOD/coordination nécessaire ?), résoudre (accorder ou retarder), suivre.
3. Si les éléments sont déjà passés à un secteur non-interopérable pour la sortie : coordination téléphonique obligatoire du CO avant modification du XFL (alarme REV jaune tant que non acquittée).

## 8.2 Relève (Handover) **[L10]**

Le contrôleur relevé doit présenter précisément :
- **(RS/RU)** Regroupement de secteurs.
- **État des moyens techniques** : radio, téléphone, radar, etc. (« RAS » si tout va bien).
- **Consignes ou informations particulières** : ex. report de turbulence, attente ouverte à Milan.
- **Gestion du trafic** : transmission des éléments importants, conflits en cours, avions sous surveillance, avions en guidage, TR en cours, évolutions verticales à venir…
- Le contrôleur relevé **s'assure de l'acceptation de la relève** par le contrôleur entrant, qui doit lui-même s'assurer d'avoir tous les éléments avant d'accepter (= prendre la responsabilité du trafic).

## 8.3 Étiquette « nettoyée » avant transfert **[L5]**

Avant de transférer un avion, vérifier qu'**aucun marquage résiduel** ne subsiste : XFL affiché en réduit (signe que le vol n'est pas encore à son niveau de sortie), particularisés, W électroniques actifs, DB partagé, champs h/s/r actifs. **Chacun de ces marquages signifie une action encore due.**

## 8.4 Fonctions IHM spécifiques mentionnées
- **MVT** : force l'envoi des éléments d'un vol à un secteur qui ne les a pas encore reçus (utile avant une coordination ou un appel téléphonique) **[L7][L9]**.
- **FL ?** : via le menu indicatif, permet à un secteur suivant interopérable de voir apparaître « FL ? » et préparer sa réponse à une demande de délégation de niveau **[L9]**.
- **MONTRER / SHOW** : force la visualisation d'un vol sur un secteur interopérable normalement non-concerné **[L10]**.
- **NOTEPAD** : post-it partageable entre CO et CR (consignes ponctuelles) **[L10]**.

## 8.5 Coordination sortante avec secteur non-interopérable (format d'appel) **[L2][L7][L10]**

> CO : « RS/RU, request [indicatif] between [X] and [Y] at [odd/even] level »
> ou : « RS/RU, approval request [indicatif] [contexte], FL[XXX] ? »

Le secteur répond « approved » / « wilco » ; en cas d'accord, le CO modifie l'étiquette ; si les éléments avaient déjà été envoyés, CHEER signale une **alarme REV (jaune)** à acquitter une fois la coordination faite.

---

# PARTIE IX — ERREURS ET PIÈGES

| Catégorie | Erreur | Conséquence | Comment la détecter | Comment l'éviter | Automatisme |
|---|---|---|---|---|---|
| Compréhension | Confondre « pas de conflit » avec « pas d'action requise » (ex. vols évolutifs à niveaux différents) | Oubli de créer un DB, surprise ultérieure | Vol proche <15NM sans DB partagé | Toujours créer un DB partagé dès <15NM détecté, même sans W électroniques | « <15NM = DB, toujours » |
| Surveillance | Arrêter la détection au premier conflit trouvé | Conflit caché non détecté, danger différé | Relire systématiquement tout le flux après un 1er conflit | Poursuivre le balayage jusqu'au bout | « Un conflit peut en cacher un autre » |
| Anticipation | Résoudre trop tard (juste avant le point de croisement) | Pas de marge pour vérifier/corriger | Écart entre le moment de la résolution et le point de croisement calculé | Décider le « quand » dès l'étape 5 de la résolution CR | « Agir tôt, vérifier ensuite » |
| Méthode | Commencer sa propre 1ère analyse avant que le collègue ait acquitté la sienne | Travailler sur des données susceptibles de changer | Vérifier le marqueur avant de démarrer | Toujours attendre le marqueur acquitté du collègue | « Marqueur coché = je peux commencer » |
| Communication | Cumuler clairance de niveau + transfert de fréquence | Risque de perte de contrôle en cas de mauvaise compréhension du pilote | Relire son message avant de le donner | Séparer systématiquement les deux instructions | « Une clairance, un message » |
| Communication | Ne pas écouter le collationnement | Erreur de fréquence/niveau non corrigée | Comparer collationnement à l'instruction donnée | Toujours écouter activement, corriger par « Negative » si besoin | « J'écoute chaque collationnement » |
| Priorisation | Rester focalisé sur un guidage en cours sans faire de tour de suivi général | Oubli d'un transfert, d'un autre conflit | Combien de temps depuis le dernier balayage complet ? | Refaire un tour de suivi avant de revenir vérifier un guidage | « Guidage en cours ≠ secteur en pause » |
| Vérification | Déverrouiller un guidage trop tôt | Rapprochement dangereux après la remise en navigation | Vérifier que la distance augmente réellement (pas seulement qu'elle a cessé de diminuer) | Attendre confirmation de l'éloignement net avant « resume own navigation » | « Éloignement confirmé avant déverrouillage » |
| Oubli d'étape | Transférer un avion sans nettoyer son étiquette | Action oubliée, danger potentiel pour le secteur suivant qui prend en charge sans contexte | Repasser mentalement : W électroniques ? DB ? XFL affiché en réduit ? h/s/r ? | Checklist « étiquette nettoyée » avant chaque transfert | « Étiquette propre avant transfert » |
| Stress / surcharge | Oublier une résolution planifiée jusqu'au déclenchement STCA | Situation d'urgence, guidage brutal à 30° | STCA se déclenche | Utiliser systématiquement le DB comme rappel, ne pas se fier à la mémoire seule sur une action différée | « Le DB porte ma mémoire, pas moi seul » |
| Coordination | Oublier une coordination obligatoire (ex. exW sortant, écart >5NM après guidage) | Le secteur suivant refuse ou n'est pas informé | Vérifier avant transfert : avion exW ? avion guidé hors de sa route initiale ? | Ajouter systématiquement ces vérifications à la checklist pré-transfert | « exW et écarts de route = coordination » |

---

# PARTIE X — SCÉNARIOS D'ENTRAÎNEMENT PERSONNALISÉS

## Niveau 1 — Fondamentaux (une seule difficulté à la fois)

### Scénario 1.1 — Intégration simple avec parité incorrecte
**Situation** : Vous êtes CO. Un vol FENAC apparaît en rose, proposé par N3 avec un EFL pair alors que sa route (BOJOL→LSE) exige une parité impaire.
**Informations disponibles** : étiquette complète, FDW, route graphique.
**Ce que vous devez détecter** : incohérence de parité dès la lecture ligne par ligne.
**Ce que vous devez penser** : « La parité ne correspond pas à la route empruntée — je dois demander une modification avant d'accepter. »
**Ce que vous devez faire** : appeler N3, demander un niveau impair entre BOJOL et LSE ; une fois confirmé, modifier votre propre XFL en cohérence ; terminer l'intégration ; passer à la détection.
**Pourquoi** : le respect de la parité limite les conflits en évitant les face-à-face au même FL.
**Piège** : oublier de modifier son propre XFL après avoir obtenu le changement d'EFL — les deux champs doivent rester cohérents.

### Scénario 1.2 — Détection simple par balayage
**Situation** : Vous êtes CO. Un vol RAM123 apparaît, en transit stable via MTL (point de conflit connu).
**Évolution** : après intégration, vous balayez latéralement et longitudinalement le flux MTL.
**Ce que vous devez détecter** : un autre vol (BAW456) au même FL, latéralement, à l'est.
**Ce que vous devez faire** : vérifier si le marqueur de 1ère analyse de BAW456 est déjà acquitté ; si non, terminer d'abord votre propre 1ère analyse de RAM123, puis démarrer celle de BAW456 en revenant sur ce conflit potentiel.
**Piège** : commencer une détection croisée entre deux vols dont aucun n'a de 1ère analyse terminée — dangereux et source de confusion.

### Scénario 1.3 — Résolution simple (verrouillage)
**Situation** : Vous êtes CR. Deux avions convergent avec une distance minimale estimée à 10NM.
**Ce que vous devez faire** : simplement verrouiller les caps des deux avions (« continue present heading for spacing » sur chacun), sans les tourner. Vérifier avec les vecteurs vitesse. Déverrouiller dès l'éloignement confirmé.
**Piège** : tourner un avion alors qu'un simple verrouillage suffisait (résolution disproportionnée, pénalise inutilement le vol).

## Niveau 2 — Intermédiaire (plusieurs éléments simultanés)

### Scénario 2.1 — Guidage avec différentiel de vitesse
**Situation** : Vous êtes CR. TAR156 (rapide, venant de loin) et FGCAD (lent, venant de MAJOR) convergent à MTL avec une différence de distance de 23NM mais une différence de vitesse qui compensera presque entièrement l'écart : arrivée quasi simultanée.
**Évolution** : vous devez agir avant même que FGCAD ne soit dans le secteur — demander l'avion tôt en fréquence.
**Ce que vous devez détecter** : la nécessité d'anticiper fortement (calcul distance/vitesse) et de coordonner un transfert anticipé avec le secteur transféreur.
**Ce que vous devez faire** : informer le CO (« Request early transfer for FGCAD, released for left turn »), puis guider FGCAD à gauche (cohérent avec sa route ultérieure vers MINDI/CFA) pour ne pas le pénaliser.
**Variante** : et si c'était TAR156 (le rapide) qu'on choisissait de tourner à droite pour passer derrière FGCAD ? Réponse attendue : altération plus faible nécessaire (20° au lieu de 30°) car un avion rapide s'écarte plus vite de sa trajectoire, mais le verrouillage devra durer plus longtemps pour ne pas qu'il rattrape le lent à la remise en navigation.

### Scénario 2.2 — Départ LIML avec conflit au plancher + configuration de sortie
**Situation** : Vous êtes CO. TAP145 (départ LIML) apparaît, EFL cohérent, mais un transit AFR1587 se trouve au FL290 (plancher) à moins de 15NM de l'entrée prévue de TAP145.
**Ce que vous devez détecter** : le départ sera autorisé 1000ft en dessous du transit → pas de danger immédiat, mais DB partagé nécessaire quand même. Puis, en sortie, vérifier qu'aucun autre vol au FL310 ne sort par la même route (SPIDY) — ici pas de problème.
**Ce que vous devez faire** : créer le DB partagé (sans W électroniques), informer le CR que la résolution se fera par séparation verticale jusqu'à ce que les avions soient croisés + 5NM en éloignement, puis que la montée pourra reprendre.
**Piège** : activer les W électroniques inutilement (pas de danger immédiat car les niveaux d'autorisation diffèrent) — cela alourdit la charge visuelle sans bénéfice réel.

### Scénario 2.3 — Révision multi-niveaux
**Situation** : Vous êtes CO. S2 demande l'acceptation de DLH771 (actuellement FL320, stable, sans conflit) pour une montée FL340.
**Ce que vous devez détecter** : les FL traversés sont FL330 et FL340 — il faut détecter à CHAQUE niveau. Aucun avion à FL330, mais un avion à FL340 avec un croisement estimé à moins de 15NM au voisinage de MTL.
**Ce que vous devez faire** : refuser l'évolution en entrée (« Négatif pour le niveau demandé, DLH771 FL320 comme prévu, il montera plus tard dans mon secteur »), mais continuer votre raisonnement en étudiant tout de même la sortie — si en réalité les deux avions divergent après MTL et que personne d'autre ne sort à FL340 sur la même route, vous pourrez accepter la montée après le croisement, une fois le vol dans votre secteur (le CR attendra le croisement effectif).
**Piège** : s'arrêter au refus initial sans étudier la suite logique de la sortie — le refus en entrée n'empêche pas d'anticiper une acceptation ultérieure une fois dans le secteur.

## Niveau 3 — Simulation test (charge élevée, plusieurs événements simultanés)

### Scénario 3.1 — Conflit vertical en cours + nouvel arrivant + révision de fréquence
**Situation** : Vous êtes CR. Une arrivée LIML (ITY363) est en descente contrainte par un trafic croisé (BAW451, FL310) ; vous surveillez le moment propice pour reprendre la descente (5NM en éloignement). Simultanément, votre CO vous signale un second conflit à MTL (EZY3203/CTM005, FL360), W électroniques activés, DB partagé.
**Évolution** : vous êtes absorbé par la surveillance du premier conflit (à GRENA) et oubliez de mettre en place la résolution du second. Le STCA se déclenche.
**Ce que vous devez détecter** : l'urgence du STCA prime absolument sur toute autre tâche.
**Ce que vous devez faire** : réagir immédiatement avec des altérations de cap fortes (minimum 30°) sur les deux avions du second conflit, phraséologie d'urgence complète (« immediately, turn right immediately 30° to avoid traffic » + information de trafic), puis reprendre le suivi normal une fois la situation stabilisée, remettre chaque avion en direct sur le point non pénalisant de sa route.
**Pourquoi le piège s'est produit** : concentration excessive sur un seul conflit (visuellement captivant car proche de sa résolution) au détriment du suivi périodique de l'ensemble du secteur — exactement le type d'erreur que la Partie VII vise à prévenir.
**Variante** : et si le CO n'avait pas partagé de DB pour le second conflit ? Le risque d'oubli devient encore plus grand — d'où l'importance systématique du DB comme filet de mémoire externe.

### Scénario 3.2 — TR en cascade avec coordination non-interopérable
**Situation** : Vous êtes CR. RAM151 apparaît, TAP826 déjà présent à 11NM sur la même route/FL — transfert sous séparation radar potentiel. Simultanément, un autre vol du secteur (DAH452) demande un changement de FL en fréquence.
**Ce que vous devez faire** :
1. Répondre à DAH452 par « I'll call you back » et reprendre la méthode complète pour lui pendant que le TR se met en place en parallèle.
2. Pour le TR : vérifier les points de Mach des deux avions, condition V1≥V2, informer le CO de la nécessité de coordonner en sortie (secteur M2, non-interopérable) avec les éléments requis (indicatifs, FL, distance, Mach).
3. Pendant ce temps, traiter la demande de DAH452 : intégrer (parité), détecter, étudier la sortie (coordination nécessaire si éléments déjà passés), résoudre.
**Piège** : traiter les deux demandes dans le désordre ou oublier l'une pendant que l'autre progresse — nécessité de garder les deux « en tête » via DB/particularisés/notes mentales structurées par la méthode.

### Scénario 3.3 — Enchaînement retour de STCA + relève imminente
**Situation** : Vous venez de gérer une situation d'urgence STCA (résolue). Il vous reste des directs à redonner, des W électroniques et DB à nettoyer sur les deux vols concernés. Une relève est prévue dans quelques minutes.
**Ce que vous devez faire** : (1) sécuriser complètement la situation immédiate (directs redonnés, DB supprimé, W désactivés), (2) reprendre une vision globale du secteur par un tour de suivi complet zone par zone, (3) préparer les éléments de relève : état des moyens, consignes particulières, gestion du trafic (y compris le fait qu'un STCA vient de se produire — élément important à transmettre), (4) s'assurer de l'acceptation de la relève par le contrôleur entrant.
**Pourquoi c'est un piège fréquent** : la tentation de « passer la main » trop vite sans nettoyer ni transmettre l'historique récent (notamment un événement de sécurité) peut faire perdre une information critique au contrôleur suivant.

---

# PARTIE XI — BANQUE DE QUESTIONS

## Questions de connaissance
1. Quelles sont les 5 étapes de la Méthode de Travail du CO ?
2. Quelles sont les 7 sous-étapes de la Résolution CR ?
3. Quel est le critère opérationnel (non réglementaire) utilisé en BSURV pour détecter un conflit potentiel ?
4. Quel est le minimum de séparation radar appliqué à l'ENAC et pourquoi ce chiffre est-il possible ?
5. Quelles sont les séparations verticales minimales en espace RVSM (équipé/non équipé) ?
6. Quelles sont les conditions LOA pour un transfert sous séparation radar avec Genève, Milan, Bordeaux, et les secteurs du même centre ?
7. Quelle est la limite de transfert de contrôle en entrée pour un départ LIML ?
8. Qu'est-ce qu'un FL refuge et dans quel cas est-il utilisé ?
9. Quelles sont les trois zones de valeur de distance de sortie (et actions associées) pour un vol évolutif sortant vers un même flux ?
10. Que signifie le halo cyan sur un RPS ?

## Questions de compréhension
11. Pourquoi le CR doit-il attendre que le CO ait acquitté son marqueur de 1ère analyse avant de démarrer la sienne ?
12. Pourquoi ne faut-il jamais cumuler une clairance de niveau et un transfert de fréquence dans le même message ?
13. Pourquoi un avion rapide nécessite-t-il une altération de cap plus faible qu'un avion lent pour un même effet de séparation à un instant donné — et pourquoi son verrouillage doit-il durer plus longtemps ?
14. Pourquoi la détection ne doit-elle jamais s'arrêter au premier conflit trouvé ?
15. Pourquoi le respect de la parité des routes est-il important ?

## Questions d'application
16. Vous êtes CO, un vol apparaît avec un XFL en désaccord avec l'ADES. Que faites-vous, dans quel ordre ?
17. Vous êtes CR, vous estimez une distance minimale de séparation de 4NM entre deux avions convergents dans 6 minutes. Que faites-vous ?
18. Vous êtes CO, un secteur adjacent non-interopérable vous demande d'accepter un vol à un niveau qui créerait un conflit à un niveau intermédiaire de sa montée. Que répondez-vous ?
19. Vous êtes CR, une arrivée LIML doit descendre mais un trafic au niveau plancher croise sa route à moins de 15NM. Décrivez votre séquence d'action complète.
20. Le STCA se déclenche sur deux avions que vous suiviez sans avoir mis en place de résolution. Que faites-vous immédiatement ?

## Questions pièges
21. Un CO détecte un conflit <15NM entre un départ LIML et un transit au plancher, mais les deux avions seront autorisés à des niveaux différents au moment considéré. Faut-il activer les W électroniques ? Faut-il quand même créer un DB ?
22. Un CR vient de verrouiller les caps de deux avions ; la distance entre eux a cessé de diminuer. Peut-il déjà déverrouiller ?
23. Un pilote collationne une fréquence légèrement différente de celle donnée. S'agit-il forcément d'une erreur de frappe du contrôleur ?
24. Un vol évolutif entre dans le secteur ; le CO n'a détecté aucun conflit au FL plancher. Le CR peut-il en conclure qu'aucune détection supplémentaire n'est nécessaire ?
25. Lors d'une résolution par guidage, l'avion tourné s'approche à 3NM de la frontière du secteur adjacent. Est-ce acceptable sans action supplémentaire ?

## Questions type oral
26. Expliquez en 30 secondes la différence entre EFL et CFL.
27. Expliquez la différence entre Assumable et Avancé.
28. Expliquez pourquoi un TR nécessite V1 ≥ V2.
29. Expliquez le rôle du DB dans le suivi de vol.
30. Expliquez pourquoi le marqueur de 1ère analyse CO est visible côté CR et non l'inverse.

## Questions type simu
31. Vous êtes CO, un vol évolutif entrant par le plancher présente un conflit <15NM avec un transit stable au même FL (et non au FL plancher). Ce cas relève-t-il de la méthode "vol évolutif" du Livret 8, ou d'une détection classique de vol stable ? Justifiez.
32. Vous êtes CR, un TR est en cours (silencieux, secteur interopérable) et un des deux avions demande soudain à changer de vitesse. Que devez-vous vérifier avant d'accorder ?
33. Vous êtes CO, un avion exempté RVSM doit sortir vers un secteur adjacent. Décrivez toutes les actions à ne pas oublier avant le transfert.

---

# CORRIGÉS — PARTIE XI

**1.** Intégration, Détection, Configuration de sortie, Marquage de fin de 1ère analyse, Suivi du vol (cycle continu) **[L1][L2][L3][L4]**.

**2.** (1) Déterminer le point de croisement ; (2) estimer qui arrive premier et la distance minimale ; (3) déterminer le cas (>15NM / 5-15NM / <5NM) et le type de résolution ; (4) élaborer la solution ; (5) décider du moment et agir ; (6) vérifier que la solution résout le conflit ; (7) déverrouiller en fin de guidage **[L5]**.

**3.** Une distance minimale estimée inférieure à 15NM au point le plus proche — seuil empirique, non réglementaire **[L2]**.

**4.** 5NM, rendu possible par le traitement multi-radar mono-pulse et le traitement des informations radar par le système à l'ENAC **[L4]**.

**5.** RVSM équipé/équipé : 1000ft. Non équipé vs tout autre : 2000ft. Au-dessus du FL410 : 2000ft pour tous **[L3]**.

**6.** Genève (G2/LSAG) : coordination téléphonique obligatoire, 10NM. Milan (M2/LIMM) : coordination téléphonique obligatoire, 10NM. Bordeaux (LFBB) : transfert radar silencieux, 10NM. Même centre ENAC : transfert radar silencieux, 10NM **[L7]**.

**7.** FL285 (limite entre RS/RU et RM) **[L8]**.

**8.** Le premier FL libre en dessous du FL demandé, respectant la parité, utilisé par le CR quand la distance de sortie sera <10NM et/ou vitesses non compatibles avec un TR **[L8]**.

**9.** >20NM : pas de TR, pas de FL refuge. 10-20NM avec vitesses compatibles : TR par verrouillage, pas de FL refuge. <10NM et/ou vitesses non compatibles : pas de TR, FL refuge maintenu **[L8]**.

**10.** Un vol exempté RVSM (exW) **[L3][L10]**.

**11.** Parce que l'analyse du CO peut encore modifier des éléments du vol (ex. changement d'EFL) ; le CR ne doit pas travailler sur des données susceptibles de changer **[L2]**.

**12.** Si le pilote comprend mal la clairance puis quitte immédiatement la fréquence, aucune correction rapide n'est possible — risque potentiellement extrêmement dangereux **[L9]**.

**13.** Un avion rapide s'écarte plus vite de sa trajectoire pour une même altération de cap donnée à un instant donné (moins d'altération nécessaire) ; mais comme il est rapide, il risque de rattraper l'avion lent une fois remis en navigation directe — d'où un verrouillage prolongé **[L6]**.

**14.** Parce qu'un conflit peut en cacher un autre ; en opérationnel, il est rare qu'un vol ne soit en conflit qu'avec un seul autre avion **[L4]**.

**15.** Pour éviter un face-à-face au même FL sur une même route (risque de collision frontale) **[L2]**.

**16.** Détecter et corriger l'incohérence pendant l'intégration (avant de poursuivre) : contacter le secteur transféreur si besoin de modifier l'EFL, ou modifier son propre XFL si la correction relève de son secteur ; seulement ensuite poursuivre vers la détection **[L1][L2]**.

**17.** <5NM ou incertitude → guidage : tourner au moins un avion, verrouiller l'autre (ou tourner les deux) ; agir suffisamment tôt (6 min ici) pour avoir le temps de vérifier l'efficacité **[L5][L6]**.

**18.** Refuser l'évolution au niveau intermédiaire concerné, maintenir la séparation verticale, informer le secteur demandeur que le niveau initial est maintenu, l'avion montera plus tard dans votre secteur **[L10]**.

**19.** Informer le CR, créer un DB partagé (avec le CO préalablement) ; assurer une séparation verticale (clairer initialement 1000ft au-dessus du trafic gênant) ; transférer l'avion en descente au plus tard en passant FL310 pour éviter un palier ; si palier inévitable, demander au CO une délégation de niveau à RM via la fonction FL? ; ne jamais cumuler clairance et transfert de fréquence **[L9]**.

**20.** Réagir immédiatement : altérations de cap fortes (min. 30°) sur les deux avions avec phraséologie d'urgence complète, informations de trafic si possible, puis remise en direct une fois la situation passée **[L10]**.

**21.** Non, pas de W électroniques nécessaires (pas de danger immédiat car niveaux d'autorisation différents) ; **oui**, un DB partagé doit être créé quand même, pour que le CR n'oublie pas ce conflit potentiel **[L8]**.

**22.** Non — il faut attendre que la distance **recommence à augmenter** (éloignement net confirmé), pas simplement qu'elle ait cessé de diminuer **[L4][L5]**.

**23.** Non — ce n'est pas forcément une erreur de frappe du contrôleur ; le pilote peut avoir mal collationné. D'où l'importance d'écouter attentivement chaque collationnement et de corriger via « Negative » si besoin **[L5]**.

**24.** Non — le CO ne détecte qu'au FL plancher ; c'est le **CR** qui est responsable de la détection sur **tous les FL intermédiaires** entre l'entrée et la sortie **[L8][L9]**.

**25.** Non, ce n'est pas acceptable sans action — le plot ne doit jamais s'approcher à moins de 2,5NM (moitié du minimum radar) des frontières sans coordination préalable avec le secteur concerné **[L5]**.

**26.** EFL = niveau d'entrée dans le secteur (affiché tant que le vol n'est pas assumé) ; CFL = niveau clairé, mis à jour à chaque nouvelle autorisation ; l'EFL devient le CFL au moment où le vol est assumé **[L1]**.

**27.** Assumable = le secteur précédent interopérable a déjà transféré le vol ; Avancé = le vol n'a pas encore été transféré, ses éléments sont simplement reçus **[L1]**.

**28.** Pour garantir que le premier avion ne soit jamais rattrapé par le second pendant le maintien de la séparation par vitesse — condition impérative des LOA de transfert sous séparation radar **[L7]**.

**29.** Le DB regroupe 2 à 6 vols concernés par une situation, donne une vision chronologique des situations à venir, et sert de rappel automatique (survol → vecteurs vitesse, halos bleus) pour ne pas oublier un conflit en cours pendant qu'on gère autre chose **[L1][L3]**.

**30.** Parce que le CR doit attendre la fin de la 1ère analyse du CO avant de commencer la sienne (les éléments du vol pouvant encore changer) — le marqueur lui sert donc de signal d'autorisation à démarrer **[L2]**.

**31.** Il s'agit d'une détection classique de vol stable (balayage latéral/longitudinal) — la méthode "vol évolutif" du Livret 8 concerne spécifiquement la détection restreinte au FL plancher pour le CO ; un conflit à un niveau différent du plancher relève du raisonnement classique de croisement stable **[L2][L8], déduction cohérente]**.

**32.** Vérifier que le changement de vitesse ne casse pas la condition V1≥V2 imposée par le TR en cours ; sinon, refuser ou ajuster **[L7]**.

**33.** Vérifier/confirmer la coordination téléphonique obligatoire de sortie avec le secteur suivant (car exW) avant tout transfert ; s'assurer que le CR ne transfère jamais un vol exW sans confirmation de cette coordination ; retirer tout particularisé/marquage résiduel ; nettoyer l'étiquette **[L3][L10]**.

---

# PARTIE XII — AUTOMATISMES (arbres décisionnels compacts)

**Intégration**
> Vol rose apparaît → Lire toute l'étiquette (G→D, ligne par ligne) → Vérifier parité EFL/route → Vérifier cohérence XFL/ADES → Incohérence ? → OUI : corriger avant de poursuivre / NON : mémoriser (indicatif, routes, FL, ACFT lent/rapide, actions à venir) → passer à Détection.

**Détection**
> Balayage latéral + longitudinal du flux → Vol trouvé au même FL/route croisée ? → NON : conflit écarté pour cette zone, continuer le balayage complet → OUI : marqueur 1ère analyse de l'autre vol acquitté ? → NON : terminer d'abord ma propre 1ère analyse, revenir ensuite → OUI : estimer distance minimale → <15NM ? → NON : pas de conflit → OUI : conflit → DB (+ W électroniques si danger imminent) → informer le collègue → **NE PAS S'ARRÊTER, continuer le balayage** (un conflit peut en cacher un autre).

**Résolution CR**
> Point de croisement → qui est premier, distance minimale corrigée de la vitesse → >15NM : surveillance / 5-15NM : verrouillage double / <5NM : guidage (tourner + verrouiller) → décider du moment (assez tôt) → agir (consulter cap → instruction → saisie IHM simultanée) → vérifier (vecteurs vitesse 3 min) → distance augmente ? → NON : attendre / OUI : déverrouiller (resume own navigation) + nettoyer DB/W.

**Vol évolutif entrant (départ)**
> CO détecte SEULEMENT au FL plancher → conflit ? → DB partagé (+ W si danger immédiat) → informer CR → **CR résout dans tous les cas** (séparation verticale, jamais de guidage) → CR détecte sur TOUS les FL intermédiaires jusqu'à la sortie.

**Vol évolutif sortant (arrivée)**
> CO détecte en entrée (vol stable croisé) + vérifie sortie (FL plancher) → CR détecte sur tous les FL intermédiaires → transfert au plus tard en passant FL310 → palier nécessaire ? → OUI : CO demande délégation FL à RM (fonction "FL ?") → NON : poursuite normale de la descente.

**Transfert sous séparation radar**
> Même route/FL, distance mesurée → >20NM ? → OUI : séparation réduite, rien à faire / NON (<20NM) : vérifier V1≥V2 → OK ? → NON : refuser toute demande incompatible / OUI : secteur interopérable et silencieux ? → OUI : verrouiller directement / NON : CO coordonne (indicatifs, FL, distance, Mach) → verrouiller vitesses → transfert de communication rapproché → lever restriction dès divergence confirmée.

**Urgence STCA**
> STCA se déclenche → **STOP tout le reste** → altération 30° minimum sur les deux avions, phraséologie d'urgence → info trafic → situation stabilisée ? → NON : continuer à surveiller intensivement / OUI : remise en direct sur point non pénalisant → reprendre suivi normal.

**Avant tout transfert de fréquence**
> Étiquette nettoyée ? (W électroniques off, DB supprimé, XFL=CFL, pas de h/s/r résiduel, pas de particularisé oublié) → coordination requise (exW, écart >5NM) déjà faite ? → OUI aux deux : transférer / NON : compléter d'abord.

---

# PARTIE XIII — CHECKLISTS MENTALES

## Checklist mentale courte (relecture avant simu)
- [ ] Lire, vérifier, mémoriser à chaque intégration.
- [ ] Balayer large (latéral + longitudinal), jamais s'arrêter au premier conflit.
- [ ] <15NM = DB systématique, même sans danger immédiat.
- [ ] Résoudre tôt, vérifier après.
- [ ] Vol évolutif = CO détecte au plancher seulement, CR détecte partout, jamais de guidage.
- [ ] Jamais cumuler clairance + transfert fréquence.
- [ ] Toujours écouter le collationnement.
- [ ] Étiquette nettoyée avant transfert.
- [ ] Informer systématiquement mon collègue après chaque détection/action.
- [ ] Tour de suivi régulier même en pleine gestion d'un conflit.

## « Les 30 secondes avant la simu »
1. Zones de travail en tête : LTP-E / GRENA-BOSUA / MTL-S / MEN-O / MINDI-NO / LSE-N.
2. Seuils : 15NM = conflit à traiter ; 5NM = minimum radar absolu ; 2,5NM = marge frontière secteur.
3. Réflexe : marqueur avant tout, DB avant d'oublier, informer avant d'agir seul.
4. En cas de doute sur une résolution : verrouiller d'abord, décider ensuite — ne jamais laisser filer sans action minimale de sécurité.

## « Quand je commence à être débordé »
1. **Sécurité d'abord** : y a-t-il un STCA ou une situation à <5NM imminente ? Traiter en priorité absolue.
2. Revenir aux **zones de travail** une par une, méthodiquement, plutôt que de sauter d'un avion à l'autre.
3. Utiliser le **DB** comme mémoire externe — ne pas essayer de tout retenir seul.
4. Informer mon collègue à voix haute de ce qui est en cours (ancrage verbal = ancrage mental).
5. Terminer une méthode avant d'en commencer une autre autant que possible (éviter les 1ères analyses simultanées).

---

# PARTIE XIV — FICHE DE SURVIE CO

**Méthode CO (1ère analyse)** : Intégration (lire/vérifier/mémoriser) → Détection (balayage latéral+longitudinal, <15NM=conflit) → Configuration sortie (remontée des flux convergents) → Marquer fin 1ère analyse → Suivi continu.

**Méthode CR (résolution)** : Point croisement → qui premier/distance mini → cas (>15/5-15/<5NM) → agir tôt → vérifier (VV 3min) → déverrouiller à l'éloignement confirmé.

**Séparations** : radar 5NM · conflit à traiter <15NM · RVSM 1000ft (équipé/équipé) sinon 2000ft · au-dessus FL410 2000ft · frontière secteur 2,5NM minimum pour un plot guidé.

**Vols évolutifs (LIML)** : CO détecte SEULEMENT au plancher ; CR détecte TOUS les FL intermédiaires ; résolution CR = séparation verticale uniquement (jamais de guidage) ; transfert en descente avant FL310 ; FL refuge si sortie <10NM ou vitesses incompatibles.

**TR (radar handover)** : <20NM → verrouiller vitesses, V1≥V2 ; LOA : G2/M2 coordination tel. 10NM ; LFBB et intra-ENAC silencieux 10NM.

**Communication** : jamais clairance+transfert ensemble · toujours écouter collationnement · consulter cap avant instruction · informer systématiquement le collègue.

**Urgence STCA** : stop tout → 30° mini sur les deux avions → info trafic → remise en direct après stabilisation.

**Avant transfert** : étiquette nettoyée (W off, DB supprimé, XFL=CFL, pas de h/s/r) + coordinations dues (exW, écart >5NM) faites.

**Réflexe ultime** : « Un conflit peut en cacher un autre. Le DB porte ma mémoire. J'informe toujours mon collègue. »

---

# PARTIE XV — PLAN DE RÉVISION

## Priorité 1 — À maîtriser absolument
- Méthode CO en 5 étapes + méthode CR en 5 étapes / résolution en 7 sous-étapes.
- Critère de conflit 15NM et logique de calcul du point de croisement.
- Table de décision résolution (>15 / 5-15 / <5NM).
- Vols évolutifs : répartition de détection CO (plancher) vs CR (tous niveaux intermédiaires), résolution uniquement verticale.
- Règle absolue « jamais clairance + transfert fréquence ».
- Réaction STCA.
*À comprendre → à mémoriser → à pratiquer (scénarios niveau 1-2) → à automatiser (répétition phraséologie + calculs mentaux de croisement).*

## Priorité 2 — À très bien connaître
- Conditions et LOA de transfert sous séparation radar (G2/M2/LFBB/intra-ENAC).
- FL refuge et les 3 cas de distance de sortie.
- Coordination : règle « éléments déjà passés / pas encore passés » et ses conséquences.
- Séparations verticales RVSM et exW.
- Fonctions IHM : MVT, FL?, MONTRER/SHOW, NOTEPAD.
*À comprendre → à mémoriser → à pratiquer (scénarios niveau 2-3).*

## Priorité 3 — À connaître, moins critique en pression immédiate
- Zones de travail précises et balises secondaires (FREDI, SANTO, LANZA, MOZAO, SPIDY, BOSUA).
- Détails de relève (handover).
- Historique/contexte pédagogique (structure UCE, CDS).
*À comprendre → à mémoriser.*

---

# PARTIE XVI — MODE ENTRAÎNEMENT INTERACTIF

Ce manuel est prêt à servir de base à deux modes interactifs, disponibles à la demande :

**« Lance-moi une simu »** — je vous donnerai une situation de contrôle réaliste (basée sur les scénarios de la Partie X et leurs variantes), sans révéler la solution ; vous prendrez vos décisions ; je ferai évoluer le trafic en fonction de vos réponses, j'introduirai progressivement de la charge et des événements inattendus (nouveaux vols, demandes pilotes, révisions de secteurs adjacents, éventuellement un STCA si une résolution est oubliée), puis j'évaluerai vos décisions et expliquerai après coup ce qui était correct ou non, en citant la règle source.

**« Fais-moi passer un test blanc »** — un test mélangeant connaissances, méthodes, situations, pièges, anticipation, priorisation et récupération après erreur, sans réponses données en cours de route ; à la fin : score, erreurs, notions mal maîtrisées, méthodes à retravailler, niveau de préparation estimé, recommandations de révision ciblées sur la Partie XV.

---

# CONTRÔLE QUALITÉ FINAL

- Les 10 livrets ont été analysés intégralement (contenu ENONCE + REPONSES).
- Les méthodes CO, CR, TR, vols évolutifs (entrée et sortie), révision de niveau en entrée, urgence STCA et relève sont toutes couvertes avec leurs procédures détaillées.
- Les nuances et cas particuliers (FL refuge, 3 cas de distance TR, différentiel de vitesse en guidage, coordination selon éléments déjà passés/non passés) ont été conservés tels quels, sans simplification abusive.
- Les points où les livrets ne précisent pas explicitement un détail (ex. nom exact de la « 5ème étape » du CO dans L3) sont signalés comme tels plutôt que comblés par une invention.
- Ce manuel est directement exploitable comme support principal de révision ; il peut être complété conversationnellement via les modes « simu » et « test blanc » de la Partie XVI.
