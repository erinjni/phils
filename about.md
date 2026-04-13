---
layout: page
title: About
subtitle: Who are the Phils?
---

Up until 1994, the a cappella scene at Rice was sparse. Groups like the Night Owls, Brown Quartet, and All-Lovett Accord were formed, but none managed to last. Laura Huff and Emily Jiang decided to change this. Together, they created the group that would one day be known as the Rice Philharmonics.

Since these humble beginnings, the Philharmonics have expanded their influence across campus, in the Houston community, and throughout the nation. The Phils have performed at several competitions, including the International Championship of Collegiate A Cappella. Most recently, they were semi-finalists in the 2022 ICCAs. The Phils have also recorded and released multiple studio albums. Their newest album is currently in the works and will be available to stream on iTunes and Spotify soon. Be on the lookout!

### Our Music

The Phils arrange all of their own music, spanning a variety of genres like pop, R&B, soft rock, and indie. They also hold an arranging workshop to assist members interested in learning how to arrange a cappella music. Recently, the Phils have performed music from…

<div style="columns: 3; column-gap: 20px; margin-top: 10px;">
  <ul>
    <li>Laufey</li>
    <li>Conan Gray</li>
    <li>Hozier</li>
    <li>Lizzie McAlpine</li>
    <li>Ariana Grande</li>
    <li>Fleetwood Mac</li>
    <li>Tori Kelly</li>
    <li>Bruno Mars</li>
    <li>Wasia Project</li>
    <li>Harry Styles</li>
    <li>Taylor Swift</li>
    <li>Benson Boone</li>
    <li>Teddy Swims</li>
    <li>Sammy Rae & The Friends</li>
    <li>Daniel Caesar</li>
    <li>Joji</li>
    <li>Frank Ocean</li>
  </ul>
</div>

### Past Gigs
The Phils perform at various events on Rice University campus and throughout the Houston area. Past performances include Pancakes for Parkinson's, Alzheimer's Buddies, Fondren Library Study Break, Houston Holiday Market, POST, and Camp Kesem. Every year, the Phils offer Singing Valentines, where they personally serenade that special someone. Interested in booking the Phils for your next event? Reach out through the link above or via their socials!

<div class="slideshow" style="position: relative; width: 100%; max-width: 900px; height: 500px; margin: 20px auto; border-radius: 20px; overflow: hidden; box-shadow: 0 10px 40px rgba(0, 0, 0, 0.2);">
  <img src="/assets/img/phils_p4p.jpg" class="slideshow-image active" style="position: absolute; width: 100%; height: 100%; object-fit: cover; opacity: 0; transition: opacity 1s ease-in-out;">
  <img src="/assets/img/phils_val.jpg" class="slideshow-image" style="position: absolute; width: 100%; height: 100%; object-fit: cover; opacity: 0; transition: opacity 1s ease-in-out;">
  <img src="/assets/img/phils_post.jpg" class="slideshow-image" style="position: absolute; width: 100%; height: 100%; object-fit: cover; opacity: 0; transition: opacity 1s ease-in-out;">
  <img src="/assets/img/phils_fondy.jpg" class="slideshow-image" style="position: absolute; width: 100%; height: 100%; object-fit: cover; opacity: 0; transition: opacity 1s ease-in-out;">
  <div class="slideshow-nav" style="position: absolute; bottom: 20px; left: 50%; transform: translateX(-50%); display: flex; gap: 10px; z-index: 10;">
    <div class="slideshow-dot active" data-index="0" style="width: 12px; height: 12px; border-radius: 50%; background: rgba(255,255,255,0.5); cursor: pointer;"></div>
    <div class="slideshow-dot" data-index="1" style="width: 12px; height: 12px; border-radius: 50%; background: rgba(255,255,255,0.5); cursor: pointer;"></div>
    <div class="slideshow-dot" data-index="2" style="width: 12px; height: 12px; border-radius: 50%; background: rgba(255,255,255,0.5); cursor: pointer;"></div>
    <div class="slideshow-dot" data-index="3" style="width: 12px; height: 12px; border-radius: 50%; background: rgba(255,255,255,0.5); cursor: pointer;"></div>
  </div>
</div>

<style>
  .slideshow-image.active { opacity: 1 !important; }
  .slideshow-dot.active { background: white !important; }
</style>

<script>
  const aboutSlideshow = document.querySelector('.slideshow');
  const aboutImages = aboutSlideshow.querySelectorAll('.slideshow-image');
  const aboutDots = aboutSlideshow.querySelectorAll('.slideshow-dot');
  let aboutIndex = 0;
  let aboutInterval;

  function showAboutSlide(index) {
    aboutImages.forEach(img => img.classList.remove('active'));
    aboutDots.forEach(dot => dot.classList.remove('active'));
    aboutImages[index].classList.add('active');
    aboutDots[index].classList.add('active');
  }

  function nextAboutSlide() {
    aboutIndex = (aboutIndex + 1) % aboutImages.length;
    showAboutSlide(aboutIndex);
  }

  aboutInterval = setInterval(nextAboutSlide, 4000);

  aboutDots.forEach(dot => {
    dot.addEventListener('click', () => {
      clearInterval(aboutInterval);
      aboutIndex = parseInt(dot.dataset.index);
      showAboutSlide(aboutIndex);
      aboutInterval = setInterval(nextAboutSlide, 4000);
    });
  });
</script>

### Upcoming Performances

The Phils pherform for the Rice community at concerts throughout the year. You can see them at…
- Fall concert: Phils are traditionally joined onstage by alumni during Africa
- Holiday concert: Wearing an ugly holiday sweater is encouraged but not required
- Acapellooza: All of Rice’s a cappella groups have individual showcases, followed by a group song
- All request: Audience members decide the Phils’ set list, which includes senior solos (bring those tissues)
