# CuteScript
CuteNews 2.1.2 'avatar' RCE

 "The attacker can infiltrate the server through the avatar upload process in the profile area.
        There is no realistic control of the $imgsize function in "/core/modules/dashboard.php"
        Header content of the file can be changed and the control can be bypassed.
        We can use the "GIF" header for this process.
        An ordinary user is enough to exploit the vulnerability. No need for admin user."
        
        
        
        1.Rename shell to .gif
        2.load burp
        3.Upload new profile picture, capture the request and rename the file back to "revshell.php" and forward the request.
        4.upload successful, right click and "copy image location."
        5.Start netcat on port you specified in script.
        paste image location in the search bar and click go.
        6. check back in with netcat for revshell.
