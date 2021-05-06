# Add a pet
Adds a new pet with with defining categories.

**Note:** An <a href="http://www.google.com">access token</a> is required for this endpoint.

| Method| Endpoint | Description |
|---|---|---|
| POST| http://api.nylas.com/pet/addapet/access_token=ACCESSTOKEN| Adds a new pet with additional descriptive fields described below.|

## Request Schema

<table>
	<tr>
		<th>Field Name</th>
		<th>Type</th>
		<th>Description</th>
		<th>Required</th>
	</tr>
	<tr>
		<td>category</td>
		<td colspan="3">An object containing animal details</td>
	</tr>
	<tr>
		<td>&nbsp &nbsp name</td>
		<td>String</td>
		<td>Main animal category classification<br>
		ex.  <em>breed<em>
	</td>
		<td>Yes</td>
	<tr>
		<td>&nbsp &nbsp sub</td>
		<td colspan="3">An object containing secondary animal details </td>
	</tr>	
	<tr>
		<td>&nbsp &nbsp &nbsp &nbsp prop1</td>
		<td>String</td>
		<td>Secondary animal description. <br>
		ex. "Male", "Female"</td>
		<td>Yes</td>
	</tr>
	<tr>
		<td>name</td>
		<td>String</td>
		<td>The animals name</td>
		<td>Yes</td>
	</tr>
	<tr>
		<td>photoURLs</td>
		<td>Array</td>
		<td>Contains an array of URL strings to images</td>
		<td>No</td>
	</tr>
	<tr>
		<td>tags</td>
		<td colspan="3">An array used to define pets by age</td>
	</tr>
	<tr>
		<td>&nbsp &nbsp name</td>
		<td>String</td>
		<td>Age group associated with tag <br>ex. "Kitten, "Juvenile, "Adult"...</td>
		<td>No</td>
	</tr>
	<tr>
		<td>status</td>
		<td>String</td>
		<td>Animal adoption status. Entries limited to “Available”, “Pending”, and “Not Available”</td>
		<td>Yes</td>
	</tr>
	<tr>
		<td>petType</td>
		<td>String</td>
		<td>Type of animal<br> Entries currently limited to “Cat”, “Dog”, "Rabbit", and "Fish"</td>
		<td>Yes</td>
	</tr>
</table>

## JSON Request

```
{
  "category": { 
    "name": "American Shorthair",
    "sub": {
      "prop1": "Female"
    }
  },
  "name": "Pyewacket",
  "photoUrls": [
    "www.google.com"
  ],
  "tags": [
    {
      "name": "Adult"
    }
  ],
  "status": "Not Available",
  "petType": "Cat", 
}
```

## Responses

|HTTP Codes| HTTP Response | Description|
|---|---|---|
|200|OK|New pet successfully created|
|405|Method Not Allowed| Invalid information. New pet was not created.|



