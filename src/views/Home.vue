<template>
  <div>
    <Layout />
    <main>
      <section>
        <article>
          <div class="title"><h2>MARKET PLACE</h2></div>
          <div>
            <div>FORTNITE-PACK</div>
            <div>NEW GAMES</div>
          </div>
          <div>GIFT CARDS</div>
        </article>
        <article>
          <div class="profile">PROFILE</div>
          <div class="score">SCORE</div>
          <div class="medals">MEDALS</div>
        </article>
        <article>
          <h2>BUY TOKENS</h2>
        </article>
        <article>
          <div class="title"><h2>MOST POPULAR GAMES</h2></div>
          <div class="list-popular-games"></div>
        </article>
        <article>
          <h2>MENU SLICE STORE</h2>
        </article>
      </section>
    </main>
  </div>
</template>

<script>
import Layout from "@/components/Layout.vue";

export default {
  name: 'Home',
  components: {
    Layout
  }
}

</script>