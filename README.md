# DisplayImageFromURL



From this image:
https://assets2.sportsnet.ca/wp-content/uploads/2018/06/beckham-1040x572.jpg
![alt text](https://assets2.sportsnet.ca/wp-content/uploads/2018/06/beckham-1040x572.jpg)

This code will fetch online to dislay on the UIImageViewer in App Swift:
![alt text](https://github.com/taminhtu/DisplayImageFromURL/blob/master/Screen%20Shot%202018-09-05%20at%2022.51.43.png)


You can watch the video here:

[![Watch the video](https://raw.github.com/GabLeRoux/WebMole/master/ressources/WebMole_Youtube_Video.png)](https://www.youtube.com/watch?v=4m66M7KJuX4&t=416s)


If the image file that you get from un-secure link (http but not https), you can fix the error by openning the info.plist file as source code and add this xml code: 
```
<key>NSAppTransportSecurity</key>
    <dict>
        <key>NSAllowsArbitraryLoads</key>
        <true/>
        <key>NSExceptionDomains</key>
        <dict>
            <key>yourdomain.com</key>
            <dict>
                <key>NSIncludesSubdomains</key>
                <true/>
                <key>NSThirdPartyExceptionRequiresForwardSecrecy</key>
                <false/>
            </dict>
       </dict>
  </dict>
```
