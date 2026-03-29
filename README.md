# Phils Website!

> Created by Erin Ni &middot; [Based on Beautiful Jekyll 6.0.1](https://beautifuljekyll.com/)

This is the official website for **The Rice Philharmonics**. 

## Phils Website Repo Guide

- [IMPORTANT](#IMPORTANT)
- [FALL 2028 WARNING] (#fall2028)
- [File Organization](#org)

# IMPORTANT
As the new Phils Webmaster, you have been bestowed with the honor of managing The Rice Philharmonics Website! 

Here are the important things you must do before/during the school year:
- **Before auditions**: Update audition info on ['auditions.md'](./auditions.md) once the dates are finalized. 
- **After auditions**: Update the home page and members page. Here are the steps:
1. Update the members database. Go to ['members.yml'](./members.yml), move the old members to alumni and the new members to the top.
2. Upload all the new pics into the img folder. I put one full group pic (phils 2025 pointing), one normal and one silly picture for each member, and 3 group pics for each class. You can put the old pics in a folder and forget about them forever 🥲 or you can start an archive photo album or anything it's up to you! just be sure to update these instructions so that the next webmaster knows what to do.
3. Assign everyone to write someone else's bio. You can just randomly assign, text them individually, and give them some examples. Try to do this maybe a few weeks after, just so that people can get to know each other before writing.
- **Throughout the year**: Update when we have events going on, concerts, public gigs, etc. I haven't really made an organized events folder or page, maybe you can make it pop up on the home page of the site or something.

# FALL 2028 WARNING
If you are not Webmaster starting Fall 2028, disregard this section and keep reading. If you are currently in the Fall 2028 semester, however, the following information is absolutely critical. Disregard this section and catastroPHic things will happen. Please pay attention:

The website is currently being hosted on [IONOS](https://login.ionos.com/identifier#). The login info can be found in the Google Sheet named "Phils Web Account Details". I lowkey hate them because they called me and we had such a great chat and suddenly I was paying for 3 new packages that I did not want and had to call customer support to cancel them again and it took FOREVER. Anyways, our contract will end in 2029. If you're the new webmaster for the Fall 2028 semester, you face a difficult choice. 
- **Choice #1**: Renew the IONOS contract. As of 2025, it costs $85 for 5 years. Maybe worth it, who knows.
- **Choice #2**: Get a Rice website domain to host for free. Email helpdesk@rice.edu for a new custom Rice domain. phils.rice.edu would be nice. Hypothetically this method works according to my friend, so try it out.
- **Choice #3**: Find somewhere else to host the website. Highly do not recommend after many struggles and scams.

Choose wisely, the future is in your hands.

# File Organization
TBH I don’t know what half the files do, I forked it off a site template. But I know enough to make it work. Feel free to learn more about what each file in the repo does! Here are the bare bones of what you need to know.
* **[`_config.yml`](./_config.yml)**: This is where you configure how the site looks (navbar links, logo, colors, and social media). You don’t really need to change much unless you want to overhaul the aesthetic.
* **[`_includes/`](./_includes/)** and **[`_layouts/`](./_layouts/)**: These folders house the base layouts for the footer, header, and navigation. If you decide the layouts look "booty cheeks," you can change them here—just be careful, as changing base.html affects every page using it.
* **[`index.html`](./index.html)**: The home page. It was originally AI-generated, so feel free to keep using Claude or your own creativity to change it up!
* **[`about.md`](./about.md)**, **[`auditions.md`](./auditions.md)**, **[`media.md`](./media.md)**, **[`members.md`](./members.md)**: These are the core pages of your site. They are written in Markdown for easy editing. The media page is currently a blank canvas—go ham!
* **[`_data/members.yml`](./_data/members.yml)**: The database for current members and alumni. It’s self-explanatory: current members at the top, alumni at the bottom. This is where you’ll manage pictures and bios.
* **[`assets/img/`](./assets/img/)**: The storage folder for all images. You can archive old photos in subfolders annually to keep things tidy for the next webmaster.
* **[`404.html`](./404.html)**: The error page for broken links. It currently features a YouTube video from last year; try to swap this out occasionally to keep it fresh.
* **[`favicon.ico`](./favicon.ico)**: This is the tiny icon displayed on the browser tab. Update this if the logo changes.



**Good luck and have fun, Webmaster.**