---
layout: post
title: Building Websites Behind the Great Firewall
date: 2017-06-06 23:26:19
categories: Support Engineer
tag: Web Development, Support Engineer
---

While we are freely connecting and communicating with the world, the Chinese government place a limitation on what its citizens can access. This restriction never hindered China’s internal development. In fact, the nature of the government control fuel local developers and tinkerers to duplicate and create tools for their digital ecosystem. All the tools that exist in our everyday digital life, China has the exact clone of the tool and often time there is an added to feature to solve specific localize issues. We have Google; China has Baidu. We have Facebook; China has Weibo. It’s a whole different world, where your expertise and skills are tested for adaptability.

After supporting America made, Chinese websites for the past two years, I’ve compiled a list of my research and finding for developers who are building for Chinese clients. Since the government closely monitors tools outside of China, you will almost always run into performance issues if you’re unaware of the content restriction at every step of the build out. Luckily, China has its ecosystem of digital tools for web development. You’ll find a list of alternative tools for creating website inside the Great Firewall.


## Design
A common Chinese website can look like this.

{% img  /img/1688china.png [100%] [1688 China [Sample Chinese Website]] %}

Or this.

{% img  /img/chinadaily.png [100%] [China Daily [Sample Chinese News Website]] %}


My designer senses are tingling. I’m getting design clutterfobic. The cluttered feeling is related to how the Chinese language display on screen and paper. There is no capitalize system, and the spacing between the character are limited. Any font styling such as bold, italic and underline creates less white space and often time the corporate behind the notion of Chinese site being too “busy.” There is also two type of Chinese character set, simplified and non-simplified. You are limited to how the paragraphs of text are going to appear on the site. It doesn’t mean the design can not look clean and crisp. Get ready, to introduce them to white space, clean design and content filled imagery. I recommend collecting an arsenal of beautifully designed sites for your initial design call.

Since we are on the subject of fonts, let’s spend a little bit of time on font management. Unlike the alphabetic languages, the Chinese character system requires many more character text. Naturally, the font faces heavier in file size and much more complicated to display. You’ll notice many fonts hosted on your servers are three times the size of alphabetic language fonts. Keep the font file size in mind; this is part of your site performance budget.

For detail implementation information, I recommend reading Kendra Schaefer’s blog post on Chinese fonts.
http://www.kendraschaefer.com/2012/06/chinese-standard-web-fonts-the-ultimate-guide-to-css-font-family-declarations-for-web-design-in-simplified-chinese/

The ever-so-popular, Google font is inaccessible inside of China without VPN. The vast number of Chinese visitors will not be able to see your beautiful font face. China has two font libraries available for use. I recommend reviewing the available font library before designing the site.
http://en.justfont.com/fonts
https://www.youziku.com/

There has been some success with Typekit. I’ve run into two occasions where the fonts are blocked. Typekit support resolved the issue.

Javascript and jquery libraries
Sorry! Bootstrap, Fontawesome, and jquery libraries are all hosted outside of China. Luckily Chinese internet companies have duplicated these libraries and hosted them on their servers. Check out http://www.bootcdn.cn.

For open source plug-ins, be sure use tools with CDN accelerator and research to make your CDN distributes their services inside of China. Cloudfare services have networks inside China.


## Video and Social Media Services
Inside China, WeChat is the all-in-one application to replace, Facebook, Twitter, Venmo payment system, Uber, etc. China tech market is amazingly quick and adaptable to the changing tech world. They understand mobile apps (It’s pronounced APP. I’m not sure why but the Chinese believe it is an acronym rather than an abbreviation.) are the future. WeChat a phone messaging app so integrating onto your website is currently not possible. They are working on an API. China is building a whole ecosystem around this one app. WeChat support business pages, push notification marketing, payment, car rental and more. You can get almost any services on WeChat. If you want to do business inside China, you better be ready to generate WeChat marketing. For the website, many of the clients will add a QR to redirect users to their WeChat business page.

For embed video services, you’ll likely be using Youku.com. Youku is the youtube equivalent inside of China. Videos hosting on the hosting server is an option, but of course, the server needs to inside China for this to be effective.


## Analytics
Here’s a curve ball. While all Google services are considered banned inside China, Google Analytics is allowed. The government enabled it quietly to allow website tracking. A few of my former clients use Google Analytics in conjunction with Baidu Analytics.

Since we’re tackling the performance issue, you’ll need to be more rigid with the best practices for general site optimization. Review all images and media for web optimization. Minimalist in all areas of the website is the key to success. China’s digital ecosystem is constantly changing and shifting. If anyone notices, any updates, please don’t hesitate to contact me. Good luck! 祝你好运！
