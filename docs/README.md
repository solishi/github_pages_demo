---
pageClass: home-page
# some data for the components

name: Boyang Shi
#profile: /profile.jpg

socials:
  - title: github
    icon: "/icons/github.svg"
    link: https://github.com/solishi
  - title: linkedin
    icon: "/icons/linkedin-mono.svg"
    link: https://www.linkedin.com/in/byshi/

cv: https://drive.google.com/file/d/16FpWlsX0YUVSw8Cqx-uj8mSPjW39sx2o/view?usp=sharing
bio: Recent graduate from University of Bishops
email: solisshi (at) gmail (dot) com
---

<ProfileSection :frontmatter="$page.frontmatter" />

## About Me

I get my bachelor degree in Computer Engineering in [University of Michigan](https://http://www.umich.edu/)

My research area includes Web develop and deep learning. :dizzy:


## News

- [Sep 2013] Attend University of Michigan
- [Nov 2019] Work at Taihuiren Company
- [Sep 2020] Attend University of Bishops

## Education & Experiences

- **University of Michigan** <br/>
Sep 2013 - 2019 Bachlor Degree in Computer Engineering
- **Taihuiren Company** <br/>
Sep 2013 - 2019 Software Engineer
- **University of Bishops** <br/>
Sep 2013 - 2019 Master Degree in Data Science


## Projects


[→ Full list](/projects/)

<ProjectCard  hideBorder=true>

  **IOT canteen**

  :house:Taihuiren Company

  *Face-recognition,Signal transmission,Tomcat,Mysql, Django,E-chart*

- [Vue.js](https://github.com/solishi/yunlin)

Learned about and implemented facial recognition, signal transmission, Tomcat, MySQL, Django, and ECharts. Collected data related to food waste by using electronic scales. Applied Bluetooth to transport local data. Wrote optimized
analysis algorithms for data. Displayed real-time results charts on a 40-inch monitor. Encouraged employees to reduce
their food waste.


</ProjectCard>


<!-- Custom style for this page -->

<style lang="stylus">

.theme-container.home-page .page
  font-size 14px
  font-family "lucida grande", "lucida sans unicode", lucida, "Helvetica Neue", Helvetica, Arial, sans-serif;
  p
    margin 0 0 0.5rem
  p, ul, ol
    line-height normal
  a
    font-weight normal
  .theme-default-content:not(.custom) > h2
    margin-bottom 0.5rem
  .theme-default-content:not(.custom) > h2:first-child + p
    margin-top 0.5rem
  .theme-default-content:not(.custom) > h3
    padding-top 4rem

  /* Override */
  .md-card
    margin-top 0.5em
    .card-image
      padding 0.2rem
      img
        max-width 120px
        max-height 120px
    .card-content p
      -webkit-margin-after 0.2em

@media (max-width: 419px)
  .theme-container.home-page .page
    p, ul, ol
      line-height 1.5

    .md-card
      .card-image
        img
          width 100%
          max-width 400px

</style>
