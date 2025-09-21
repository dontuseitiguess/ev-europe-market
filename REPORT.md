## 1. Contexte & Objectifs

- L’Europe est un marché clé pour l’électrification automobile (BEV, PHEV).  
- Les constructeurs premium (Porsche, BMW, Mercedes, Audi) et les groupes luxe (LVMH via mobilité durable) scrutent ces tendances.  
- Objectif : fournir une **analyse claire et chiffrée** sur :
  - les pays leaders,
  - la dynamique BEV vs PHEV,
  - la transition vs Diesel/Petrol,
  - un scénario de prévision 2030.

## 2. Données & Méthodologie

- Source : **Eurostat – road_eqr_carpda** (new passenger car registrations by fuel type).  
- Période : **2015 → 2023** (focus post-2015 pour refléter l’accélération EV).  
- Périmètre : pays européens + UE total.  
- Motorisations retenues :
  - **BEV** (Battery Electric Vehicles)
  - **PHEV** (Plug-in Hybrid)
  - **HEV** (Hybrid)
  - **Petrol**
  - **Diesel**
  - **Other** (LPG, CNG, H2, etc.)
- Pipeline :
  1. **Préparation des données** (Eurostat TSV → CSV propre).  
  2. **EDA** (Top pays, évolution UE, mix motorisations).  
  3. **Prévision 2030** (régression linéaire sur log des immatriculations).  

## 3. Insights Clés (EDA)

### a) Pays leaders (2023)
- **Allemagne, France, UK, Norvège, Pays-Bas** dominent les ventes BEV+PHEV.
- Les pays nordiques (Norvège, Suède) affichent des taux d’adoption spectaculaires (>80% EV en parts de marché).

### b) Transition énergétique
- **Diesel en chute libre** depuis 2015.
- **Petrol** reste important mais recule au profit des BEV.
- Les **HEV** et **PHEV** jouent un rôle de transition.

### c) Mix 2023
- BEV ~20–25% des immatriculations UE.  
- PHEV ~7–10%.  
- Diesel <15% (vs >50% en 2015).  

## 4. Prévision 2030

- Modèle : **régression linéaire (log1p)** sur immatriculations UE (2015–2023).
- Scénarios : **base**, **low (-20%)**, **high (+20%)**.
- Résultats (UE total, scénario base) :
  - **BEV :** ~4–5M en 2030 (vs 0.86M en 2015).  
  - **PHEV :** croissance mais plateau relatif (~1–1.5M en 2030).  
- CAGR 2023–2030 :
  - **BEV :** +XX% par an (forte croissance).  
  - **PHEV :** +YY% par an (croissance plus modérée).  

📊 Voir : `dashboard/forecast_bev_phev.png`

## 5. Implications Business

- **Constructeurs premium (Porsche, BMW, Mercedes, Audi) :**
  - BEV devient le **core product** d’ici 2030.
  - Les PHEV servent de **gamme de transition** mais doivent être progressivement réduits.

- **Luxe & image (LVMH, Richemont, etc.) :**
  - Associer l’image luxe à la **mobilité 100% électrique** (brand value + sustainability).
  - Opportunité de partenariats “green mobility”.

- **Politiques publiques :**
  - Soutien BEV indispensable (infrastructures recharge, subventions).
  - Diesel pratiquement hors marché en 2030.

- **Marchés clés à surveiller :**
  - **Allemagne, France, UK, Norvège, Pays-Bas** (leaders BEV).
  - Pays d’Europe de l’Est → potentiel de rattrapage.

## 6. Limitations & Next Steps

- Modèle simple (linéaire) → ne capture pas toutes les dynamiques marché.
- Pas encore d’analyse par segments (SUV, compact, premium).
- Prévisions sensibles aux politiques publiques et infrastructures.
- Prochaines étapes possibles :
  - Utiliser des modèles **non-linéaires (exponential, ARIMA, Prophet)**.
  - Focus **par pays** (DE, FR, UK, NO).
  - Intégrer des données **prix / parts de marché / émissions CO₂**.

## 7. Conclusion

- L’Europe est engagée dans une **transition rapide vers le BEV**.  
- Les PHEV resteront transitoires, mais la tendance est claire :  
  **2030 = décennie 100% électrique** pour le marché premium.  
- Opportunités business majeures pour les constructeurs et le luxe :  
  investir dès maintenant dans la mobilité zéro-émission.
