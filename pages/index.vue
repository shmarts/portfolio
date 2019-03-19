<script>
export default {
  name: 'PageIndex',
  data () {
    return {
      clients: [
        {
          name: 'CaptainJet & Jetfly',
          hex: '#8ec9db',
          role: 'Front End Developer'
        },
        {
          name: 'rchyve',
          hex: '#d53030',
          role: 'Founder & Lead Software Engineer'
        },
        {
          name: 'Stunlock Studios',
          hex: '#e76d2e',
          role: 'Front End Developer'
        },
        {
          name: 'Dojo Madness',
          hex: '#7c49fb',
          role: 'Full Stack Developer'
        },
        {
          name: 'Noka',
          hex: '#30f6a9',
          role: 'Full Stack Developer'
        },
        {
          name: 'GRDigital',
          hex: '#7e7e7e',
          role: 'Full Stack Developer'
        }
      ]
    }
  }
}
</script>

<template>
  <main class="index">
    <section class="about">
      <p class="about__text">
        Martin — <span style="color: #d53030">Full stack engineer</span> based in London,
        specialising in developing web apps using modern technologies.
      </p>
      <p class="about__text">
        Founder of <span style="color: #d53030">rchyve</span>, a platform allowing fashion
        enthusiasts to browse and document archival menswear.
      </p>
    </section>
    <section class="clients">
      <h2 class="clients__title">Featured clients & projects</h2>
      <ul class="client-list">
        <li class="client-list__client" v-for="client in clients" :key="client.name">
          <span class="client__text" :style="{ color: client.hex }">{{ client.name }}</span>
          <span class="client__text">{{ client.role }}</span>
        </li>
      </ul>
    </section>
  </main>
</template>

<style lang="scss">
.about__text, .client__text {
  font-size: 64px;
  font-weight: 700;
  line-height: 1.2em;
  letter-spacing: 0.5px;
  @media only screen and (max-width: 1000px) {
    font-size: 48px;
  }
  @media only screen and (max-width: 760px) {
    font-size: 36px;
  }
  @media only screen and (max-width: 500px) {
    font-size: 28px;
  }
  @media only screen and (max-width: 400px) {
    font-size: 24px;
    letter-spacing: auto;
  }
  @media only screen and (max-width: 320px) {
    font-size: 20px;
    line-height: 1.1em;
  }
}

.about__text {
  margin-bottom: 1.2em;
}

.clients {
  margin-top: 100px;
  @media only screen and (max-width: 600px) {
    margin-top: 60px;
  }
  &__title {
    color: rgba(#000, 0.35);
    text-transform: uppercase;
    font-size: 16px;
    font-weight: 700;
    margin-bottom: 20px;
    @media only screen and (max-width: 500px) {
      font-size: 12px;
      margin-bottom: 10px;
    }
  }
}

.client-list {
  &__client {
    margin-bottom: 40px;
    @media only screen and (max-width: 500px) {
      margin-bottom: 24px;
    }
    @media only screen and (max-width: 320px) {
      margin-bottom: 16px;
    }
  }
}

.client__text {
  display: block;
}

</style>
