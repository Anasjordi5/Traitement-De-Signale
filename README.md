# Traitement-De-Signale
Main project: signal processing lab using Python to study sampling, spectra, aliasing, and ideal low‑pass reconstruction of multi‑sinusoidal signals via numerical experiments and plots.​  Travail supp: configurable spectral analysis tool that shows sampled spectrum, aliasing, and LPF‑recovered components for any chosen sinusoidal signal.

# Spectral Analysis of Sampled Signals (Exercises 1–4)      

This project focuses on the **spectral analysis of continuous-time signals after sampling**, with an emphasis on understanding **frequency replication, aliasing, and signal recovery using ideal low-pass filters (LPF)**.  
All signals are defined using **explicit sinusoidal components and DC terms**, which allows precise control of amplitudes and frequencies and ensures physically correct spectra.

### Exercise 1 – Single-Component Signal (No Aliasing)
The first exercise studies a signal composed of a **single cosine component**.  
The sampling frequency satisfies the **Shannon sampling theorem**, so no aliasing occurs.  
The sampled spectrum shows periodic replicas at multiples of the sampling frequency, and an ideal LPF perfectly recovers the original signal.  
This exercise establishes the basic concepts of sampling and spectral replication.

### Exercise 2 – Two-Component Signal (No Aliasing)
The second exercise extends the analysis to a signal containing **two frequency components**.  
The sampling frequency is still high enough to avoid aliasing.  
The spectrum shows replicas of both components around multiples of the sampling frequency, while the LPF correctly preserves all original frequencies.  
This exercise highlights how multiple components coexist in the sampled spectrum without distortion.

### Exercise 3 – Two-Component Signal with Aliasing
In the third exercise, one frequency component exceeds the **Nyquist frequency**, causing **aliasing**.  
The sampled spectrum clearly shows the high-frequency component folding back into the baseband.  
After low-pass filtering, the recovered signal differs from the original, demonstrating that **aliasing is irreversible** once it occurs.  
This exercise illustrates the practical consequences of undersampling.

### Exercise 4 – Multi-Component Signal with DC Term
The fourth exercise analyzes a more complex signal containing a **DC component and multiple sinusoidal frequencies**.  
Both **unilateral and bilateral spectra** are examined to compare their representations.  
Aliasing effects are identified, and the impact of an LPF on the recovered signal is studied.  
This exercise provides a complete view of sampling behavior, aliasing symmetry, and amplitude distribution in real signals.


# Analyse Spectrale et Échantillonnage de Signaux

## Description du Projet
Ce dépôt contient des outils d'analyse spectrale pour l'étude de signaux échantillonnés, développés dans le cadre d'un projet de traitement du signal. L'objectif principal est de comprendre le comportement des signaux continus lors de l'échantillonnage, d'identifier les phénomènes d'aliasing (repliement) et de simuler la reconstruction via des filtres idéaux.

## Fonctionnalités Clés
- **Génération de Signaux Personnalisés** : Définition de signaux à partir de composantes sinusoïdales (fréquence et amplitude) et d'un terme continu (DC).
- **Analyse de l'Échantillonnage** : Calcul automatique du spectre échantillonné en fonction d'une fréquence d'échantillonnage ($f_s$) définie par l'utilisateur.
- **Détection de l'Aliasing** : Identification automatique du non-respect du théorème de Shannon ($f_s < 2f_{max}$) et visualisation des répliques spectrales.
- **Filtrage de Reconstruction** : Simulation d'un filtre passe-bas (LPF) idéal pour récupérer le signal original, avec correction automatique des gains d'amplitude.
- **Visualisations Avancées** :
    - Affichage du spectre bilatéral (fréquences positives et négatives).
    - Graphiques comparatifs entre le spectre échantillonné et le spectre récupéré.

## Exemples d'Analyse
Le projet traite différents scénarios, notamment :
1. **Signal à une composante** : Étude du signal $x(t) = 5 \cos(2\pi \cdot 1000 \cdot t)$ avec $f_s = 8000$ Hz, démontrant un cas sans aliasing.
2. **Signal multi-composantes** : Analyse d'un signal complexe composé de fréquences à 2000, 4000 et 6000 Hz, permettant d'observer l'impact de l'aliasing lorsque la fréquence maximale dépasse $f_s/2$.


## Dépendances
- Python 3.x
- NumPy (calcul numérique)
- Matplotlib (visualisation des spectres)

### Key Concepts Covered
- Bilateral and unilateral spectra  
- Frequency replication due to sampling  
- Shannon sampling theorem  
- Aliasing and spectral folding  
- Ideal low-pass filtering and signal recovery  
- Correct amplitude handling (DC and sinusoidal components)

This project provides a clear and visual understanding of how sampling affects signals in the frequency domain and why proper sampling conditions are critical in signal processing.
