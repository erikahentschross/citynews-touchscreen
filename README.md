# CityNews Touchscreen 

For use on-screen for election coverage of Canadian elections

### Best displayed on a 1920 x 1080 screen.

To view in browser at this resolution: 
1. Navigate to the touchscreen page and press F12
2. Click the "Toggle device Emulation" button. (Ctrl + Shift + M)
3. Change the dimensions to 1920 x 1080


## Data folder structure

Elections are organized in the data folder as follows: 

-PROV (abbrev)
--election year
    --banner.png
    --{prov}_config.json
    --{prov}_results.json
    --{prov}_prevResults.json
    --{prov}_topo.json 
--headshots
    -- ...candidate headshots

## Pushing data to the widget

#### Setup tab
Under Cloud, enter credentials for the CMS you are using. The directory field should point to the subdirectory the widget is placed in

#### Run tab
1. Enter BLADE URL. BLADE URL can be generated using the Election URL Generator in Chameleon or from the BLADE discovery tool in BLADE Runner. Select election event. Must be in JSON format
2. Check Cloud checkbox
3. Filename: /data/{prov}/{year}/{prov}_results.json
4. Filename:(only push once if the previous year's data is inaccurate) /data/{prov}/{year}/{prov}_prevResults.json





