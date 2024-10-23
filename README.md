# Nginx Proxy for Mixpanel
This is an nginx config that serves as a proxy to Mixpanel's Ingestion API and JavaScript library endpoints. [Docs on Tracking via Proxy](https://docs.mixpanel.com/docs/tracking/how-tos/tracking-via-proxy). The purpose of the proxy is to get around adblockers blocking event tracking. Truemed sends events to a Truemed-owned domain, and the proxy routes them to Mixpanel.

