![CF](http://i.imgur.com/7v5ASc8.png) LAB
=================================================

## Database Dashboard

### Author: Becca Lee

### Links and Resources
* [front-end site](https://xv2xk51myp.codesandbox.io/)
* [front-end repo](https://codesandbox.io/s/xv2xk51myp)
* [Q-Server](https://db-q-server.herokuapp.com/) (_Note: when opening this link, your browser may say "page not found"_)
* [Q-Server Repo](https://github.com/beccalee123/q-server)
* [API-Server](https://db-api-bl.herokuapp.com/)
* [API-Server Repo](https://github.com/beccalee123/API-Server-DB)

### Front-End Modules
- `index.js` renders the main app
- `lib/subsrcriber.js` connects to the Q server to receive incoming data
- `app.js` renders the dashboard and handles the rendering of incoming data
- `reset.scss` is a scss reset file
- `styles.scss` contains the app styling

### Setup
#### Front-End `.env` requirements
* `REACT_Q_SERVER` - should be set to the Q Server URL, [https://db-q-server.herokuapp.com](https://db-q-server.herokuapp.com), and must be entered without the trailing slash

#### Running the app
- Visit the front-end link above, which will update dynamically as records are added, updated, or deleted from the API-Server database
- If you'd like to work with the records to test output, open a terminal window and be sure you have [httPIE](https://httpie.org/) installed
- To add a record to the teams route, enter the following command `echo '{"name":"<Your name choice>"}' | http POST https://db-api-bl.herokuapp.com/api/v1/teams`
- To update a record on the teams route, enter the following command `echo '{"name":"<Your updated name choice>"}' | http PUT https://db-api-bl.herokuapp.com/api/v1/teams/<_id of the record you're updating>`
- To delete a record on the teams route, enter the following command `http DELETE https://db-api-bl.herokuapp.com/api/v1/teams/<_id of the record you're deleting>`
- - To add a record to the players route, enter the following command `echo '{"name":"<Your name choice>","position":"<Your choice of 'P','C','1B','2B','3B','SS','LF','RF','CF']>","throws":"<Your choice of 'R','L'>","bats":"<Your choice of 'R','L'>","team":"Your choice of team name"}' | http POST https://db-api-bl.herokuapp.com/api/v1/players`
- To update a record on the players route, enter the following command `echo '{"name":"<Your updated name choice>","position":"<Your upidated choice of 'P','C','1B','2B','3B','SS','LF','RF','CF']>","throws":"<Your updated choice of 'R','L'>","bats":"<Your updated choice of 'R','L'>","team":"Your updated choice of team name"}' | http PUT https://db-api-bl.herokuapp.com/api/v1/players/<_id of the record you're updating>`
- To delete a record on the players route, enter the following command `http DELETE https://db-api-bl.herokuapp.com/api/v1/players/<_id of the record you're deleting>`

#### Tests
* How do you run tests?
* What assertions were made?
* What assertions need to be / should be made?

#### Packages:
- Typing animations courtesy of (`react-typing-animation`)[https://www.npmjs.com/package/react-typing-animation] 
