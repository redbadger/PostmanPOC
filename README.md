# PostmanPOC
POC for storing a Postman collection and env variables in GitHub

## Importing the collection

In Postman, import as 'Link', pasting this value in `https://raw.githubusercontent.com/redbadger/PostmanPOC/main/collection.json`

## Importing the environment variables

In Postman, import as 'Link', pasting this value in `https://raw.githubusercontent.com/redbadger/PostmanPOC/main/env.json`

## Installing Newman

`npm install -g newman`

## Running the collection

From this repo, `newman run https://raw.githubusercontent.com/redbadger/PostmanPOC/main/collection.json -e https://raw.githubusercontent.com/redbadger/PostmanPOC/main/env.json`

If new environment variables need adding, run `newman run https://raw.githubusercontent.com/redbadger/PostmanPOC/main/collection.json -e https://raw.githubusercontent.com/redbadger/PostmanPOC/main/env.json --export-environment env.json`

The above command will run the collection using the stored environment variables. It will then output new environment variables at the end of the run, which would need to be commited to Git

## Next steps

From there, any changes made to the collection or env file would need to be commited to Git to replace the old versions. These changes would be subject to the same review process as any code changes
