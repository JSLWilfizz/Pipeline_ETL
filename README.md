# Pipeline_ETL


To use JANNICA we need to put in folder JANICCA/data a .csv formating by date,Central,Tecnology, divide data by year in the differents folders, If is necessary create a new folder with another year.

In atributes_for_data/data.yaml:

  # Change columns names to use to prepare data
  central_name : Codigo Central
  date: Date
  generation: Generacion_MWh
  tecnology: Tecnologia

  work: (Build or Predict) # Use Build to make a model , or Predict to use a existing model 

  ignore_zone: (True or False, to specify if model was by zone(False)  or Tecnology(True))

  objetive_energy: (Fossil or Renewable or Both)
  objetive_zone : (Here is necessary put a specific zone or all)
  objetive_year: 2050 # Year to predict


  to_sum: If exist tecnology than have different names and are the same type 
    - Hidráulica de Pasada
    - Hidráulica de Embalse
    - Mini Hidráulica de Pasada

  energy: 
    Renewable: # Specify type of Energy
      - Hidráulica de Pasada
      - Eólica
      - Solar Fotovoltaica
      - Cogeneración
      - Geotermica
      - Hidráulica de Embalse
      - Mini Hidráulica de Pasada


    Fossil: # Specify type of Energy
      - Biomasa
      - Carbón
      - Gas Natural
      - Petróleo Diesel

  zones: # How zone are classify 
    Norte: # Macrozone
      - Región de Atacama #State
      - Región de Coquimbo #State
      - Región de Antofagasta #State 
      - Región de Arica y Parinacota #State

    Centro:
      - Región de Valparaíso #State
      - Región del Maule #State
      - Región de Ñuble #State
      - Región Metropolitana de Santiago #State
      - Región del Libertador Gral. Bernardo O’Higgins #State
    Sur:
      - Región del Biobío #State
      - Región de la Araucanía #State
      - Región de Los Ríos #State
      - Región de Los Lagos #State
