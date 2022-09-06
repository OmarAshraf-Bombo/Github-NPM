# ➖➖➖➖➖➖🔴 JSON 🔴➖➖➖➖➖➖

> JSON >> Javascript Object Notation

> JSON is a lightweight format for storing and transporting data

> JSON is often used when data is sent from a server to a web page

> JSON is "self-describing" and easy to understand.

> JSON is a String Shaped Object Which Contains Properties & Values.

> You Can Convert JSON Object to Javascript Object & Vice Versa.

> Alternative to XML

> Extension is `.json`

## Differnece Between JSON & XML ?

JSON is Text Base Format <br>
JSON is Light Weight <br>
JSON is Shorter <br>
JSON Don't Use Tags <br>
JSON Can Use Arrays <br>
JSON Don't Support Comments <br>

_-----------------------------------_

XML is a Markup Language <br>
XML is Heavier <br>
XML is Not Short <br>
XML Use Tags <br>
XML Can Not Use Arrays <br>
XML Support Comments <br>

## JSON Syntax

> Data is Written inside Curly Brackets `{ }`

> Data Contains Key & Value

> Key & value is Seperate by `:` // "Key": Value

> key Must Be Wrapped in Double Quotes

> Seperate Data by `,` Comma.

> Square Brackets `[]` Contains Arrays.

> Curly Brackets `{}` Contains Objetcs.

## JSON Data Types

#### JSON Supports 6 Data Types.....

1. Number
1. String
1. Object
1. Array
1. Bolean
1. Null

## JSON Example

```json
{
  "username": "Omar",
  "country": "Egypt",
  "skills": [
    ["HTML", "PugJs", "Haml"],
    ["CSS", "Sass", "Less"],
    ["JS", "Babel", "React"]
  ],
  "addresses": {
    "Egypt": "Giza",
    "KSA": "Riyadh",
    "Germany": ["Berlin", "Munich", "Stuttgar"]
  },
  "age": 29,
  "working": true,
  "id": null
}
```

## Accessing JSON Data

1. Using Dot Notation.

```javascript
objectName.username; // omar
objectName.country; // Egypt
objectName.skills; // Output is Skills Array
objectName.skills[2]; // Output is Last Array in Skills Array
objectName.age; // 29
objectName.addresses.KSA; // Riyadh
objectName.addresses.Germany[1]; // Munich
```

2. Using Bracket Notation [Square Notation].

```javascript
objectName["username"]; // omar
objectName["country"]; // Egypt
objectName["skills"]; // Output is Skills Array
objectName["skills"][2]; // Output is Last Array in Skills Array
objectName["age"]; // 29
objectName["addresses"]["KSA"]; // Riyadh
objectName["addresses"]["Germany"][1]; // Munich
```

## Parse & Stringify

### **Parse**

```javascript
let myJsonObject = '{"username": "omar", "age": 29}';   // String
let myJavascriptObject = JSON.parse(myJsonObject);

console.log(typeof myJavascriptObject);
// Output is Object
console.log(myJavascriptObject);
// Output is {username: "omar", age: 29}
// Parse Converted The JSON String To Javascript Object.
```

### **Stringify**

```javascript
let myJavascriptObject = { username: "omar", age: 29 }; // Object
let myJsonObject = JSON.stringify(myJavascriptObject);

console.log(typeof myJsonObject);
// Output is String
console.log(myJsonObject);
// Output is '{"username": "omar", "age": 29}'
// Stringify Converted The Javascript Object To JSON String.
```

## What Really Happens in Real Life.

> We Have an `API` Link Which Contains The `JSON` Data as String "Text"

> We Make an `XMLHttpRequest` To Get The Data..........`(AJAX)`

> We Send That Request

> We Receive The Data "Text"

> We Take The Data and `Parse` it Using `JSON.Parse()`

> Now We Have a Javascript Object Which We Can Use As We Need.

---

## You Can Check [AJAX](https://github.com/OmarAshraf-Bombo/Tutorials-and-CheatSheets/tree/main/AJAX) Tutorial to Understand The `XMLHttpRequest`.
