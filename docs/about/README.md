---
pageClass: about-page
description: 'The biography and information about me.'
avatar: /profile.jpg
head: 'Boyang Shi'
info: 'Recent graduate from University of Bishops'
interests: 'Current Interests: TextToSpeech;Stabel Diffusion.'
socials:
- title: github
  link: https://github.com/solishi
- title: linkedin
  link: https://www.linkedin.com/in/byshi/
- title: email
  link: 'mailto:solisshi[at]gmail.com'
actions:
- text: Projects
  link: /projects/
- text: Blog
  link: https://github.com/mtobeiyf
footer: Made with ♥ by Fing. Powered by VuePress
---

<AboutCard :frontmatter="$page.frontmatter" >

I attended [University of Bishops](https://https://www.ubishops.ca/) to study Data Science :dizzy:

</AboutCard>

<style lang="stylus">

.theme-container.about-page .page
  background-color #e6ecf0
  min-height calc(100vh)

  .last-updated
    display none

</style>
