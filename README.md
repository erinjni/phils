# Phils Website!

> Created by Erin Ni &middot; [Based on Beautiful Jekyll](https://beautifuljekyll.com/)

This is the official website for **The Rice Philharmonics**. 

## Phils Website Repo Guide

- [IMPORTANT](#IMPORTANT)
- [Configuring pages](#config)
- [Adding new pages](#pages)
- [other notes](#other)

# IMPORTANT
As the new Phils Webmaster, you have been bestowed with the honor of managing The Rice Philharmonics Website! If you are not Webmaster starting Fall 2028, disregard the rest of this section and keep reading. If you are currently in the Fall 2028 semester, however, the following information is absolutely critical. Disregard this section and catostrophic things will happen. Please pay attention:

The website is currently being hosted on [IONOS](https://login.ionos.com/identifier#). The login info can be found in the Google Sheet named "Phils Web Account Details". I lowkey hate them because they called me and we had such a great chat and suddenly I was paying for 3 new packages that I did not want and had to call customer support to cancel them again and it took FOREVER. Anyways, our contract will end in 2029. If you're the new webmaster for the Fall 2028 semester, you face a difficult choice. 
- **Choice #1**: Renew the IONOS contract. As of 2025, it costs $85 for 5 years. Maybe worth it, who knows.
- **Choice #2**: Get a Rice website domain to host for free. Email helpdesk@rice.edu for a new custom Rice domain. phils.rice.edu would be nice. Hypothetically this method works according to my friend, so try it out.

Choose wisely, the future is in your hands. I believe in you. Now keep reading.

# config

The [_config.yml](./_config.yml) file is where we set the basic basic stuff for the website. The most important stuff are:
- **navbar-links**: This sets the pages shown on the navigation bar and which markdown (md) files or links they link to.
- **social-network-links**: This configures what social medias we want to include in the footer.
- **colors**: This sets what colors are used for the navbar, footer, pages, and text. 

The [_includes](./_includes/) and [_layouts](./_layouts/) are where you set the basic layouts for the footer, header, navigation, and social media links. The layouts are base layouts for the pages. If you ever decide the layouts look booty cheeks, you can change it up here. Just be careful of the dependencies with other stuff, if you change one thing in like base.html it'll change everything that's using it, so pay attention to that.


# pages
This is copied straight from Beautiful Jekyll:

> To add pages to your site, you can either write a markdown file (`.md`) or you can write an HTML file. It's much easier to write markdown than HTML, so that's the recommended approach ([here's a great tutorial](https://markdowntutorial.com/) if you need to learn markdown in 5 minutes).
> 
> To see an example of a markdown file, click on any file that ends in `.md`, for example [`about.md`](./about.md). On that page you can see some nicely formatted text (there's a word in bold, a link, a few bullet points), and if you click on the pencil icon to edit the file, you'll see the markdown code that generated the pretty text. Very easy! 
> 
> In contrast, look at [`tags.html`](./tags.html). That's how your write HTML - not as pretty. So stick with markdown if you don't know HTML.
> 
> Any markdown or HTML file that you create will be available on your website under `https://<yourusername>.github.io/<pagename>`. For example, if you create a file `about.md` (or `about.html`) then it'll exist at `https://<yourusername>.github.io/about`.

# other

If you have any more questions on how the website works you can look at the [Beautiful Jekyll](https://github.com/daattali/beautiful-jekyll) repo or ask [Claude](https://claude.ai/) (or whatever AI coder is popular these days). 

**Good luck and have fun, Webmaster.**