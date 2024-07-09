# top_nodejs_express-locallibrary-tutorial
This is an app developed by following allong the NodeJS Course on The Odin Project: [Introduction to Express | The Odin Project](https://www.theodinproject.com/lessons/nodejs-introduction-to-express).

TOP provides some additional commentary, but essentially it points you to the Mozilla Developer Network (MDN) web docs express tutorial. This is a 7 part series that takes you through how to use the Express Web framework.

See [Express web framework (Node.js/JavaScript) - Learn web development | MDN](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs)

The code follows the guide to the T until I get to [Express Tutorial Part 7: Deploying to production - Learn web development | MDN](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/deployment) where we try to deploy to production. Opted to try deploy to Azure instead of the options suggested in the article.

This guide was used to to make it happen [Deploy a Node.js web app using MongoDB to Azure - Azure App Service | Microsoft Learn](https://learn.microsoft.com/en-us/azure/app-service/tutorial-nodejs-mongodb-app).

## Current issues:
2024-07-08
- [x] Unable to view created documents in Cosmos DB. Maybe I just need to give it some time to show up.
  - Adding IP to whitelist didn't fix this. But I think this is related to permissions.
  - Need to enable access from Azure portal in Settings > Networking. [Configure an IP firewall for your Azure Cosmos DB account | Microsoft Learn](https://learn.microsoft.com/en-us/azure/cosmos-db/how-to-configure-firewall?WT.mc_id=Portal-Microsoft_Azure_DocumentDB)
- [x] Unable to set up Indexes in Cosmos DB - related to the above. Can't view the collections so cannot create the Index, without the index, existing sort() queries in controllers cannot work. Tested this by removing the sort in the author controller and it worked.
  - Was able to update the Index, by adding IP to whitelist. But still couldn't see the dat.
