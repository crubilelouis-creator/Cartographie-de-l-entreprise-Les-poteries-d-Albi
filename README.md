# Cartographie-de-l-entreprise-Les-poteries-d-Albi
```mermaid
flowchart TB

%% PROCESSUS DE PILOTAGE
PILOTAGE["PROCESSUS DE MANAGEMENT / PILOTAGE<br/>• Direction générale<br/>• Direction adjointe<br/>• Définition de la stratégie<br/>• Pilotage financier<br/>• Politique qualité"]
AMELIORATION["Amélioration continue<br/>• Suivi indicateurs<br/>• Actions correctives"]

PILOTAGE --> AMELIORATION

%% PROCESSUS DE REALISATION
subgraph REALISATION["PROCESSUS DE RÉALISATION (CŒUR DE MÉTIER)"]

  subgraph COMMERCIAL["Processus commercial"]
    C1["Prospection B2B"]
    C2["Analyse du besoin client"]
    C3["Devis & négociation"]
    C4["Validation commande"]
    C1 --> C2 --> C3 --> C4
  end

  subgraph PRODUCTION["Processus de production artisanale"]
    P1["Tournage"]
    P2["Séchage"]
    P3["Émaillage"]
    P4["Patine"]
    P5["Enfournement"]
    P6["Cuisson"]
    P7["Contrôle qualité"]
    P1 --> P2 --> P3 --> P4 --> P5 --> P6 --> P7
  end

  subgraph LOGISTIQUE["Logistique & livraison"]
    L1["Préparation commandes"]
    L2["Montage palettes"]
    L3["Expédition"]
    L4["Livraison client B2B"]
    L1 --> L2 --> L3 --> L4
  end

  COMMERCIAL --> PRODUCTION --> LOGISTIQUE

end

%% PROCESSUS SUPPORT
subgraph SUPPORT["PROCESSUS SUPPORT"]
  S1["Ressources humaines (RH externalisée)"]
  S2["Comptabilité / Finance"]
  S3["Achats & approvisionnement"]
  S4["Administration"]
  S5["Maintenance fours & équipements"]
end

%% FLUX
PILOTAGE --> REALISATION
SUPPORT --> REALISATION

CLIENTS["Besoins clients B2B<br/>Jardineries • GSB • Distributeurs"]
SATISFACTION["Satisfaction clients<br/>Qualité • Délais • Fiabilité"]

CLIENTS --> REALISATION
REALISATION --> SATISFACTION
