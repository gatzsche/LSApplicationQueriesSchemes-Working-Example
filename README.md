# LSApplicationQueriesSchemes-Working-Example
iOS 9 introduces LSApplicationQueriesSchemes to allow apps to query if other apps are installed. This project provides two sample apps TestA and TestB which are querying for each other. 

In its info.plist file TestA defines the following URL schemes: 

'''
<key>CFBundleURLSchemes</key>
<array>
  <string>testA</string>
</array>
'''

TestB wants to check if TestA is installed by calling

'''
BOOL canBeOpened = [[UIApplication sharedApplication] 
                   canOpenURL:[NSURL URLWithString:@"TestA.scheme2://"]];
'''

This is normally not allowed in iOS9. But by adding the following code to TestB's info.plist file, the query will return YES:

'''
<key>LSApplicationQueriesSchemes</key>
<array>
  <string>TestA</string>
</array>
'''


