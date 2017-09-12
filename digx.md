From the webpage, it seems that we'll be using dig to look for information.

Looking at available options for dig, I saw that one option, -x, fits with the site name. dig -x is a reverse lookup based on ip. So first, I used dig to obtain the ip of digx.asisctf.com.

`dig digx.asisctf.com`

    ;; ANSWER SECTION:
    digx.asisctf.com.       300     IN      A       192.81.223.250


Then I did a reverse lookup on that ip

`dig -x 192.81.223.250`

    ;; ANSWER SECTION:
    250.223.81.192.in-addr.arpa. 1800 IN    PTR     airplane.asisctf.com.


It looks like there is another domain under that ip...

On visiting the new site it tells me to put my device into airplane mode, shutting off my Wi-fi worked and the flag was displayed.

`ASIS{_just_Go_Offline_When_you_want_to_be_creative_!}`
