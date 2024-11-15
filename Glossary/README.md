# API Proxies
- 👀 := Foundation of building out your API 👀
     - == interfaces for your backend services / abstract them
         - abstract == if you make changes in the backend services → APIs are still invoked
- == way to expose APIs on Apigee
- ⚠️ give the full power of Apigee’s API platform ⚠️
     - secure API calls
     - throttle traffic
         - rate limit & quotas
     - mediate messages
     - control error handling
     - cache things
     - build developer portals
     - document APIs
     - analyze API traffic data
     - earn money — with the use of your APIs —
     - protect agains bots
     - [modernize SOAP services](https://www.googlecloudcommunity.com/gc/Apigee/Apigee-X-Support-for-SOAP-Webservices/m-p/419451#M70359)
- types of endpoints
     - proxyEndpoint
         - == way / client apps — consume — APIs
             - API proxy URL
             **Note:** → HTTP or HTTPS
             - policies
                 - security
                 - quota checks
                 - rate limits
     - targetEndpoint
         - == way API proxy — interacts with — backend service
             - security settings
             - policies
                 - check response’s message format

    ![API Proxy](apiProxy.png)

- types of proxies
    - standard
        - := proxy / includes ONLY Standard policies
        - uses
            - lightweight API solutions
            - NOT included in API products
    - extensible
        - := proxies / includes ≥ 1 Extensible policies or flow hook
            - → can include more functionality

# API products
- := central mechanism / — limit the accesss control to — APIs
- == product line
  - == ≥ 1 API proxies grouped
    - Reason: 🧠operation 🧠
- allows
  - ≥ 1 operations are bundled
  - APIs are made available
- API product1 ← can share an API proxy with → API product2
- How does it work?
  - create ≥ 1 API Proxy
  - create API Product
  - deploy API Proxy & API Product
  - register client app + API product
  - use the API key / included in the API product — to authenticate 

    ![how does it work?](apiProductHowWorks.png)

# Operation
- == API proxy + resource paths  + access limits
  - 👁️resource paths / accessed on API proxy👁️
  - access limits by — HTTP methods OR quota
- := [group of attributes](https://cloud.google.com/apigee/docs/api-platform/publish/what-api-product#operations) / — restrict access to — ≥ 1 API proxy — based on —
  - resource path
  - HTTP method
  - quota

# API keys
- provisioned for API products (≠ API themselves)
- characteristics
  - it can be revoked at anytime
  - time limit to refresh

- TODO: