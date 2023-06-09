## Zomato Merchant API (Unofficial) | 2022 - 2023

> **Disclaimer:** This project is not affiliated, associated, authorized, endorsed by, or in any way officially connected with Zomato or any of its subsidiaries or affiliates. The official Zomato website can be found at [https://zomato.com](https://zomato.com). "Zomato", "Zomato API", "Zomato *" as well as related names, marks, emblems, and images are registered trademarks of their respective owners.

### Features included:

- ✅ Multiple login
- ✅ Orders list
- ✅ Orders list filtering (By status)
- ✅ Accept new order
- ✅ Mark order ready
- ✅ Go online & Offline - status
- ✅ Item list (Menu)
- ✅ Item list editing (Menu editing)
- ✅ This isn't web scraping, so you will get the native speed of Zomato.


### Login

```
POST http://localhost:port/login
```

**Request Body:**
```json
{
    "phone": "123456789",
    "system_id": "demo_system"
}
```

**Example Response:**
```json
{
    "message": "cookies saved successfully.",
    "status": 1
}
```

### OTP

```
POST http://localhost:10000/OTP
```

Call this API after receiving the OTP. Make sure to call the `/login` API before calling this API.

**Request Body:**
```json
{
    "otp": "323232",
    "system_id": "demo_system"
}
```

**Example Response:**
```json
{
    "message": "OTP saved successfully.",
    "status": 1
}
```

### Logout

```
POST http://localhost:10000/users/logout
```

Logout and delete your data from the API.

**Request Body:**
```json
{
    "system_id": "demo_system"
}
```

**Example Response:**
```json
{
    "message": "logout successful.",
    "status": 1,
}
```

### Get Merchant Info

```
POST http://localhost:10000/info/restaurants
```

Get merchant information for the logged-in user.

**Request Body:**
```json
{
    "system_id": "demo_system"
}
```

**Example Response:**
```json
{
    {
    "message": "info saved successful.",
    "status": 1,
    "data": {
      "count": 1,
      "res_opening": {
        "notify_after_secs": 0,
        "should_notify": false,
        "tts_message": "You are now online on Zomato"
      },
      "entities": [
        {
          "id": 19885042,
          "name": "XXXXXXXX",
          "city_name": "Pune",
          "address": "XXXXX",
          "subzone": "XXXXX",
          "latitude": "18.4444",
          "longitude": "73.4444",
          "delivery_status": 0,
          "disable_delivery_toggle": true,
          "res_partner_status": 0,
          "default_delivery_time": 0,
          "show_runnr_banner": 0,
          "show_self_delivery_banner": 0,
          "self_delivery_serviceable": 0,
          "self_delivery_status": 0,
          "show_self_delivery_toggle": false,
          "is_take_away_serviceable": 0,
          "is_take_away_enabled": 0,
          "logistic_partner_serviceable": false,
          "logistics_partner_status": false,
          "country_id": 1,
          "country_phone_regex": "^[0-9]{10,10}$",
          "country_isd_code": "91",
          "dispatch_buffer": 10,
          "owner_details": {
            "name": "xxxx",
            "phone": "+xxxxxx",
            "email": "xxxx@xxxxx.com"
          },
          "o2_only": "xxxx",
          "o2_priority": "xxxxx",
          "thumbnail": "xxxx",
          "map_url": "xxxx",
          "active_since": "06 Sep 2021",
          "rating_info": {
            "aggregate_rating": "4.0",
            "rating_text": "Very Good",
            "rating_color": "5BA829",
            "rating_obj": {
              "title": {
                "text": "4.0"
              },
              "bg_color": {
                "type": "lime",
                "tint": "600"
              }
            },
            "votes": 775
          },
          "rating_split_info": {
            "is_newly_opened": false,
            "is_newly_opened_for_delivery": false,
            "is_suspicious": false,
            "suspicious_ratings_count": 0,
            "ratings": {
              "DINING": {
                "type": "DINING"
              },
              "DELIVERY": {
                "type": "DELIVERY",
                "rating": "4.0",
                "rating_count": "775",
                "is_newly_opened_for_delivery": false,
                "element_ratings": [
                  {
                    "tag_id": 184058,
                    "tag_identifier": "packaging",
                    "rating": 4.0487,
                    "vote_count": 24
                  },
                  {
                    "tag_id": 189359,
                    "tag_identifier": "portion size",
                    "rating": 3.8286,
                    "vote_count": 25
                  },
                  {
                    "tag_id": 183354,
                    "tag_identifier": "value for money",
                    "rating": 4.2756,
                    "vote_count": 25
                  },
                  {
                    "tag_id": -1,
                    "tag_identifier": "food taste",
                    "rating": 3.8462,
                    "vote_count": 37
                  }
                ],
                "is_experiment_active": false
              }
            }
          },
          "start_time": "",
          "end_time": "",
          "on_time": "2023-06-09 11:00:00",
          "res_off_reason": "Your outlet is outside the delivery timings",
          "city_id": 5,
          "merchant_ids": [
            385020
          ],
          "order_ready_warning_factor": 0.5,
          "manager_details": {
            "name": "",
            "email": "",
            "phone": ""
          },
          "isStore": false,
          "isAlcoBev": false,
          "alarm_data": null,
          "supported_service_types": [
            "delivery"
          ],
          "restaurant_tags": [
            "live_delivery",
            "delivery"
          ],
          "is_staff_management_enabled": false,
          "is_hyper_pure_enabled": true,
          "hyper_pure_disabled_reason": "",
          "is_pos_res": false,
          "is_add_new_gst_flow_enabled": true,
          "share_feedback_url": "xxxxx",
          "is_new_refund_policy_applicable": true,
          "show_onboarding_screens": false,
          "is_deployment_ready": true,
          "is_promo_diy_offers_enabled": true,
          "voice_instruction_edits_allowed": true,
          "show_mx_product_tour": false,
          "is_outlet_location_edit_enabled": true,
          "is_restaurant_instant_food_fulfillment_center": false,
          "is_menu_score_v2_enabled": false,
          "delivery_staff_registration_flow_enabled": false,
          "am_details": {
            "zomato_contact_poc": 273416941,
            "zomato_contact_poc_name": "xxxx",
            "poc_email": "xxx",
            "poc_phone": "xxxx",
            "tl_email": "xxxx",
            "tl_mobile": "xxx"
          },
          "profile_pic": {
            "url": "",
            "status": "ACCEPTED",
            "is_editable": false,
            "comments": ""
          },
          "cover_pic": {
            "url": "xxxx",
            "status": "ACCEPTED",
            "is_editable": true,
            "comments": ""
          },
          "cuisines": {
            "status": "ACCEPTED",
            "is_editable": true,
            "comments": "Validates all conditions",
            "text": "Kerala",
            "cuisine_ids": [
              "62"
            ]
          },
          "cx_info_feature_enabled": false,
          "fssai_number": "xxxxx",
          "fssai_doc_url": "https://www.zomato.com/php/get_file?p="
        }
      ]
    }
  }
}
```

### Check Login Status

```
POST http://localhost:10000/user/auth-check
```

Check the login status and get other login info.

**Request Body:**
```json
{
    "system_id": "demo_system"
}
```

**Example Response:**
```json
{
    "message": "auth check successful.",
    "status": 1,
}
```

### Get List of Orders

```
POST http://localhost:10000/orders
```

Get a list of current live orders based on their status

**Request Body:**
```json
{
    "system_id": "demo_system"
}
```

**Example Response:**
```json
{
    {
  "message": "orders successful.",
  "status": 1,
  "data": [
    {
      "count": 0,
      "entities": [],
      "state": "NEW"
    },
    {
      "count": 2,
      "entities": [
        4934273288,
        4938146191
      ],
      "state": "PREPARING"
    },
    {
      "count": 1,
      "entities": [
        4937534006
      ],
      "state": "READY"
    },
    {
      "count": 0,
      "entities": [],
      "state": "DISPATCHED"
    },
    {
      "count": 0,
      "entities": [],
      "state": "RETURNING"
    }
  ]
}
}
```

### Get Order Details

```
POST http://localhost:10000/order_details
```
Here take order id from orders list and pass it in the request body.

**Request Body:**
```json
{
    "system_id": "demo_system",
    "order_id": "4934273288"
}
```

**Example Response:**
```json
{
  "message": "order details successful.",
  "status": 1,
  "data": {
    "status": "success",
    "order": {
      "id": "4934273288",
      "resId": "19885042",
      "state": "PREPARING",
      "handoverDetails": {
        "time": 49,
        "maxTime": 54,
        "minTime": 44,
        "text": "Set food preparation time",
        "stepSize": 1,
        "isPreparationDelayAllowed": true
      },
      "creator": {
        "userId": "xxxx",
        "name": "xxx",
        "countryIsdCode": "91",
        "orderCount": 4,
        "orderCountDisplay": "4th order by xxxx",
        "address": {
          "id": "xxxxx",
          "address": "xxx (6 kms, 18 mins away)",
          "addressInstructions": "xxxx",
          "location": {
            "latitude": 18.5957603,
            "longitude": 73.8304443
          },
          "locality": "xxxx (6 kms, 18 mins away)"
        },
        "profilePictureUrl": "xxxx",
        "profileUrl": "xxxx",
        "customerSegmentation": "PREMIUM",
        "isRepeatCustomer": true,
        "originalName": "xxxxx"
      },
      "createdAt": "2023-06-09T14:27:33Z",
      "actionedAt": "2023-06-09T14:28:16Z",
      "paymentMethod": "PAID",
      "riderAssigned": true,
      "zomatoDelivered": true,
      "deliveryMode": "DELIVERY",
      "otp": "7980",
      "riderReachedOutlet": "2023-06-09T14:49:50Z",
      "acceptExpiryTime": 300,
      "pickupThresholdTime": 180,
      "paymentDetails": {
        "paymentType": "PAID",
        "paymentMethod": "PAID"
      },
      "orderMessages": [
        {
          "messageType": "ORDER",
          "messageTag": "order_top",
          "value": {
            "message": "Don’t send cutlery, tissues and straws",
            "type": "ALERT",
            "icon": "e9c2"
          }
        }
      ],
      "meta": {
        "actionExpiryTime": "2023-06-09T15:17:16Z",
        "actionExpiryDuration": 2940
      },
      "nextStates": [
        "READY"
      ],
      "updatedAt": "2023-06-09T14:46:29Z",
      "expectedHandOverTime": "2023-06-09T15:25:16Z",
      "cartDetails": {
        "items": {
          "dishes": [
            {
              "id": "1",
              "name": "Pappadam [Serves 2]",
              "referenceType": "DRT_VARIANT",
              "referenceId": "656249420",
              "quantity": 3,
              "unitCost": 10,
              "totalCost": 30,
              "subCategoryId": "49196795",
              "calculations": [
                {
                  "id": "2",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 30,
                  "entityType": "DCT_VOUCHER_DISCOUNT",
                  "entityId": "2137537187",
                  "value": 3,
                  "amount": 3,
                  "calcAppliedOnAmount": 30,
                  "appliedPercentageValue": 3,
                  "calcAmount": 3
                },
                {
                  "id": "3",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 30,
                  "name": "taxable_discount",
                  "entityType": "DCT_TOTAL_TAXABLE_DISCOUNT",
                  "value": 3,
                  "amount": 3,
                  "calcAppliedOnAmount": 30,
                  "appliedPercentageValue": 3,
                  "calcAmount": 3
                },
                {
                  "id": "4",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 27,
                  "name": "CGST",
                  "entityType": "DCT_TAX",
                  "entityId": "4",
                  "isPercentage": true,
                  "value": 2.5,
                  "amount": 0.675000012,
                  "calcAppliedOnAmount": 27,
                  "appliedPercentageValue": 2.5,
                  "calcAmount": 0.675
                },
                {
                  "id": "5",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 27,
                  "name": "SGST",
                  "entityType": "DCT_TAX",
                  "entityId": "3",
                  "isPercentage": true,
                  "value": 2.5,
                  "amount": 0.675000012,
                  "calcAppliedOnAmount": 27,
                  "appliedPercentageValue": 2.5,
                  "calcAmount": 0.675
                },
                {
                  "id": "6",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 27,
                  "name": "CGST",
                  "entityType": "DCT_SOURCE_TAX",
                  "entityId": "4",
                  "isPercentage": true,
                  "value": 2.5,
                  "amount": 0.675000012,
                  "calcAppliedOnAmount": 27,
                  "appliedPercentageValue": 2.5,
                  "calcAmount": 0.675
                },
                {
                  "id": "7",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 27,
                  "name": "SGST",
                  "entityType": "DCT_SOURCE_TAX",
                  "entityId": "3",
                  "isPercentage": true,
                  "value": 2.5,
                  "amount": 0.675000012,
                  "calcAppliedOnAmount": 27,
                  "appliedPercentageValue": 2.5,
                  "calcAmount": 0.675
                }
              ],
              "metadata": {
                "tags": [
                  "veg",
                  "services"
                ],
                "catalogueId": "513068376"
              },
              "displayCost": "₹30",
              "dishUnitCost": 10,
              "dishTotalCost": 30
            },
            {
              "id": "8",
              "name": "Fish Fry Ayala (Mackerel )",
              "referenceType": "DRT_VARIANT",
              "referenceId": "531186222",
              "quantity": 2,
              "unitCost": 220,
              "totalCost": 440,
              "subCategoryId": "41871022",
              "calculations": [
                {
                  "id": "9",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 440,
                  "entityType": "DCT_VOUCHER_DISCOUNT",
                  "entityId": "2137537187",
                  "value": 44,
                  "amount": 44,
                  "calcAppliedOnAmount": 440,
                  "appliedPercentageValue": 44,
                  "calcAmount": 44
                },
                {
                  "id": "10",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 440,
                  "name": "taxable_discount",
                  "entityType": "DCT_TOTAL_TAXABLE_DISCOUNT",
                  "value": 44,
                  "amount": 44,
                  "calcAppliedOnAmount": 440,
                  "appliedPercentageValue": 44,
                  "calcAmount": 44
                },
                {
                  "id": "11",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 396,
                  "name": "CGST",
                  "entityType": "DCT_TAX",
                  "entityId": "4",
                  "isPercentage": true,
                  "value": 2.5,
                  "amount": 9.89999962,
                  "calcAppliedOnAmount": 396,
                  "appliedPercentageValue": 2.5,
                  "calcAmount": 9.9
                },
                {
                  "id": "12",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 396,
                  "name": "SGST",
                  "entityType": "DCT_TAX",
                  "entityId": "3",
                  "isPercentage": true,
                  "value": 2.5,
                  "amount": 9.89999962,
                  "calcAppliedOnAmount": 396,
                  "appliedPercentageValue": 2.5,
                  "calcAmount": 9.9
                },
                {
                  "id": "13",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 396,
                  "name": "CGST",
                  "entityType": "DCT_SOURCE_TAX",
                  "entityId": "4",
                  "isPercentage": true,
                  "value": 2.5,
                  "amount": 9.89999962,
                  "calcAppliedOnAmount": 396,
                  "appliedPercentageValue": 2.5,
                  "calcAmount": 9.9
                },
                {
                  "id": "14",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 396,
                  "name": "SGST",
                  "entityType": "DCT_SOURCE_TAX",
                  "entityId": "3",
                  "isPercentage": true,
                  "value": 2.5,
                  "amount": 9.89999962,
                  "calcAppliedOnAmount": 396,
                  "appliedPercentageValue": 2.5,
                  "calcAmount": 9.9
                }
              ],
              "metadata": {
                "tags": [
                  "non-veg",
                  "restaurant-recommended",
                  "starter",
                  "medium-spicy",
                  "home-style-meal",
                  "services",
                  "discounted-addon"
                ],
                "catalogueId": "430669415"
              },
              "displayCost": "₹440",
              "dishUnitCost": 220,
              "dishTotalCost": 440
            },
            {
              "id": "15",
              "name": "Boiled White Rice",
              "referenceType": "DRT_VARIANT",
              "referenceId": "533002872",
              "quantity": 3,
              "unitCost": 110,
              "totalCost": 330,
              "subCategoryId": "37863158",
              "calculations": [
                {
                  "id": "16",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 330,
                  "entityType": "DCT_VOUCHER_DISCOUNT",
                  "entityId": "2137537187",
                  "value": 33,
                  "amount": 33,
                  "calcAppliedOnAmount": 330,
                  "appliedPercentageValue": 33,
                  "calcAmount": 33
                },
                {
                  "id": "17",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 330,
                  "name": "taxable_discount",
                  "entityType": "DCT_TOTAL_TAXABLE_DISCOUNT",
                  "value": 33,
                  "amount": 33,
                  "calcAppliedOnAmount": 330,
                  "appliedPercentageValue": 33,
                  "calcAmount": 33
                },
                {
                  "id": "18",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 297,
                  "name": "CGST",
                  "entityType": "DCT_TAX",
                  "entityId": "4",
                  "isPercentage": true,
                  "value": 2.5,
                  "amount": 7.42500019,
                  "calcAppliedOnAmount": 297,
                  "appliedPercentageValue": 2.5,
                  "calcAmount": 7.425
                },
                {
                  "id": "19",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 297,
                  "name": "SGST",
                  "entityType": "DCT_TAX",
                  "entityId": "3",
                  "isPercentage": true,
                  "value": 2.5,
                  "amount": 7.42500019,
                  "calcAppliedOnAmount": 297,
                  "appliedPercentageValue": 2.5,
                  "calcAmount": 7.425
                },
                {
                  "id": "20",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 297,
                  "name": "CGST",
                  "entityType": "DCT_SOURCE_TAX",
                  "entityId": "4",
                  "isPercentage": true,
                  "value": 2.5,
                  "amount": 7.42500019,
                  "calcAppliedOnAmount": 297,
                  "appliedPercentageValue": 2.5,
                  "calcAmount": 7.425
                },
                {
                  "id": "21",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 297,
                  "name": "SGST",
                  "entityType": "DCT_SOURCE_TAX",
                  "entityId": "3",
                  "isPercentage": true,
                  "value": 2.5,
                  "amount": 7.42500019,
                  "calcAppliedOnAmount": 297,
                  "appliedPercentageValue": 2.5,
                  "calcAmount": 7.425
                }
              ],
              "metadata": {
                "tags": [
                  "veg",
                  "services"
                ],
                "catalogueId": "432161136"
              },
              "displayCost": "₹330",
              "dishUnitCost": 110,
              "dishTotalCost": 330
            },
            {
              "id": "22",
              "name": "Sambar [Serves 2]",
              "referenceType": "DRT_VARIANT",
              "referenceId": "477134553",
              "quantity": 1,
              "unitCost": 100,
              "totalCost": 100,
              "subCategoryId": "37863154",
              "calculations": [
                {
                  "id": "23",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 100,
                  "entityType": "DCT_VOUCHER_DISCOUNT",
                  "entityId": "2137537187",
                  "value": 10,
                  "amount": 10,
                  "calcAppliedOnAmount": 100,
                  "appliedPercentageValue": 10,
                  "calcAmount": 10
                },
                {
                  "id": "24",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 100,
                  "name": "taxable_discount",
                  "entityType": "DCT_TOTAL_TAXABLE_DISCOUNT",
                  "value": 10,
                  "amount": 10,
                  "calcAppliedOnAmount": 100,
                  "appliedPercentageValue": 10,
                  "calcAmount": 10
                },
                {
                  "id": "25",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 90,
                  "name": "CGST",
                  "entityType": "DCT_TAX",
                  "entityId": "4",
                  "isPercentage": true,
                  "value": 2.5,
                  "amount": 2.25,
                  "calcAppliedOnAmount": 90,
                  "appliedPercentageValue": 2.5,
                  "calcAmount": 2.25
                },
                {
                  "id": "26",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 90,
                  "name": "SGST",
                  "entityType": "DCT_TAX",
                  "entityId": "3",
                  "isPercentage": true,
                  "value": 2.5,
                  "amount": 2.25,
                  "calcAppliedOnAmount": 90,
                  "appliedPercentageValue": 2.5,
                  "calcAmount": 2.25
                },
                {
                  "id": "27",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 90,
                  "name": "CGST",
                  "entityType": "DCT_SOURCE_TAX",
                  "entityId": "4",
                  "isPercentage": true,
                  "value": 2.5,
                  "amount": 2.25,
                  "calcAppliedOnAmount": 90,
                  "appliedPercentageValue": 2.5,
                  "calcAmount": 2.25
                },
                {
                  "id": "28",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 90,
                  "name": "SGST",
                  "entityType": "DCT_SOURCE_TAX",
                  "entityId": "3",
                  "isPercentage": true,
                  "value": 2.5,
                  "amount": 2.25,
                  "calcAppliedOnAmount": 90,
                  "appliedPercentageValue": 2.5,
                  "calcAmount": 2.25
                }
              ],
              "metadata": {
                "tags": [
                  "veg",
                  "chef-special",
                  "main-course",
                  "medium-spicy",
                  "home-style-meal",
                  "services"
                ],
                "catalogueId": "385080781"
              },
              "displayCost": "₹100",
              "dishUnitCost": 100,
              "dishTotalCost": 100
            },
            {
              "id": "29",
              "name": "Kerala Red Fish Curry",
              "referenceType": "DRT_VARIANT",
              "referenceId": "477134562",
              "quantity": 1,
              "unitCost": 220,
              "totalCost": 220,
              "subCategoryId": "37863154",
              "calculations": [
                {
                  "id": "30",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 220,
                  "entityType": "DCT_VOUCHER_DISCOUNT",
                  "entityId": "2137537187",
                  "value": 22,
                  "amount": 22,
                  "calcAppliedOnAmount": 220,
                  "appliedPercentageValue": 22,
                  "calcAmount": 22
                },
                {
                  "id": "31",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 220,
                  "name": "taxable_discount",
                  "entityType": "DCT_TOTAL_TAXABLE_DISCOUNT",
                  "value": 22,
                  "amount": 22,
                  "calcAppliedOnAmount": 220,
                  "appliedPercentageValue": 22,
                  "calcAmount": 22
                },
                {
                  "id": "32",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 198,
                  "name": "CGST",
                  "entityType": "DCT_TAX",
                  "entityId": "4",
                  "isPercentage": true,
                  "value": 2.5,
                  "amount": 4.94999981,
                  "calcAppliedOnAmount": 198,
                  "appliedPercentageValue": 2.5,
                  "calcAmount": 4.95
                },
                {
                  "id": "33",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 198,
                  "name": "SGST",
                  "entityType": "DCT_TAX",
                  "entityId": "3",
                  "isPercentage": true,
                  "value": 2.5,
                  "amount": 4.94999981,
                  "calcAppliedOnAmount": 198,
                  "appliedPercentageValue": 2.5,
                  "calcAmount": 4.95
                },
                {
                  "id": "34",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 198,
                  "name": "CGST",
                  "entityType": "DCT_SOURCE_TAX",
                  "entityId": "4",
                  "isPercentage": true,
                  "value": 2.5,
                  "amount": 4.94999981,
                  "calcAppliedOnAmount": 198,
                  "appliedPercentageValue": 2.5,
                  "calcAmount": 4.95
                },
                {
                  "id": "35",
                  "appliedOnType": "DCAOT_DISH",
                  "appliedOnAmount": 198,
                  "name": "SGST",
                  "entityType": "DCT_SOURCE_TAX",
                  "entityId": "3",
                  "isPercentage": true,
                  "value": 2.5,
                  "amount": 4.94999981,
                  "calcAppliedOnAmount": 198,
                  "appliedPercentageValue": 2.5,
                  "calcAmount": 4.95
                }
              ],
              "metadata": {
                "tags": [
                  "non-veg",
                  "medium-spicy",
                  "services"
                ],
                "catalogueId": "385080790"
              },
              "displayCost": "₹220",
              "dishUnitCost": 220,
              "dishTotalCost": 220
            }
          ]
        },
        "charges": [
          {
            "amountDetails": {
              "id": "36",
              "itemName": "Taxes",
              "quantity": 1,
              "type": "tax",
              "unitCost": 50.4000015,
              "displayCost": "₹0",
              "amountTotalCost": 50.4,
              "amountUnitCost": 50.4
            },
            "amountBreakup": {
              "title": "Taxes",
              "body": {
                "keyValues": [
                  {
                    "key": {
                      "message": "Net tax on order (paid by customer)"
                    },
                    "value": {
                      "message": "₹50.40"
                    }
                  },
                  {
                    "key": {
                      "message": "GST on restaurant services under section 9(5)"
                    },
                    "value": {
                      "message": "-₹50.40"
                    }
                  }
                ],
                "footer": {
                  "key": {
                    "message": "Net tax transferrable to restaurant"
                  },
                  "value": {
                    "message": "₹0.00"
                  }
                }
              }
            }
          }
        ],
        "subtotal": {
          "amountDetails": {
            "id": "38",
            "itemName": "Item total",
            "totalCost": 1120,
            "type": "subtotal2",
            "displayCost": "₹1120",
            "amountTotalCost": 1120
          }
        },
        "total": {
          "amountDetails": {
            "id": "32087375554",
            "itemName": "Total Bill",
            "quantity": 1,
            "totalCost": 1008,
            "type": "total_merchant",
            "unitCost": 1008,
            "displayCost": "₹1008",
            "amountTotalCost": 1008,
            "amountUnitCost": 1008
          }
        },
        "discountApplied": {
          "discounts": [
            {
              "discount": {
                "id": "-1",
                "name": "Promo",
                "type": "total_merchant_voucher_and_salt_discount",
                "offers": [
                  {
                    "type": "PERCENTAGE_DISCOUNT",
                    "amount": -112,
                    "offerAmount": 112
                  }
                ],
                "totalDiscountAmount": -112,
                "displayCost": "-₹112"
              },
              "amountBreakup": {
                "title": "Promo",
                "body": {
                  "keyValues": [
                    {
                      "key": {
                        "message": "Zomato Promo"
                      },
                      "value": {
                        "message": "-₹112"
                      }
                    }
                  ],
                  "footer": {
                    "key": {
                      "message": "Promo"
                    },
                    "value": {
                      "message": "-₹112"
                    }
                  }
                }
              }
            }
          ]
        }
      },
      "supportingRiderDetails": [
        {
          "name": "xxxx",
          "image": "xxxx",
          "phone": "xxxx",
          "gender": "MALE",
          "pickup": "2023-06-09T15:10:00Z",
          "drop": "2023-06-09T15:22:36Z",
          "riderStatus": "ARRIVED",
          "riderMask": {
            "rootQuestionId": 6,
            "questions": [
              {
                "id": 6,
                "name": "Is xxxx wearing a face mask?",
                "parentId": -1,
                "type": "BUTTON",
                "options": [
                  {
                    "optionId": 1,
                    "name": "Yes",
                    "childId": -1,
                    "isValid": true
                  },
                  {
                    "optionId": 2,
                    "name": "No",
                    "childId": -1,
                    "isValid": true
                  }
                ]
              }
            ]
          },
          "assignedAt": "2023-06-09T14:46:28Z",
          "riderArrivedAt": "2023-06-09T14:49:50Z"
        },
        {
          "name": "xxxxx",
          "desc": "xxxx",
          "image": "xxxx",
          "phone": "8975147417",
          "gender": "MALE",
          "riderStatus": "ASSIGNED",
          "additionalRiderInfo": {
            "message": "2 delivery partners assigned! Hand over the order when both delivery partners have arrived.",
            "highlightText": "2 delivery partners assigned!"
          }
        }
      ],
      "orderActions": [
        {
          "type": "RIDER_REQUEST",
          "status": "ACTION_TAKEN",
          "redirectText": {
            "message": "Request for extra delivery partner?",
            "icon": "e996"
          }
        },
        {
          "type": "RIDER_REQUEST",
          "title": {
            "message": "Looks like a large order"
          },
          "status": "ACTION_TAKEN",
          "subtitle": {
            "message": "Do you require one more delivery partner to carry this food?"
          },
          "redirectText": {
            "message": "Request for extra delivery partner?",
            "icon": "e996"
          }
        }
      ],
      "delayInfo": {
        "stateMachine": [
          {
            "state": "NO_DELAY",
            "startAt": "2023-06-09T14:28:16Z",
            "expireAt": "2023-06-09T15:17:16Z"
          },
          {
            "state": "DELAY_BUTTON_INPUT_EXPECTED",
            "startAt": "2023-06-09T15:17:16Z",
            "expireAt": "2023-06-09T15:32:16Z"
          },
          {
            "state": "DELAY_INPUT_EXPIRED",
            "startAt": "2023-06-09T15:32:16Z",
            "expireAt": "2023-06-10T15:32:16Z"
          }
        ]
      },
      "displayId": "3288",
      "isAdditionalHelpInputRequired": true,
      "topBannerUrl": "https://b.zmtcdn.com/data/o2_assets/4c97c2e830da9c215a8f4ac2119936901658922017.png"
    }
  }
}
```

