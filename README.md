# Nylas Technical Writer Take Home

Thanks for taking the time to complete the Nylas take-home. :tada:

The take-home consists of 2 parts:

* Writing sample
* API exercise;  Nylas is an API company, after all. 


## Writing Sample

Provide a link to your favorite thing you've ever written. It does not have to be documentation related or technical in any way. 
You can also include links to any writing samples that were not part of your application.

## API Exercise

Explain how to create a new `Pet` using the provided documentation below. 

### Proposed Endpoint Add a new Pet

**Example Payload**

application/json

name is required to make a pet

```text
{
  "category": { //what category the pet belongs to
    "name": "string", //category name
    "sub": {
      "prop1": "string" //maybe a sub category for the pet
    }
  },
  "name": "Guru", //pet name
  "photoUrls": [
    "string" // phots of the pet. We aren't going to store images, so provide a URL
  ],
  "tags": [
    {
      "name": "string" //let them provide their tags as a way to organize the pets
    }
  ],
  "status": "available", //is the pet avail for adoptions. can also have pending_adoption and adopted.
  "petType": "cat", //what type of pet. Let's start with cat, dog, rabbit and fish. add more as we get feedback.
}
```

**Endpoint**

http://api.nylas.com/pet


**Returns**

Should return 200 Created and 405 Invalid Input

**Auth**
Let's stay with Bearer auth using the access_token with scopes of `write:pets` and `read:pets`.


## Bonus

Use the [Open API 3.0](https://github.com/OAI/OpenAPI-Specification/blob/master/versions/3.0.0.md) specification to document the endpoint. 

## Submitting

* Fork this repo
* Create a new branch on your fork
* Add the link to your writing sample somewhere in the branch and your API documentation.
* Share the link, or if it's private, add me as a contributor @tjperry07.

Not sure how to use GitHub, share what you made using Google Drive or Dropbox. 

If something isn't clearly explained, don't hesitate to email us back. 

## Tools

* [Hemingway](http://www.hemingwayapp.com/)
* [Grammarly](https://www.grammarly.com/)
* [Stoplight](https://stoplight.io/)
* [editor.swagger.io](https://editor.swagger.io/)
* [Redoc](https://github.com/Redocly/redoc)
* [RapiDoc](https://mrin9.github.io/RapiDoc/)
* [I'd rather be writing](https://idratherbewriting.com/learnapidoc/)
* [OpenAPI.Tools](https://openapi.tools/)
* [Postman](https://www.postman.com/)
