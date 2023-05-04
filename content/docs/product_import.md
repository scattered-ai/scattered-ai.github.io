---
title: "Product Import"
weight: 1
# bookFlatSection: false
# bookToc: true
# bookHidden: false
# bookCollapseSection: false
# bookComments: false
# bookSearchExclude: false
---

# Product Feed Importer Documentation

The product feed importer accepts a list of retail products in CSV format. Each retail product object should contain the following fields:


- externalId (string): The client's desired product ID. This is the same ID used in the response.
- advertiserName (string): The name of the seller on the retailer site. This allows the display of only relevant products when an advertiser sets up a campaign.
- name (string): The name of the product.
- description (string): A description of the product.
- brand (string): The brand of the product.
- category (string): The category of the product. This is the same category used in the request.
- productCodeType (string): The type of product code. Accepted values are "UPC", "EAN", "JAN", "ISBN", "ITF-14", and "CUSTOM". All types except "CUSTOM" have validation.
- productCode (string): The product code, corresponding to the productCodeType.
- imageUrl (string): The URL of the product's image, used for displaying a thumbnail of the product when setting up a campaign.


## Example

```csv
id,advertiser_name,name,description,brand,category,product_code_type,product_code,image_url
11,advertiser 1,product 1,Just product 1. Nothing fancy,Wigry3,bikes,EAN,5901234123457,https://test.domain.com/product-1.jpg
12,advertiser 1,product 2,Just product 2. Nothing fancy,BMW,cars,EAN,8712345678901,https://test.domain.com/product-2?abc=1&abc=2.jpg
13,advertiser 1,Product 3,Just `product` 3. 'Nothing' fancy.,BearMass,nutrition,EAN,4012345678909,https://test.domain.com/product-3.jpg
21,advertiser 2,Product 1,Just `product` 1. 'Nothing' fancy.,Orielly,books,EAN,5051234567890,https://test.domain.com/product-1.jpg
22,advertiser 2,Product 2,Just `product` 2. 'Nothing' fancy.,Orielly,books,EAN,5701234567897,https://test.domain.com/product-2.jpg
23,advertiser 2,Product 3,Just `product` 3. 'Nothing' fancy.,Samsung,electronics,EAN,8001234567892,https://test.domain.com/product-3.jpg
24,advertiser 2,Product 4,Just `product` 4. 'Nothing' fancy.,Orielly,books,EAN,7791234567896,https://test.domain.com/product-4.jpg
25,advertiser 2,Product 5,Just `product` 5. 'Nothing' fancy.,Samsung,electronics,EAN,8431234567894,https://test.domain.com/product-5.jpg
26,advertiser 2,Product 6,Just `product` 6. 'Nothing' fancy.,Samsung,electronics,EAN,5391234567894,https://test.domain.com/product-6.jpg
27,advertiser 2,Product 7,Just `product` 7. 'Nothing' fancy.,Muscle Mass,sport,EAN,5391234567894,https://test.domain.com/product-7.jpg
28,advertiser 2,Product 8,Just `product` 8. 'Nothing' fancy.,Ikea,furniture,EAN,8591234567894,https://test.domain.com/product-8.jpg
29,advertiser 2,Product 9,Just `product` 9. 'Nothing' fancy.,Ikea,furniture,EAN,8051234567894,https://test.domain.com/product-9.jpg
31,advertiser 3,Product 1,Just `product` 1. 'Nothing' fancy.,John Deer,agriculture,EAN,8501234567894,https://test.domain.com/product-1.jpg
32,advertiser 3,Product 2,Just `product` 2. 'Nothing' fancy.,John Deer,agriculture,EAN,8431234567894,https://test.domain.com/product-2.jpg
33,advertiser 3,Product 3,Just `product` 3. 'Nothing' fancy.,BMW,cars,EAN,8421234567894,https://test.domain.com/product-3.jpg
34,advertiser 3,Product 4,Just `product` 4. 'Nothing' fancy.,GreenPacks,tourism,EAN,8391234567894,https://test.domain.com/product-4.jpg
35,advertiser 3,Product 5,Just `product` 5. 'Nothing' fancy.,Wigry3,bikes,EAN,8881234567894,https://test.domain.com/product-5.jpg
36,advertiser 3,Product 6,Just `product` 6. 'Nothing' fancy.,Wigry3,bikes,EAN,8741234567894,https://test.domain.com/product-6.jpg
37,advertiser 3,Product 7,Just `product` 7. 'Nothing' fancy.,Plastics Inc.,random,EAN,8351234567894,https://test.domain.com/product-7.jpg
38,advertiser 3,Product 8,Just `product` 8. 'Nothing' fancy.,Plastics Inc.,random,CUSTOM,🫠🙃,https://test.domain.com/product-8.jpg
```