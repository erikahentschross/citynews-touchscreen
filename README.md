# CityNews Touchscreen 

For use on-screen for election coverage of Canadian elections

### Best displayed on a 1920 x 1080 screen.

To view in browser at this resolution: 
1. Navigate to the touchscreen page and press F12
2. Click the "Toggle device Emulation" button. (Ctrl + Shift + M)
3. Change the dimensions to 1920 x 1080


## Data folder structure

Elections are organized in the data folder as follows: 

```bash
├── PROV (2 letter abbreviation)
│   ├── ElectionYear
│   │   ├── banner.png
│   │   ├── {PROV}_config.json
│   │   ├── {PROV}_results.json
│   │   ├── {PROV}_prevResults.json
│   │   ├── {PROV}_topo.json
│   └── headshots
│   │   ├── ...candidate headshots
```

## Pushing data to the widget

BLADE Runner is used to push data from the database to the widget. Ideally, setup and use on a system that is always running and has network connection to the databse and the internet.

#### Setup tab
Under Cloud, enter credentials for the CMS you are using. The directory field should point to the subdirectory the widget is placed in

#### Run tab
1. Enter BLADE URL. BLADE URL can be generated using the Election URL Generator in Chameleon or from the BLADE discovery tool in BLADE Runner. Select election event. Must be in JSON format
2. Check Cloud checkbox
3. Filename: /data/{prov}/{year}/{prov}_results.json
4. Filename:(only push once if the previous year's data is inaccurate) /data/{prov}/{year}/{prov}_prevResults.json

## Pushing candidate headshots

Candidate heashots are easily retrieved from chameleon using the Candidate Headshots URL Generator:
1. Select Election Event from the dropdown
2. Change file format to .jpg
3. once downloaded and unzipped, place headshots directly into the headshots folder (see data folder structure)


