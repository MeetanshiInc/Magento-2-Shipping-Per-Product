# Magento 2 Shipping Per Product

The **Magento 2 Shipping Per Product** extension allows store owners to set unique shipping rates for individual products, ensuring accurate and tailored shipping costs for customers. This feature is especially beneficial for stores that carry a diverse range of items with varying sizes, weights or handling requirements.

## **How It Works**

The **Magento 2 Shipping Per Product extension** provides a seamless way for store admins to assign specific shipping costs at the product level, ensuring each item has an appropriate shipping charge. By doing so, customers only pay the exact amount needed for shipping based on the product they choose.

## **Key Features**

* Set unique shipping rates per product in your Magento 2 store by activating the extension.  
* Customize the title displayed to customers for the shipping method.  
* Name the shipping method to suit your branding and display it to customers on the frontend.  
* Enable and define a default shipping rate for products.  
* The default rate applies automatically to products without individual shipping rates.  
* Add a custom handling fee to orders as needed.  
* Restrict the shipping per product feature to specific countries.  
* Create a custom message for when the shipping method is unavailable, shown to customers on the frontend.  
* Limit shipping per product access to admin users only.  
* Specify minimum and maximum order amounts to activate shipping per product functionality.

## **Product-Level Shipping Rate Setup**

With the Magento 2 Shipping Per Product extension, admins can set customized shipping rates per product, allowing for enhanced control and accuracy.

* Assign unique shipping costs to each product.  
* Ideal for products with distinct shipping requirements, such as heavy, oversized, or fragile items.

### **Customizable Country-Specific Rates**

* Set specific rates based on the destination country or region.  
* Ensure customers pay an accurate rate based on their location.

## **Flexible Shipping Rate Calculation**

The extension provides versatile rate calculation options, allowing store owners to tailor shipping fees to their business needs.

### **Fixed and Percentage-Based Rates**

* Choose between a flat rate or a percentage of the product price for shipping.  
* Offers flexibility for various shipping models and item types.

### **Override Shipping Rates for Promotions**

* Enable or disable custom shipping rates during specific promotions.  
* Provides flexibility for special offers or free shipping events.

## **Extension Installation**

To install the Magento 2 Shipping Per Product Extension to store follow the following steps:

### **Step 1:** 

Extract the zip folder and upload our extension to the root of your Magento 2 directory via FTP.

### **Step 2:**

Login to your SSH and run below commands step by step:

* php bin/magento setup:upgrade  
* For Magento version 2.0.x to 2.1.x \- php bin/magento setup:static-content:deploy  
* For Magento version 2.2.x & above \- php bin/magento setup:static-content:deploy –f  
* php bin/magento cache:flush

## **How to Configure Magento 2 Shipping Per Product Extension**

To configure the Magento 2 Shipping Per Product extension, log into the Magento admin panel and Go to **Sales \> Shipping Methods \> Shipping Per Product**. Here, you’ll find various settings to customize the extension to your store’s needs.

### **Step 1: Enable the extension & configure**

