# LSApplicationQueriesSchemes-Working-Example
iOS 9 introduces LSApplicationQueriesSchemes to allow apps to query if other apps are installed. This project provides two sample apps TestA and TestB which are querying for each other.

* Both TestA and TestB define a URL Scheme within their info.plist files
* Both TestA adds TestB to its LSApplicationQueriesSchemes inside info.plist and vice versa. 
* Thus both apps are allowed to query for each other. 