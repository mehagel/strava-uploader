# strava-uploader

Uses the Strava v3 API (documented [here](http://strava.github.io/api/)) to upload GPX and CSV activities exported from RunKeeper.

## Usage:

- First, we need to register an application with the Strava API service. Go to the [Strava API Management Page](https://www.strava.com/settings/api), and create a new application. Note the Client ID and Client Secret - you will need them later.
- Next, you need to get your data from Runkeeper. Go to the Settings page, and look for "Export Data" near the bottom. Define your time range, wait a minute or two, and then click download. Unzip the file - the directory should have .gpx files for all of your GPS-tracked runs, and two spreadsheets - "measurements.csv" and "cardio_activities.csv". 
- Open a Terminal window and `cd` to the data directory (should be something like "runkeeper-data-export-1234567")
- Install the requirements - `pip install -r requirements.txt`
- Next, we need to get an Authorization Token from Runkeeper for your Athlete account. Run 


## Misc other notes:
- Do NOT modify or even save (without modification) the CSV from Excel. Even if you just open it and save it with no modification, Excel changes the date formatting which will break this script. If you do need to modify the CSV for some reason (e.g., mine had a run with a missing distance, not clear why), do it in Sublime or another text editor.