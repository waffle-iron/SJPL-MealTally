[![Stories in Ready](https://badge.waffle.io/codeforsanjose/SJPL-MealTally.png?label=ready&title=Ready)](https://waffle.io/codeforsanjose/SJPL-MealTally)
## Background

The San Jose Public Library runs a [summer program](https://www.sjpl.org/summerfood) where they provide three meals a day + snacks to children at seven of their branches. The meals come from the YMCA, and left over meals can be served to adults, but the library must pay the YMCA for any meals that don't go to a child.

Because of the above restriction, the library must keep diligent documentation of each meal, and the coordinator sends a weekly report for each library. For the past two summers, a volunteer was needed just for the task of filling out the paperwork at each library at every meal - keeping track of how many new meals were received, left over, how many went to kids, etc. Not only does this mean that the volunteer can't help with other tasks, but it is also creates over 8,000 pages of paperwork per month. Keeping up on the paperwork is a grueling task.

## State of the app and current tasks

Last October, some friends and I hacked together a software [solution](https://github.com/robeau/SJPL-MealTally) during a 30-hour [hackathon](https://devpost.com/software/togetherly-mealtally). We have since delivered the mobile and web app to the library, but since this was a quick hack, there are still some tasks that need to be taken care of before the meal program starts back up in May. I am currently the only developer still working with them on the web portion of the project, and my time is limited, plus this seems like a great project for CfSJ to be involved in as it benefits our public libraries. See open issues for a list of current tasks.

## Running the web app locally

1. Clone the project and cd into SJPL-MealTally/server.

2. You will need to either add a ../../config folder with a MongoLabs URI and an email URI OR create two new environment variables:
  * **MLABURI** = mongodb://\<dbUser\>:\<dbPassword\>@ds0\<port\>.mlab.com:\<port\>/mealtally
  * **MAILURI** = smtps://\<emailAddress\>:\<password\>@smtp.gmail.com/?pool=true (if you're using gmail, you will have to change some settings - you'll get an email about it the first time you try to run the app with your URI)
  * NOTE: If you go with the config file option, please make sure to add it to your .gitignore so that your sensitive information is not accidentally posted to github.

3. `npm install`

4. `node app`

The app should connect to the database and be running at localhost:3000

