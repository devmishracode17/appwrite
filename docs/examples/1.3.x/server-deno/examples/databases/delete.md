import * as sdk from "https://deno.land/x/appwrite/mod.ts";

// Init SDK
let client = new sdk.Client();

let databases = new sdk.Databases(client);

client
    .setEndpoint('https://[HOSTNAME_OR_IP]/v1') // Your API Endpoint
    .setProject('5df5acd0d48c2') // Your project ID
    .setKey('919c2d18fb5d4...a2ae413da83346ad2') // Your secret API key
;


let promise = databases.delete('[DATABASE_ID]');

promise.then(function (response) {
    console.log(response);
}, function (error) {
    console.log(error);
});