## Custom paypal smart button integration on shopify Refresh Theme cart page instead of checkout page

### Step 1 - Go to the theme page click on edit code 

![image](https://github.com/Umer-Aziz/Shopify-paypal-payment/assets/62507205/3073b576-36fa-4ce9-a2e9-69432bfbc384)

### Step 2 - Create a paypal-smart-buttons.liquid file inside Snippets Folder
### Step - 3 Copy the Code from above paypal-smart-buttons.liquid file paste in Shopify file

![image](https://github.com/Umer-Aziz/Shopify-paypal-payment/assets/62507205/c2590524-b958-4348-b5db-086cad27493b)

### Step - 4 Replace your paypal app ID where cleint-id=test , replace test with your ID

<code><script src="https://www.paypal.com/sdk/js?client-id=test&currency=USD&components=buttons,hosted-fields&enable-funding=card&disable-funding=paylater,venmo" data-sdk-integration-source="integrationbuilder_sc"></script>
</code> 

### Step 5 - Create customer-form.liquid same as above in Snippet folder & copy paste the code

### Step - 6  Replace the api or getform.io id here to get customer detail


![image](https://github.com/Umer-Aziz/Shopify-paypal-payment/assets/62507205/ee16896e-5e53-4426-ad97-c96e507abcfb)

### Step - 7 Render the Form in Cart page by using this Line of code in main-cart-items.liquid file

<code>  {% render 'customer-form' %} </code>

![image](https://github.com/Umer-Aziz/Shopify-paypal-payment/assets/62507205/fbbbfcb0-d7cf-41a5-834b-47843ba3d541)

### Step - 8 Render the paypal-smart-buttons.liquid in Cart page by using this Line of code in main-cart-footer.liquid file

<code>  {% render 'paypal-smart-buttons' %} </code>

![image](https://github.com/Umer-Aziz/Shopify-paypal-payment/assets/62507205/641e4984-54a6-4af5-8280-fa1033f0e958)

## Here is how it looks on website cart page 

![image](https://github.com/Umer-Aziz/Shopify-paypal-payment/assets/62507205/ca0e3b2d-4e0b-4fb3-a152-59302b8b3278)

##### The paypal smart buttons are enabled when the Billing form of a customer is submitted
