# ogr2ft
ogr2ft tool copies features from any OGR data source to Google Fusion Table.

### Usage

```
usage: ogr2ft.py [-h] -i INPUT_FILE -o OUTPUT_FUSION_TABLE [-a]                   
                                                                                  
Uploads a given feature collection to Google Fusion Table.                        
                                                                                  
optional arguments:                                                               
  -h, --help            show this help message and exit                           
  -i INPUT_FILE, --input-file INPUT_FILE                                          
                        input feature source (KML, SHP, SpatiLite, etc.)          
  -o OUTPUT_FUSION_TABLE, --output-fusion-table OUTPUT_FUSION_TABLE               
                        output Fusion Table name                                  
  -a, --add-missing     add missing features from the last inserted feature       
                        index                                                     
```

### Example Run

```

python ./ogr2ft.py -i ../input.kml -o test_fusion_table
Creating Fusion Table: test1
Inserted 200 of 9420 features (2.12%)
Inserted 400 of 9420 features (4.25%)
Inserted 400 of 9420 features (4.25%)
Inserted 800 of 9420 features (8.49%)
Inserted 800 of 9420 features (8.49%)
Inserted 1200 of 9420 features (12.74%)
Inserted 1400 of 9420 features (14.86%)
Inserted 1400 of 9420 features (14.86%)
Inserted 1600 of 9420 features (16.99%)
Inserted 1800 of 9420 features (19.11%)
Inserted 2000 of 9420 features (21.23%)
Inserted 2200 of 9420 features (23.35%)
Inserted 2400 of 9420 features (25.48%)
Inserted 2600 of 9420 features (27.60%)
Inserted 2800 of 9420 features (29.72%)
Inserted 3000 of 9420 features (31.85%)
Inserted 3200 of 9420 features (33.97%)
Inserted 3400 of 9420 features (36.09%)
Inserted 3600 of 9420 features (38.22%)
Inserted 4000 of 9420 features (42.46%)
Inserted 4200 of 9420 features (44.59%)
Inserted 4400 of 9420 features (46.71%)
Inserted 4600 of 9420 features (48.83%)
Inserted 4800 of 9420 features (50.96%)
Inserted 5000 of 9420 features (53.08%)
Inserted 5200 of 9420 features (55.20%)
Inserted 5600 of 9420 features (59.45%)
Inserted 5600 of 9420 features (59.45%)
Inserted 5800 of 9420 features (61.57%)
Inserted 6000 of 9420 features (63.69%)
Inserted 6200 of 9420 features (65.82%)
Inserted 6400 of 9420 features (67.94%)
Inserted 6600 of 9420 features (70.06%)
Inserted 6800 of 9420 features (72.19%)
Inserted 7000 of 9420 features (74.31%)
Inserted 7200 of 9420 features (76.43%)
Inserted 7400 of 9420 features (78.56%)
Inserted 7600 of 9420 features (80.68%)
Inserted 7800 of 9420 features (82.80%)
Inserted 8000 of 9420 features (84.93%)
Inserted 8200 of 9420 features (87.05%)
Inserted 8600 of 9420 features (91.30%)
Inserted 8600 of 9420 features (91.30%)
Inserted 8800 of 9420 features (93.42%)
Inserted 9200 of 9420 features (97.66%)
Inserted 9400 of 9420 features (99.79%)
Inserted 9420 of 9420 features (100.00%).
```

### Known Issues
* Inserted row messages prints the same message from time to time, it looks like previous transaction is still busy 
  while new inserts occur. The final table seems to be ok.
