# 🎤 Phonétique et Synthèse de la parole

**Auteur :** Hamizi Tannnina  
**Numéro étudiant :** 22207593  

---

## 📌 Description du projet

Ce projet s’inscrit dans le cadre du cours de **Phonétique et Synthèse de la parole**.  
L’objectif est de mettre en place un système de **synthèse vocale à partir de diphones**, en utilisant l’outil **Praat**.  

Le travail comprend :  

- La création d’un **dictionnaire phonétique** (`dico2.txt`) contenant les transcriptions nécessaires.  
- L’enregistrement et la segmentation d’un ensemble de **logatomes** permettant de couvrir les combinaisons phonétiques utiles.  
- La génération d’un **fichier TextGrid** (`chain.TextGrid`) pour annoter et segmenter le signal sonore (`chain.wav`).  
- L’écriture d’un **script Praat** (`script_hamizi.praat`) afin d’automatiser la concaténation des diphones et produire des phrases complètes.  
- La production d’un **fichier de sortie audio** (`phrase_synthetiser.wav`) qui correspond à la phrase synthétisée.  

---

## 📂 Contenu du dépôt

- `README.md` – documentation du projet  
- `script_hamizi.praat` – script de synthèse Praat  
- `dico.txt` – dictionnaire phonétique  
- `chain.TextGrid` – segmentation en diphones  
- `chain.wav` – enregistrement initial  
- `phrase_synthetiser.wav` – résultat de la synthèse  

---

## 📝 Choix des mots et des phrases

Les phrases ont été construites à partir de scènes de la vie quotidienne.  
Deux ensembles de mots ont été utilisés :  

- **Mots pleins :** dame, danseuse, seule, perdue, accompagnée, gare, rue, jeune  
- **Mots grammaticaux :** la, est, dans  

**Exemples de phrases générées :**

- La jolie dame est accompagnée.  
- La méchante dame est perdue.  
- La jeune dame.  
- La jolie danseuse.  
- La dame est seule dans la gare.  
- La jolie dame est perdue dans la rue.  
- La dame est perdue.  
- La jolie dame est perdue dans la gare.  
- La danseuse est méchante.  

👉 Un **tier spécifique** a été créé dans Praat afin de segmenter les logatomes en **diphones**.  
👉 **Nombre total de diphones enregistrés :** 194  

---

## ⚙️ Méthodologie

1. **Enregistrement sonore** (`chain.wav`) : production d’un corpus de logatomes.  
2. **Segmentation** avec Praat (`chain.TextGrid`) : annotation des diphones.  
3. **Création du dictionnaire phonétique** (`dico2.txt`) :  
   - transcription phonétique adaptée,  
   - gestion de certaines variantes,  
   - ajout de mots manquants (*ex. : « est » → /e/*).  
4. **Écriture du script Praat** (`script_hamizi.praat`) pour :  
   - concaténer les diphones selon les séquences,  
   - générer les phrases définies,  
   - sauvegarder le fichier final (`phrase_synthetiser.wav`).  
5. **Évaluation et ajustements** : corrections sur les diphones mal enregistrés, ajustement de la fréquence, tentative d’amélioration prosodique.  

---

## 🛠️ Problèmes rencontrés & solutions

### 🔤 Dictionnaire
- **Modifications de transcriptions :**  
  - `dans` : `da~` → `dA`  
  - `accompagnée` : `aKo~panje` → `aKCpanje` → `aKCpaJe`  
- **Ajout de mots :**  
  - *« est »* (/e/) ajouté manuellement.  

### 🎙️ Synthèse
- Problème avec le mot *« est »* :  
  - parfois absent dans le rendu sonore malgré sa présence dans le TextGrid,  
  - parfois affiché mais non produit à l’écoute.  

### 🔊 Qualité sonore
- Fichier initial à **45 kHz** converti en **44.1 kHz** pour compatibilité.  
- Certaines phrases trop rapides → nécessité de ralentir le tempo.  

### 📈 Prosodie
- Tentative d’intégrer la gestion de **f0** et **durée** via une boîte de dialogue.  
- Problème de condition (`if`) empêchant l’activation correcte.  
- Solution : ajout manuel des modifications prosodiques, sans automatisation.  

---

## 🚀 Utilisation

1. Ouvrir **Praat**.  
2. Charger les fichiers nécessaires :  
   - `dico.txt`  
   - `chain.TextGrid`  
   - `chain.wav`  
3. Exécuter le script :  
   ```bash
   script_hamizi.praat
4. Résultat attendu :
un fichier de sortie audio → phrase_synthetiser.wav.
