# Spotify Playlists Ranking

## Overview
This is an app for calculating the Promotion Playlists Ranking based upon the tracks on their list makes to the targeted List "RapCaviar" playlist. Ranking is calculated numbers of tracks makes to the RapCaviar and the particular playlist followers.

Percentage for number of tracks makes to **RapCaviar** and their percentage of followers with respect to the highest number of tracks made to "RapCaviar" and highest percetage. Summing up their percentage and calculating with respect to the 100% , promotion playlist is ranked. For those playlist from whom the track is not yet made to "RapCaviar", their ranking is calculated based on the followers following after the ranking of playlist from whom the tracks made to the **RapCaviar**.

We have used Flask for the web view as we need to show the ranking on the page.

## Run it

Run the following commands to get the code from GitHub and run locally this will run the project locally I have created an spotify app and used the Oauth web workflow to get the token and call the API and then with the help of refresh token get the new token if the token is expired.

This app is development mod so the login users is limited if you want to test it and want to use your app Add the CLIENT ID and CLIENT SECRET in the ``spotify.py``

| NAME                                      | default             | required                      | type    | description                         |
|-------------------------------------------|---------------------|-------------------------------|---------|------------------------------------|
| CLIENT_ID                                 | "unspecified"       | :white_check_mark:            | str     | Spotify app client id              |
| CLIENT_SECRET                             | False               | :white_check_mark:            | str     | Spotify app client secret          |

And add the callback URL to your spotify app.


###Windows instructions
```
git clone https://github.com/yasirrose/spotify.git
cd spotify
python -m venv env
.\env\Scripts\activate
pip install -r requirements.txt
flask created_db
flask add_playlists
python app.py
```
###Unix(Linux & Linux) instructions
```
git clone https://github.com/yasirrose/spotify.git
cd spotify
python3 -m venv env
source env/bin/activate
pip install -r requirements.txt
flask created_db
flask add_playlists
python3 app.py
```

**Steps for Testing**

1. For adding tables to the database "flask created_db" , "flask add_playlists" to add playlist Ids to table for fecthing data.(I have included the full db with tables and data so you wouldn't need to run this comand)
2. python app.py to run the application.(This will launch the application on `http://127.0.0.18081/` you need to open this in browser)
3. CLick on the Login Tab to get access to the account.
4. For pulling playlist tracks data for calculation hit `http://127.0.0.1:8081/add_playlist_data` in the browser.
5. For Ranking Calculation hit `http://127.0.0.1:8081/promotion_ranking`  in the browser.
6. For viewing Ranking you can check `here: http://127.0.0.1:8081/ranking` in the browser.


**Video Demo**

[Click here to view the demo](https://www.loom.com/share/22331dcf27234d4e93d6c300e224596c)


**Note:** Feel free to contact me if you have any query.

