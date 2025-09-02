# Firestore Import Export
A script that help to export and import in Cloud Firestore

** This repo is not maintained. Please try the [backup and restore from Firestore](https://github.com/dalenguyen/firestore-backup-restore) package instead!

# Requirements

You need [NODE](https://nodejs.org/en/download/) or something that can run JAVASCRIPT (JS) file.

Get **serviceAccount** JSON file from *Project Setting > SERVICE ACCOUNTS* in Firebase Console

Change the *databaseURL* when initializeApp with your own

# Setting Up

Download or clone this repository

```
git clone https://github.com/dalenguyen/firestore-import-export.git
```

Install NPM packages

```
npm install
```

# Export database from Firestore

This will help you create a backup of your collection and subcollection from Firestore to a JSON file name **firestore-export.json**

```
node export.js <your-collection-name> <sub-collection-name-(optional)>
```

# Import database to Firestore

This will import a collection to Firestore will overwrite any documents in that collection with matching id's to those in your json. If you have date type in your JSON, please add the field to the command line. **The date and geo arguments is optional**. 

```
node import.js import-to-firestore.json date=date geo=Location
```

If you have date type in your JSON, please add to your command line 

Sample from __import-to-firestore.json__. "test" will be the collection name. The date type will have _seconds and _nanoseconds in it.

```
{
  "test" : {
    "first-key" : {
      "email"   : "dungnq@itbox4vn.com",
      "website" : "dalenguyen.me",
      "custom"  : {
        "firstName" : "Dale",
        "lastName"  : "Nguyen"
      },
      "date": {
        "_seconds":1534046400,
        "_nanoseconds":0
      },
      "Location": {
        "_latitude": 49.290683,
        "_longitude": -123.133956
      }
    },
    "second-key" : {
      "email"   : "test@dalenguyen.me",
      "website" : "google.com",
      "custom"  : {
        "firstName" : "Harry",
        "lastName"  : "Potter"
      },
      "date": {
        "_seconds":1534262435,
        "_nanoseconds":0
      },
      "Location": {
        "_latitude": 49.290683,
        "_longitude": -123.133956
      }
    }
  }
}
```

# Change serviceAccountKey.json 

	(You can get from firbase account Project settings ->Service account -> Select Node.js -> Generate new private key see:https://prnt.sc/5YcwVJHM5Pcb )

# IMPORT Commands:

node import.js FoodieDataSeed/booked_table.json

node import.js FoodieDataSeed/cms_pages.json

node import.js FoodieDataSeed/coupons.json

node import.js FoodieDataSeed/currencies.json

node import.js FoodieDataSeed/driver_payouts.json

node import.js FoodieDataSeed/favorite_item.json

node import.js FoodieDataSeed/favorite_restaurant.json

node import.js FoodieDataSeed/foods_review.json

node import.js FoodieDataSeed/menu_items.json

node import.js FoodieDataSeed/notifications.json

node import.js FoodieDataSeed/order_transactions.json

node import.js FoodieDataSeed/payouts.json

node import.js FoodieDataSeed/rating.json

node import.js FoodieDataSeed/referral.json

node import.js FoodieDataSeed/reports.json

node import.js FoodieDataSeed/restaurant_orders.json

node import.js FoodieDataSeed/review_attributes.json

node import.js FoodieDataSeed/settings.json

node import.js FoodieDataSeed/story.json

node import.js FoodieDataSeed/subscription_list.json

node import.js FoodieDataSeed/users.json

node import.js FoodieDataSeed/vendor_attributes.json

node import.js FoodieDataSeed/vendor_categories.json

node import.js FoodieDataSeed/vendor_filters.json

node import.js FoodieDataSeed/vendor_products.json

node import.js FoodieDataSeed/vendors.json

node import.js FoodieDataSeed/wallet.json

# Not Mandatory

node import.js FoodieDataSeed/channel_participation.json

node import.js FoodieDataSeed/channels.json


# Export commands:

node export.js booked_table

node export.js chat_driver

node export.js chat_restaurant

node export.js cms_pages

node export.js coupons

node export.js currencies

node export.js driver_payouts

node export.js favorite_item

node export.js favorite_restaurant

node export.js foods_review

node export.js menu_items

node export.js notifications

node export.js order_transactions

node export.js payouts

node export.js rating

node export.js referral

node export.js reports

node export.js restaurant_orders

node export.js review_attributes

node export.js settings

node export.js story

node export.js subscription_list

node export.js users

node export.js vendor_attributes

node export.js vendor_categories

node export.js vendor_filters

node export.js vendor_products

node export.js vendors

node export.js wallet

# Not Mandatory 

node export.js channel_participation

node export.js channels


<!-- Security scan triggered at 2025-09-02 04:50:46 -->