![1_Configuration-M2-Shipping-Per-Product](https://github.com/user-attachments/assets/8608d5d2-db53-4c19-a173-08836d2417e1)

* **Enabled:** Select “Yes” to activate the Shipping Per Product extension.  
* **Title:** Enter the title to display for this shipping method.  
* **Shipping Rate:** Choose how the shipping rate should be calculated.  
  * **Per Item:** Calculates the rate for each item individually.  
  * **Per Order:** Applies a single rate for the entire order.  
* **Shipping Rate Calculation:** Select a method for calculating the shipping rate.  
  * **Sum of Rate:** Adds the individual shipping rate for each item or order.  
  * **Maximum Value:** Applies the highest calculated rate for each item or order.  
  * **Minimum Value:** Applies the lowest calculated rate for each item or order.  
* **Method Name:** Enter the name for this shipping method.  
* **Default Product Shipping Cost:** Set to “Yes” to apply a default shipping rate when an individual rate is not assigned to a product.  
* **Default Rate per Item:** Specify a default rate per product when no other rate is set.  
* **Handling Fee:** Optionally, enter a handling fee to apply to orders.  
* **Ship to Applicable Countries:** Choose "All Allowed Countries" to enable Shipping Per Product for all countries.  
* **Ship to Specific Countries:** Select specific countries to enable this shipping method.  
* **Displayed Error Message:** Enter an error message to display if the shipping method is unavailable.  
* **Show Method Only for Admin:** Select “Yes” to restrict Shipping Per Product to admin use only.  
* **Minimum Order Amount:** Specify the minimum order amount required to enable this shipping method.  
* **Maximum Order Amount:** Define the maximum order amount allowed for using this shipping method.  
* **Sort Order:** Set the display order for this shipping method among others

### Step 2: Add Shipping Rates for Individual Products

![2_Set-Shipping-Rate-for-Product](https://github.com/user-attachments/assets/15ef8cfd-5525-4844-a137-27d0ea6b1be0)

To assign a unique shipping rate to a specific product, navigate to Catalog \> Products in the Magento admin panel. Select the product you wish to configure, then click Edit. Locate the Shipping Rate option and enter the desired rate to customize shipping costs for that individual product. This feature allows for precise shipping cost control based on each product’s specific requirements.

### Step 3: Check Shipping Per Product on the Frontend

Once individual shipping rates and the default rate are configured, the Shipping Per Product extension is activated on the frontend. When customers add products to their cart, the extension calculates and applies the shipping rate per product, as detailed in the table below. This ensures transparent and accurate shipping charges during checkout.

| Shipping Rate per Product 1 | Shipping Rate per Product 2 | Quantity for product 1 added to cart | Quantity for product 2 added to cart | Shipping Method | Calculation Type | Handling Fee | Total Shipping Rate |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| 10 | 20 | 2 | 2 | Per Order | Sum of Rate | 5 | 35 |
| 10 | 20 | 2 | 2 | Per Item | Sum of Rate | 5 | 65 |
| 10 | 20 | 2 | 2 | Per Order | Maximum Value | 5 | 25 |
| 10 | 20 | 2 | 2 | Per Item | Maximum Value | 5 | 45 |
| 10 | 20 | 2 | 2 | Per Order | Minimum Value | 5 | 15 |
| 10 | 20 | 2 | 2 | Per Item | Minimum Value | 5 | 25 |

* ### **Shipping Per Product on Cart Page – Per Order – Sum of Rates**
  
![2_Shipping-Per-Product-Charged-per-Order-Sum-of-Rates-on-Cart-Page](https://github.com/user-attachments/assets/b6e498ac-0282-409c-b50e-f86409c44d06)

When the shipping method is configured as Per Order with the calculation method set to Sum of Rates, the shipping cost is calculated by summing the individual rates for each product in the cart. For instance, if two quantities of two different products, each with its own shipping rate, are added to the cart, the total shipping charge will be calculated accordingly, as shown below.

* ### **Shipping Per Product on Checkout Page**

![4_Shipping-Per-Product-Charged-per-Item-Sum-of-Rates-on-Checkout-Page](https://github.com/user-attachments/assets/d4d4836d-c03f-485b-8e15-4179b8e83e6f)

The **Shipping Per Product** method is applied to the order on the checkout page, ensuring accurate shipping charges based on individual product rates.

* ### **Shipping Per Product in the “My Account” Section**

![5_Shipping-Per-Product-in-My-Account-Page](https://github.com/user-attachments/assets/490db762-54f0-497d-84e8-36b1eda843c5)

After an order is placed using the **Shipping Per Product** method, customers can view the shipping details, including the shipping method name, in the **My Orders** tab within the **My Account** section.

* ### Shipping Per Product Details in the Backend

In addition to the frontend, details for the Shipping Per Product method are also accessible from the backend. Navigate to Sales \> Orders to view each order, where the shipping per product information is displayed within the Order View, as shown in the image below.

### Step 4: Update Product-Specific Shipping Details in Admin Console

![6_Shipping-Per-Product-in-Order-View-Backend](https://github.com/user-attachments/assets/f8536caf-c2bd-40d0-afbd-0c1f728f3dbe)

In addition to the frontend, details for the **Shipping Per Product** method are also accessible from the backend. sNavigate to **Sales \> Orders** to view each order, where the shipping per product information is displayed within the Order View, as shown in the image below.

## Download our [Magento 2 Shipping Per Product](https://meetanshi.com/magento-2-shipping-per-product.html) Extension


