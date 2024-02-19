## **Flask Application Design:**

**Goal**: Create a Flask web app for F1 race fans to track statistics of their favorite drivers and teams.

## **HTML Files:**

- **index.html**: Main page that displays the list of drivers and teams, includes navigation to individual driver/team pages:
   - `<ul>` List of driver/team names
   - Links to driver/team pages
- **driver.html**: Individual page for each driver:
   - Driver details (name, team, nationality, etc.)
   - Table of race statistics (wins, podiums, etc.)
   - Form to add new race results
- **team.html**: Individual page for each team:
   - Team details (name, constructor, history, etc.)
   - Table of driver statistics (driver standings, wins, etc.)
   - Form to add new driver to team

## **Routes:**

- **@app.route('/')**: Home page displaying the list of drivers and teams
- **@app.route('/driver/<driver_id>')**: Individual driver page
- **@app.route('/team/<team_id>')**: Individual team page
- **@app.route('/add_race', methods=['POST'])**: Add race results for a driver
- **@app.route('/add_driver', methods=['POST'])**: Add a new driver to a team
- **@app.route('/delete_driver/<driver_id>/<team_id>', methods=['POST'])**: Remove a driver from a team