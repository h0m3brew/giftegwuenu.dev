<template>
  <div class="author">
    <g-image
      alt="Author image"
      class="author__image"
      src="~/assets/images/author.jpg"
      width="180"
      height="180"
      blur="5"
    />

    <h1 v-if="showTitle" class="author__site-title">{{ $static.metaData.siteName }}</h1>

    <p class="author__intro">
      Hello! 👋
      <br>I’m a Frontend Engineer based in Lagos, Nigeria and I'm passionate about making the web accessible to everyone and building communities.
    </p>

    <p class="author__links">
      <a href="//twitter.com/lauragift_">
        <g-image alt="twitter" class src="~/assets/images/twitter.png"/>
      </a>
      <a href="//dev.to/lauragift21">
        <g-image alt="dev" class src="~/assets/images/dev.jpg" width="30"/>
      </a>
      <a href="//instagram.com/thegiftcode_">
        <g-image alt="instagram" class src="~/assets/images/instagram.png"/>
      </a>
       <a href="/rss.xml">
        <g-image alt="rss" class src="~/assets/images/rss.png" width="30"/>
      </a>
      <a href="//github.com/lauragift21">
        <g-image alt="github" class src="~/assets/images/github.png"/>
      </a>
      <a href="//linkedin.com/in/egwuenugift">
        <g-image alt="linkedin" class src="~/assets/images/linkedin.png" width="32"/>
      </a>
      <a href="//noti.st/lauragift21">
        <g-image alt="notist" class src="~/assets/images/notist.jpg" width="32"/>
      </a>
    </p>
  </div>
</template>

<static-query>
query {
  metaData {
    siteName
  }
}
</static-query>

<script>
export default {
  props: ["showTitle"]
};
</script>

<style lang="scss">
.author {
  margin: 0 auto;
  max-width: 500px;
  text-align: center;
  padding: calc(var(--space) / 2) 0;

  &__image {
    border-radius: 100%;
    width: 90px;
    height: 90px;
    margin-bottom: 1em;
  }

  &__intro {
    opacity: 0.8;
  }

  &__site-title {
    font-size: 1.5em;
  }

  &__links {
    margin-top: -0.5em;
    a {
      margin: 0 0.5em;
    }
  }
}
</style>
