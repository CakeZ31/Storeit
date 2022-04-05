# Storeit

## Favorite Existing Apps -List
1. StockX
1. BUMP
1. GOAT
1. Kixify
1. NTWRK
1. Copdate
1. Nike SNKRS
1. Craigslist

## Favorite Existing Apps - Categorize and Evaluate
### GOAT
   - **Category:** Inventory/Selling Shoes and Appearal 
   - **Mobile:** Website has inventory walkthrough, uses most sought out shoes as opening page, mobile first experience.
   - **Story:** Allows users to explore the market and virtually see the shoe before purchase. 
   - **Market:** Anyone that is looking to either purchase or sell shoes can utilize the app. Ability become a seller after undergoing an authentication process.
   - **Habit:** There is daily updates and new drop notification where any seller and buyer can monitor the prices of the shoes
   - **Scope:** GOAT started off as a smaller app for inventory 

## Product Spec
### 1. User Stories

**Required Must-have Stories**

* User logs in with their employee ID to go to the next screen
* User has a waiting list of customers where they can add and delete customers as they leave. 
* User will be able to see the inventory of shoes with the sizes and prices. 
* Simple Profile page for each user

**Optional Nice-to-have Stories**

* Search engine through the inventory to make the process faster.
* A page of the description of the shoes with a bigger picture for the customer to view.
* Call function for customers on the waiting list
* Shoe filter to find the shoes a lot faster

### 2. Screen Archetypes

* Login 
* Waiting List - User signs in with their employee ID and is send to this waiting list
   * Upon logging in the employee will be prompted with the waiting list where they can view, add and delete customers off the waiting list 
* Shoe Inventory View - Shows the shoes that are currently in their inventory
   * When selecting a customer, the employee will be able to see the shoes that will be displayed with the shoe size and price. 
* Profile Screen 
   * Shows the picture of the employee and who they are currently helping

### 3. Navigation

**Tab Navigation** (Tab to Screen)

* Log in
* Customer waitlist
* Inventory
* Profile account

Optional:
* Shoe Description with larger photo and description

**Flow Navigation** (Screen to Screen)
* Log-in -> Customer Waiting list
* Customer Selected -> Shoe viewing list
* Drop down menu -> Profile account 


## New App Ideas - List
1. User friendly UI
   - Mean't to help out stores keep a better and more appealing inventory

2. Employee profile/account
   - Creating an employee based app so that they can manage inventory and keep a monitored list

3. Waiting list
   - Implementing a waiting list where employee can add and delete new customers. 

## Top 3 New App Ideas
1. User Friendly UI
2. Waitlist
3. Employee Account

## New App Ideas - Evaluate and Categorize
1. Employee Profile/Account
   - **Description**: Allows employees to monitor and manage their shoe store inventory by having a more fluid experience for both the customer and employee. 
   - **Category:** Store Seller/ Inventory
   - **Mobile:** Mobile is essential because they will be able to navigate through the inventory on their work phones and attend the customer faster. 
   - **Story:** Generates a faster shoe search and purchase for the customer while allowing for the employee to develop a more smooth experience with the customer.
   - **Market:** Any shoe store, individual sellers and looking forward also any inventory store not jsut shoe stores.
   - **Habit:** Employees will use this regularly to help out their customers find and buy the shoes they desire. 
   - **Scope:** It would allow employees to access an inventory of shoes that their store has and identify a faster shoe search. Could be put to test with an actual store and real customers.

## Wireframe images
![](https://i.imgur.com/rkrNAPW.jpg)
![](https://i.imgur.com/RNJFog6.jpg)



## Digital Wireframe/Mockup Images

![](https://i.imgur.com/uTvyGMF.png)

## Schema 
### Models
#### Post

   | Property      | Type     | Description |
   | ------------- | -------- | ------------|
   | itemId        | Number   | id for item listed |
   | itemName      | String   | name of product |
   | image         | File     | image of product |
   | description   | String   | descruption of product |
   | stockRemaining| Number   | amount of product still in stock |
   | employeeID    | Pointer  | ID that points to an employee user |
   | customerName  | String   | name of customer that is next in line |
   | phoneNumber   | String   | phone number of customer |
### Networking
#### List of network requests by screen
   - Log In Screen
      - (Read/GET) If cridentials match an existing employee ID
   - Product Listing Screen
      - (Read/GET) Create a new post object
      - (Update/PUT) Change quantity of items still available
   - Waitlist Screen
      - (Read/GET) get current list of customers waiting
      - (Delete) removes customer when serviced
