# Aknur Sherkhan - Data Science & ML Portfolio

[LinkedIn](https://linkedin.com/in/aknursherkhan) · aknur@uni.minerva.edu

---

## Projects

### [Kazakh-Russian Speech Classifier](https://github.com/aknursherkhan/kazakh-russian-speech-classifier)
Language identification from raw audio. Trained on personal voice messages augmented with Google FLEURS; used `GroupShuffleSplit` to prevent data leakage across recordings. Three modeling approaches: logistic regression baseline, CNN on 2D MFCC representations, and an Attentional BiLSTM with Bahdanau attention. Also includes an unsupervised Seq2Seq autoencoder experiment to test whether latent representations naturally separate by language without labels.

`PyTorch` · `librosa` · `Bahdanau attention` · `Seq2Seq autoencoder` · `MFCC` · `SpecAugment`

---

### [Postability Scorer](https://github.com/aknursherkhan/mini-capstone)
Ranks photos from your camera roll by how likely you are to post them on Instagram, based on your actual posting history. V1 used binary classification and had decent ROC-AUC but failed in practice because the model learned file format differences between Instagram-compressed JPEGs and raw camera files rather than aesthetic taste. V2 scrapped labels entirely: CLIP embeddings cluster your posting history by visual style, and six engineered quality features are normalized to your own posting standards rather than a universal benchmark.

`CLIP` · `PyTorch` · `KMeans` · `OpenCV` · `scikit-learn`

---

### [Urban Traffic Congestion Simulation](https://github.com/aknursherkhan/urban-traffic-simulation)
Discrete-event traffic simulator built on real OpenStreetMap road networks. Cars navigate via shortest-time Dijkstra routing with dynamic congestion-aware rerouting; speed follows the Greenshields linear speed-density model. Validated across two cities (Berlin, Buenos Aires) with 50 independent Monte Carlo runs each. Main finding: edge betweenness centrality predicts peak congestion with Spearman r = 0.93 across both cities, making it a practical proxy for identifying bottleneck roads without running a full simulation.

`OSMnx` · `NetworkX` · `Greenshields model` · `Monte Carlo` · `Dijkstra`

---

### [Airport Security Queue Simulation](https://github.com/aknursherkhan/airport-security-simulation)
Discrete-event simulation of airport security screening built from scratch in object-oriented Python: Poisson arrivals, truncated-normal service times, k parallel queues with shortest-queue routing, and an extended model where 3% of travelers trigger secondary screening by a single senior officer (blocking their primary queue while under inspection). Results validated against the Pollaczek-Khinchin formula across station counts k = 5 to 15.

`NumPy` · `SciPy` · `M/G/k queueing theory` · `Pollaczek-Khinchin`

---

### [Bayesian Analysis of Argentine Football Attendance](https://github.com/aknursherkhan/bayesian-football-attendance)
Hierarchical Bayesian model of match attendance across 240 Argentine Primera Division games. Compares complete pooling vs. partial pooling with team and day-of-week random effects; model selection via Pareto-smoothed LOO-CV. Justified Negative Binomial over Poisson due to overdispersion, and resolved MCMC divergences by switching to non-centered reparametrization. Includes posterior predictive imputation for 22 games with missing attendance data.

`PyMC` · `ArviZ` · `PSIS-LOO` · `Negative Binomial` · `hierarchical modeling`

---

### [Predator-Prey Reaction-Diffusion Simulation](https://github.com/aknursherkhan/predator-prey-simulation)
Fox-bunny ecosystem on a 200x200 spatial grid. Logistic prey growth, hunting, and stochastic predator mortality operate locally while both populations diffuse via periodic boundary conditions. Parameter sweeps over fox growth rate identify two phase boundaries and a stochastic phase transition near the upper stability limit. Separate analysis of fox diffusion rate shows predator mobility reshapes spatial clustering without destabilizing global population balance.

`NumPy` · `Matplotlib` · `reaction-diffusion modeling` · `phase transition analysis`
