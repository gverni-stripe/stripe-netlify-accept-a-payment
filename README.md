[![Netlify Status](https://api.netlify.com/api/v1/badges/518f1cc7-75d9-486f-b4f3-393dae35305b/deploy-status)](https://app.netlify.com/sites/stripe-netlify-accept-a-payment/deploys)

# Stripe Accept a payment boilerplate for Netlify 

Demo available [here](https://stripe-netlify-accept-a-payment.netlify.app/)

This is a simple boilerplate for the [Stripe Accept A Payment](https://github.com/stripe-samples/accept-a-payment) Sample. 

To use this sample on Netlify from GitHub: 
* Clone the project into your GitHub profile
* Go on your Netlify console and click "Add a new site"
* Click "Deploy with GitHub"
* Select the repo you cloned
* Set the following Build settings:
  * Base Directory: leave empty
  * Build Command: leve empty
  * Publish directory: `client` (don't blame me for the name. I'm keeping it consistent with the sample app)
  * Functions directory: leave prefilled value (`netlify/functions`)
* Click on `Environment Variable` button and add the following environmental variable
  * `STRIPE_PUBLISHABLE_KEY`: your Stripe publishable key
  * `STRIPE_SECRET_KEY`: your stripe secret key
* Click Deploy button

# Testing locally 

If you want to run this repo locally, install the netlify CLI and then run the following commands: 
* Install dependencies 
```
npm install
```
* Run netlify CLI in dev mode 
```
netlify dev 
```

The output should be something like: 

```
◈ Netlify Dev ◈
◈ Injecting environment variable values for all scopes
◈ Ignored general context env var: LANG (defined in process)
◈ Injected site settings env var: STRIPE_PUBLISHABLE_KEY
◈ Injected site settings env var: STRIPE_SECRET_KEY
◈ Setting up local development server
◈ Starting Netlify Dev with custom config
Serving "./client/" at http://127.0.0.1:3000
Ready for changes
✔ Waiting for framework port 3000. This can be configured using the 'targetPort' property in the netlify.toml
◈ Loaded function config
◈ Loaded function create-payment-intent

   ┌──────────────────────────────────────────────────┐
   │                                                  │
   │   ◈ Server now ready on http://localhost:8888    │
   │                                                  │
   └──────────────────────────────────────────────────┘
```

This will spawn two servers:
* `live-server` on port 3000 
* Netlify server on port 8888 (or another one depending on your system)

Open the Netlify server in your browser to have both static and functions served on the same port 