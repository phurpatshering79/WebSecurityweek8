# Project 7 - WordPress Pentesting

Time spent: **9** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report
1. (Required) WordPress  4.0-4.7.2 - Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
  - [x] Summary: This vulnerablity allows remote attackers to inject arbitrary web script or HTML via video URL in YouTube emebeds.
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.7.3
  - [x] GIF Walkthrough:

<img src='https://github.com/phurpatshering79/WebSecurityweek8/blob/master/Pvideo.gif' title='youtube video' alt='Youtube Video' />

  - [x] Steps to recreate: Create a new page and place the following code in the body:

    ```
    [embed src='https://youtube.com/embed/xxxx\x3csvg onload=alert(1)\x3e'][/embed]
    ```

    When the page is viewed, the injected code is executed.
    
    2. (Required) WordPress <= 4.3 - Authenticated Shortcode Tags Cross-Site Scripting (XSS)
- [x] Summary: A stored/persistent, Cross-Site script XSS vulnerablilty which allows remote attackers to inject arbitrary web script/HTML by abusing the way unclosed HTML elements
during the processing of shortcode tags are mishandled.
- Vulnerability types: XSS
- Tested in version: 4.2
- Fixed in version: 4.3
- [x] GIF Walkthrough:

<img src='https://github.com/phurpatshering79/WebSecurityweek8/blob/master/Ppost.gif' title='gif 1' alt='gif 1' />

- [x] Steps to recreate: Create a new post and place the following code in the body:

```
<a href="" "onclick=alert(1)">check</a>
```

When a user clicks in the post, the injected code is executed.

3. (Required)WordPress => 4.2 - User Authentication
- [x] Summary:
- Vulnerability types: user authentication,
- Tested in version: 4.2
- [x] GIF Walkthrough: 

<img src='https://github.com/phurpatshering79/WebSecurityweek8/blob/master/PSignIn.gif' title='imageGif' alt='imageGif' />


- [x] Steps to recreate:
Enter "admin" as username and type random password.
Enter "different name" as username and type "admin" as password.
# Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

Copyright [2019] [Phurpa Sherpa]

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

