<template>
  <div v-if="$themeConfig.authors">
    <span v-for="author in $themeConfig.authors" :key="author.name">
      <div class="d-flex align-items-center">
        <div v-if="author.name === $frontmatter.author">
          <span>{{ author.name }}</span> &nbsp;
          <NavLink
            v-if="author.name === $frontmatter.author"
            :link="author.link"
            class="btn btn-sm btn-outline-dark"
            >{{ author.linktext }}</NavLink
          >
        </div>
      </div>
    </span>
  </div>
</template>
