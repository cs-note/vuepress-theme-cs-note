---
home: true
heroText: CS note
footer: MIT Licensed | Copyright © 2018-present CS note
---

<div class="post" v-for="post in $site.pages">
  <router-link :to="post.path">
    <h2>{{post.frontmatter.title}}</h2>
  </router-link>
</div>
