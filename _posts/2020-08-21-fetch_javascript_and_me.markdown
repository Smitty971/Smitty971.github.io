---
layout: post
title:      "Fetch, Javascript and Me"
date:       2020-08-21 15:33:42 +0000
permalink:  fetch_javascript_and_me
---





What was so hard about it? This is what I find myself asking after finishing my Javascript project. Before I started the project and during the early stages I struggled to understand exactly what it all was doing. Granted i think the lessons paint a clear picture. It felt like latin to me.

While I can't quite put my former thoughts to paper I can at least put Fetch into my own words. Fetch or an AJAX technique gives us a way to load more data after information is already displayed to users on a webpage.


		`fetch("heres a string of our data source")
		.then(function(response) {
			return response;
		})`

This is a pretty simple fetch where were pulling in data, calling something spefic and then telling the code to display the respone or input it into whatever you're changing it to. 
		For example heres a snippet from my project:

  

		getLists() {
			return fetch(this.baseUrl
			.then(res => res.json())
		}

All i'm doing here is fetching a set of lists from my db. Then taking the response or the code that I want and turning it into json

> Written with [StackEdit](https://stackedit.io/).
