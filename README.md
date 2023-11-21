# Modèle de Simulation pour véhicule hybride hydrogène-batterie

Ce projet comprend un script Python (`script.py`) qui effectue des simulations du modèle de véhicule en fonction des paramètres d'entrée fournis. Les résultats de ces simulations sont sauvegardés dans un fichier JSON (`simulations.json`). Un notebook Jupyter (`results.ipynb`) est également fourni pour analyser et visualiser les résultats des simulations.

## Utilisation

### 1. Execution des simulations

Exécutez le script script.py pour lancer une simulation. Modifiez les variables de ce fichier pour en modifier les paramètres d'entrée 
Les résultats des simulations seront enregistrés dans le fichier simulations.json.

### 2. Structure des résultats

Une simulation est sauvegardée sous forme d'un dictionnaire à l'allure suivante :

{
        "Asservissement": "BAT",
        "Trajet": "CityBus_AT_PS_UrbanDeliveryHighLoad.csv",
        "Rendement moteur": 0.9,    #en kW
        "Coef montee PAC": 0.05,    
        "Coef descente PAC": 0.1,   
        "Charge min PAC": 0.2,  #entre 0 et 1
        "Charge max PAC": 0.95, #entre 0 et 1
        "Capacite PAC": 302,    #kW
        "Tension batterie": 600,    #V
        "Coef perte I decharge": 1.01,
        "Coef perte I charge": 0.99,
        "Rendement recuperation energie": 1,
        "dm_bat": 0.2,  #kWh/kg
        "dv_bat": 0.4,  #kWh/L
        "dp_bat": 10,   #kW/kWh
        "dm_pac": 1,    #kW/kg
        "dv_pac": 1,    #kW/L
        "dm_h2": 33,    #kWh/kg
        "dv_h2": 1.6,   #kWh/L
        "dm_h2_stocke": 1.9,    #kWh/kg
        "dv_h2_stocke": 1.2,    #kWh/L
        "c_elec": 0.2,  #euros/kWh
        "c_h2": 10,     #euros/kg
        "c_pac": 300,   #euros/kW
        "c_bat": 46,    #euros/kWh
        "c_reservoir_h2": 500,  #euros/kg
        "t_trajets": 8, #heures
        "n_trajets": 8.821965026544927,
        "E_tot_moteur": 30.821850012683964, #kWh
        "E_PAC_conso": 94.44963796935318,   #kWh
        "E_BAT_fin": -30.821850012683964,   #kWh
        "E_BAT_max": 30.82527397732501, #kWh
        "E_BAT_min": 0.0,   #kWh
        "E_tot": 125.27491194667819,    #kWh
        "P_max": 194.51166666666666,    #kW
        "P_moy": 33.9886603581639,  #kW
        "P_moy_pac": 60.409276712816364,    #kW
        "P_max_bat": 194.51166666666666,    #kW
        "Taux_PAC": 1.777336207906952,
        "Capacite_BAT": 180,    #kWh
        "Masse": 1640.5428436502439,    #kg
        "Volume": 1446.3595024462197,   #L
        "Cout installation": 111504.7182262949, #euros
        "Cout batterie": 8280,  #euros
        "Cout PAC": 90600,  #euros
        "Cout reservoir": 12624.718226294903,   #euros
        "Cout electricite": 0,  #euros
        "Cout hydrogene": 252.49436452589808    #euros
    }

### 3. Exploitation des résultats

Ouvrez le notebook Jupyter results.ipynb pour explorer et analyser les résultats des simulations.

jupyter notebook results.ipynb
