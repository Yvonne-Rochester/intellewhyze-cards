// sampleGetItemsApi.js

const fs    = require('fs');
const PAAPI = require('paapi5-nodejs-sdk');

// 1) Configure the singleton client
const defaultClient = PAAPI.ApiClient.instance;
defaultClient.accessKey = 'AKPA3RZ70D1746755668';
defaultClient.secretKey = 'ijfasno0HbZS1XCj7Bd3eoGLpGdoZwXcXUGkxOKw';
defaultClient.host      = 'webservices.amazon.com';
defaultClient.region    = 'us-east-1';

// 2) Create the API object
const api = new PAAPI.DefaultApi();

// 3) Build the GetItems request for your 10 ASINs
const request = new PAAPI.GetItemsRequest();
request.PartnerTag  = 'intellewhyze-20';
request.PartnerType = 'Associates';
request.ItemIds     = [
  'B0B6JSFPLN','B07BHCB9Y2','B0DKWYYP5F','B0BFNH9694',
  'B0C7H38YBT','B0DLKT9YF9','B0CNPMZH5B','B0D95BR9GG',
  'B0BDD7D34M','B07GBFT6Z3'
];
request.Resources   = [
  'ItemInfo.Title',
  'Images.Primary.Medium',
  'Offers.Listings.Price'
];

// 4) Fetch items and write a fully styled HTML page
api.getItems(request, (err, data) => {
  if (err) {
    console.error('API error:', JSON.stringify(err, null, 2));
    return;
  }

  const items = data.ItemsResult.Items || [];
  let html = `<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Featured Products</title>
  <style>
    body { font-family: sans-serif; padding: 1rem; margin: 0; }
    h1 { text-align: center; margin-bottom: 1rem; }
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
      gap: 1rem;
      padding: 0 1rem 1rem;
      max-width: 1200px;
      margin: 0 auto;
    }
    .product-card {
      display: flex;
      flex-direction: column;
      padding: 0.75rem;
      border: 1px solid #ddd;
      border-radius: 4px;
      background: #fff;
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
      transition: transform 0.2s, box-shadow 0.2s;
      height: auto;
    }
    .product-card:hover {
      transform: translateY(-4px);
      box-shadow: 0 6px 12px rgba(0,0,0,0.15);
    }
    .product-thumb {
      flex: 0 0 auto;
      margin-bottom: 0.5rem;
      text-align: center;
    }
    .product-thumb img {
      max-width: 100%;
      height: auto;
      border-radius: 4px;
    }
    .product-title {
      font-size: 0.95rem;
      line-height: 1.2;
      min-height: calc(1.2em * 3);
      margin: 0 0 0.5rem;
      overflow-wrap: break-word;
      hyphens: auto;
    }
    .price {
      color: #088A08;
      font-weight: bold;
      margin-bottom: 0.75rem;
      flex: 0 0 auto;
    }
    .buy-button {
      margin-top: auto;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      padding: 0.5rem 0.75rem;
      background: #FF9900;
      color: #fff;
      text-decoration: none;
      border-radius: 3px;
      font-size: 0.9rem;
      transition: background 0.2s;
    }
    .buy-button:hover {
      background: #e88b00;
    }
    .buy-button img {
      height: 1em;
      margin-right: 0.4em;
      vertical-align: middle;
    }
    /* Smartphones: single column */
@media (max-width: 600px) {
  .cards-container {
    grid-template-columns: 1fr;
  }
}

/* Small tablets: two columns */
@media (min-width: 601px) and (max-width: 900px) {
  .cards-container {
    grid-template-columns: repeat(2, 1fr);
  }
}

/* Large tablets / small desktops: three columns */
@media (min-width: 901px) and (max-width: 1200px) {
  .cards-container {
    grid-template-columns: repeat(3, 1fr);
  }
}

/* Desktops and up: you can leave the auto-fit or force 4+ columns */
// @media (min-width: 1201px) {
//   .cards-container {
//     grid-template-columns: repeat(4, 1fr);
//   }
// }
  </style>
</head>
<body>
  <h1>Featured Products</h1>
  <div class="grid">`;

  items.forEach(item => {
    const title    = item.ItemInfo.Title.DisplayValue;
    const thumb    = item.Images.Primary.Medium.URL;
    const priceObj = item.Offers.Listings[0]?.Price;
    const price    = priceObj ? priceObj.DisplayAmount : 'See price';
    const url      = item.DetailPageURL;

    html += `
    <div class="product-card">
      <div class="product-thumb">
        <a href="${url}" target="_blank">
          <img src="${thumb}" alt="${title}">
        </a>
      </div>
      <div class="product-title">${title}</div>
      <div class="price">${price}</div>
      <a class="buy-button" href="${url}" target="_blank">
        <img src="https://raw.githubusercontent.com/Yvonne-Rochester/intellewhyze-cards/main/Amazon_logo.svg" alt="Amazon logo">
        Buy on Amazon
      </a>
    </div>`;
  });

  html += `
  </div>
</body>
</html>`;

  fs.writeFileSync('index.html', html, 'utf8');
  console.log('✅ index.html created!');
});
