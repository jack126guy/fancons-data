# Jack "Fox" Grayson's Fan-Con Data

This dataset lists the fan conventions I have attended (or will be attending), and primarily supports the [fan conventions page](https://www.jackgraysonfox.xyz/fancons/) on my website.

## Format

The dataset consists of two JSON files, one with conventions and another with tag colors for use on the website.

### Conventions

The `conventions.json` file contains a list of conventions with basic event information.

This is represented as an array of objects, where each object has the following members:

* **name**: (String) Name of the event, including year or number
* **start_date**: (String, optional) Start date in ISO 8601 YYYY-MM-DD format
* **end_date**: (String, optional) End date in ISO 8601 YYYY-MM-DD format
* **location**: (Object, optional) Location of (primary) venue
	* **venue**: (String, optional) Name of venue
	* **locality**: (String, optional) City, town, or similar settlement
	* **region**: (String, optional) Subnational region, to distinguish between different localities with the same name in countries such as the United States
	* **country**: (String) Identifiable region of the world, often but not necessarily a sovereign state
* **metropolis**: (Object, optional) Metropolitan city or other settlement, for grouping events by metropolitan area
	* **locality**, **region**, **country**: Similar to the members of the **location** object, except representing the metropolis
* **series**: (String) Name of the series of events that the event belongs to
* **specifier**: (String) Specifier that identifies the event within the series, often a year
* **genre**: (String) Genre, fandom, or community that the convention appeals to
* **status**: (String) Attendance status, one of "Attending", "Tentative", or "Not Attending"
* **notes**: (String, optional) Additional explanatory notes, especially when the attendance status is "Tentative" or "Not Attending"
* **extra_tags**: (Array, optional) Extra status tags, as an array of arbitrary strings

### Tag Colors

The `tagColors.json` file contains colors corresponding to the different genres, statuses, and extra status tags in the convention data. These are used on the website as colors for different annotation tags.

This is represented as an object with the following members:

* **genre**: Colors for genres
* **status**: Colors for statuses
* **extra**: Colors for extra status tags

The value of each member is an object mapping the different items (as they appear in the convention data) to CSS color strings.

## License

This dataset and documentation are dedicated to the public domain under [Creative Commons CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/). (A copy is available in `LICENSE.txt`.)
