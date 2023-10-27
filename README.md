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



