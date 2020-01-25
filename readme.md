# Deploy in Heroku with Nodejs

Create your app with `npm init`.

Put `express.js`.

    "dependencies": {
        "express": "^4.17.1"
    }

In file `app.js` change to `const port = process.env.PORT || 3000;`.

    const express = require('express')
    const app = express()
    const port = process.env.PORT || 3000;

    app.get('/', (req, res) => res.send('Hello World!'))

    app.listen(port, () => console.log(`Example app listening on port ${port}!`))

Add file `Procfile`.

    web: node app.js

Create a heroku app.

    heroku create unique-project-nam

Link de git

    heroku git:remote -a <repo name>

Deploy

    git push heroku master

Open

    heroku open 
