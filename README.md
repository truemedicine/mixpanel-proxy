# Nginx Proxy for Mixpanel
This is an nginx config that serves as a proxy to Mixpanel's Ingestion API and JavaScript library endpoints. [Docs on Tracking via Proxy](https://docs.mixpanel.com/docs/tracking/how-tos/tracking-via-proxy). The purpose of the proxy is to get around adblockers blocking event tracking. Truemed sends events to a Truemed-owned domain, and the proxy routes them to Mixpanel.

# Deploying
In Heroku, there is an app called `mixpanel-proxy` that hosts this Docker container, which is purely a proxy. For speed of development, this is only deployed from local machines as opposed to via the repository.
To deploy:
- Clone this repo
- Make and commit changes
- `heroku git:remote -a mixpanel-proxy` - to create the heroku remote
- `git remote rename heroku mixpanel-proxy-heroku` - to rename the remote
- `git push mixpanel-proxy-heroku HEAD:master --force` - to deploy

TODO:
- Hook the Heroku up to GitHub to avoid manual deploys