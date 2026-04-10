Duino Coin API for getting price of the duinocoin in different currencies

The API documentation is avaiable at: https://api.itzzztomas.xyz/api/ 
Use `https://api.itzzztomas.xyz` for any api request

## How it works?
By using currencyratesapi.com it converts the duco price to the targeted currency. 

My API uses Euro as base currency, so it stores duco price for any conversion in EUR.
> Why? Euro is more stables and in my opinion it is more versatile with converting to different currencies.

## Why Ive made it?
I made it mainly for my next project, a swap!
But wanted to publish it for things like dashboards and different projects that just need a simple API request to convert the currency.

With most APIs for currency is that it has a problem with CORS. Many duco dashboards do request locally via the javascript, which can result in CORS request errors.

## Hosting and stability
For now I am hosting it on my raspberry pi 5 via cloudflare tunnel. I dont have a better solution atp.

The API can be down for few minutes due to my network instability. But not for longer than 5 minutes 2x per day. This downtime can varry. I will have an access to fiber optic ISP so the stability will improve. But for now I certain that this instabillity can cause any big problems. My network is recently more stabler and I dont recorded any major incidents in the past month.

## How request are handled?
The specific currency can be requested via header. More specifications are included in the https://api.itzzztomas.xyz/api/  api documentation by swagger.

I also have included some error handling. The api will return a `success` header with `false` or `true` value with additional error message if the request failed.

## Code availability
I will be publishing the code when the API code would be more mature

The API is coded in node.js with express
> I think the node.js is very lightweight and faster than flask or different python API implementions while being easy to develop and maintain
