# Name Guesser

JSON module to guess a user's name and company from just an email address.

Made by the team at **Weld** ([www.weld.io](https://www.weld.io?utm_source=github-name-guesser)), the code-free app and web creation tool:

[![Weld](https://s3-eu-west-1.amazonaws.com/weld-social-and-blog/gif/weld_explained.gif)](https://www.weld.io?utm_source=github-name-guesser)


## Screenshot

![Name Guesser example](example.png)

## Supported email formats

* *@firstnamelastname - e.g. hello@greglarson.com
* *lastname@ - e.g. glarson@gmail.com
* firstname*@ - e.g. gregory231@gmail.com
* firstname-lastname@
* firstname.*@
* firstname.lastname.lastname@ (multiple last names) - e.g. greg.larson.smith@gmail.com
* firstname.lastname@ - e.g. greg.larson@gmail.com
* firstname@ - e.g. greg@gmail.com
* firstname@lastname - e.g. greg@larson.com
* firstname_lastname@
* firstnamelastname@ (short firstname) - e.g. greglarson@gmail.com
* firstnamelastname@ - e.g. greglarson@gmail.com
* firstnamelastname@ - e.g. greglarson@gmail.com
* lastname*@ - e.g. larsong231@gmail.com
* lastname.firstname@
* lastnamefirstname@ - e.g. larsongreg@gmail.com

## Usage

Request:

	const nameGuess = require("./name-guesser-module/lib/emailtools");       // use the correct relative path to /lib/emailtools.js
	var resultJSON = nameGuess.processUser({email: "jane.doe@google.com"});
	console.log("%j", resultJSON);
	

Response:

	{
		email: "jane.doe@google.com",
		fullName: "Jane Doe"
		firstName: "Jane",
		lastName: "Doe",
		company: {
			name: "Google",
			id: "google",
			domain: "google.com"
		}
	}
