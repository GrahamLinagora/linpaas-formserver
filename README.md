# LinPaaS Form Server

Node.js based form server used to store and retrieve JSON serialized HTML forms.

## Usage

First be sure you have MongoDB and Node.js installed...

    git clone https://github.com/linagora/linpaas-formserver.git
    npm install
    node app.js

Check config.js for configuration options.

## API

Base URI for forms is at http://localhost:3000/forms

### Get Forms

    HTTP GET /forms

Returns a JSON array of forms.

### Get a form

#### From ID

    HTTP GET /forms/:id

Returns a form as JSON.

#### From its name

    HTTP GET /forms?name=:name

Returns a JSON array if form with given name are found.

### Create a form

    HTTP POST /forms

With the JSON as body:

    {
      name : 'Form name',
      model : {

      }
    }

Returns HTTP status 201 if created.