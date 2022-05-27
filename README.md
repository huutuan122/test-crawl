# Data Processing for Weather

A branch in [ntduoc100/demeter: It works on my machine (github.com)](https://github.com/ntduoc100/demeter), used to crawl data, preprocess, update, train and predict for a weather project.

To run this project, follow my steps:

- First run 3 files `dataCollecting.py `, `dataPreprocessing.py `and `dataUploading.py` step by step, which was specified in './github/workflows/crawlData.yml'
- Next, run `dataModelling.py` to get coefficient for model, which was used in the next phase.
- Finally, run `dataPredicting.py` to forecast weather data.

# Description
- `dataCollecting.py` used to collect data from free.meteo.com
- `dataPreprocessing.py` used to clean data, save them to a folder.
- `dataUploading.py`used to upload data to mongoDB server.
- `dataModelling.py` used to train model, find the best coefficient for predicting phase.
- `dataPredicting.py` used to forecast weather for each province in VietNam.
- `./github/workflow`: Each file in this foler will run each time you commit. To disable this, go to `Action` and choose the file you want to disable. Then, click Disable workflow`
  - `crawlData.yml`: used to crawl data using github action. To run this, go to `Action` and click `Enable workflow`
  - `getCoefficient.yml`: used to automatically get coefficient. This file run automatically each weak.
  - `automaticallyPredict.yml`: used to automatically predict. This file run automatically each hour.

# License

Demeter team - Grab VietNam's Tech Bootcamp 202
