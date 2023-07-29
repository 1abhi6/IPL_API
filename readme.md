# IPL Dataset API Documentation
The IPL Match Analysis API project offers comprehensive analysis of all Indian Premier League (IPL) matches from the first season in 2008 to the 2022 season. The API is designed with a user-friendly authentication system, ensuring secure access to registered users. Upon successful registration and login, users gain access to the API's extensive functionality.

With this API, users can retrieve detailed insights, statistics, and data related to IPL matches, teams, players, and performances. The analysis covers various aspects of the matches, including batting, bowling, fielding, and overall team performance. Users can access real-time updates, historical data, and trends to gain a deeper understanding of IPL matches.

The project's authentication system guarantees that only authorized users can access the API, ensuring data privacy and security. By offering an intuitive and robust platform for IPL match analysis, this project empowers users to make informed decisions, conduct research, and explore the rich history of the IPL.


This is a Flask API that provides various endpoints to access the IPL dataset. The API uses the `Flask` and `jsonify` modules for response handling and `request` module for HTTP request handling. The API provides the following endpoints:

## Endpoints

### 1. Route or teams that have played IPL so far

This endpoint returns a list of teams that have played in the IPL so far.

**Route:** `/api/teams-played-ipl`

**Method:** `GET`

**Response:** A list of teams that have played in the IPL so far.

### 2. Route for track record of each team against each other

This endpoint takes two team names as parameters and returns their track record against each other.

**Route:** `/api/team1-vs-team2`

**Method:** `GET`

**Parameters:** `team1` (string), `team2` (string)

**Response:** A dictionary containing the track record of each team against each other.

### 3. Returns record of a team against all teams

This endpoint takes a team name as parameter and returns its record against all the teams that it has played against.

**Route:** `/api/record-against-all-teams`

**Method:** `GET`

**Parameters:** `team` (string)

**Response:** A dictionary containing the record of the team against all the teams that it has played against.

### 4. Returns record of a team against each team

This endpoint takes a team name as parameter and returns its record against each team that it has played against.

**Route:** `/api/record-against-each-team`

**Method:** `GET`

**Parameters:** `team` (string)

**Response:** A dictionary containing the record of the team against each team that it has played against.

### 5. Returns complete batsman record

This endpoint takes a batsman name as parameter and returns the complete batting record of the batsman.

**Route:** `/api/batsman-record`

**Method:** `GET`

**Parameters:** `batsman` (string)

**Response:** A dictionary containing the complete batting record of the batsman.

### 6. Returns complete bowling record

This endpoint takes a bowler name as parameter and returns the complete bowling record of the bowler.

**Route:** `/api/bowling-record`

**Method:** `GET`

**Parameters:** `bowler` (string)

**Response:** A dictionary containing the complete bowling record of the bowler.

## Usage

To use any of the above endpoints, make a GET request to the desired route with any required parameters. The API will return a JSON response containing the required data.To use the above API, the following endpoints can be used:

- `GET /api/teams-played-ipl`: Returns a list of all the teams that have played in the IPL so far.
Example usage: `http://localhost:5000/api/teams-played-ipl`

- `GET /api/team1-vs-team2?team1=<team1>&team2=<team2>`: Returns the track record of team1 against team2 in IPL matches. Replace `<team1>` and `<team2>` with the names of the teams for which you want to retrieve the record.
Example usage: `http://localhost:5000/api/team1-vs-team2?team1=Mumbai%20Indians&team2=Chennai%20Super%20Kings`

- `GET /api/record-against-all-teams?team=<team>`: Returns the track record of a team against all other teams in the IPL. Replace `<team>` with the name of the team for which you want to retrieve the record.
Example usage: `http://localhost:5000/api/record-against-all-teams?team=Chennai%20Super%20Kings`

- `GET /api/record-against-each-team?team=<team>`: Returns the track record of a team against each team in the IPL. Replace `<team>` with the name of the team for which you want to retrieve the record.
Example usage: `http://localhost:5000/api/record-against-each-team?team=Chennai%20Super%20Kings`

- `GET /api/batsman-record?batsman=<batsman>`: Returns the complete batting record of a batsman in IPL. Replace `<batsman>` with the name of the batsman for which you want to retrieve the record.
Example usage: `http://localhost:5000/api/batsman-record?batsman=VK%20Kohli`

- `GET /api/bowling-record?bowler=<bowler>`: Returns the complete bowling record of a bowler in IPL. Replace `<bowler>` with the name of the bowler for which you want to retrieve the record.
Example usage: `http://localhost:5000/api/bowling-record?bowler=JJ%20Bumrah`

Note: The examples above use `http://localhost:5000` as the base URL assuming the Flask application is running on the same machine.
Run flask using 
`flask run app.py`
