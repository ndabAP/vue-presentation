<template>
    <div id="app">
        <slide :steps="4">
            <article>
                <section v-if="step === 1" class="bg-purple aligncenter">
                    <span class="background dark"
                          style="background-image:url('/images/slides/rawpixel-558599-unsplash.jpg')"></span>
                    <div class="wrap">
                        <h1 class="text-landing">Modern Web Development with Vue.js</h1>
                        <p class="text-intro">State of the Art. Vue.js Stärken. Ausblick.</p>
                    </div>
                </section>

                <section v-if="step >= 2" class="slide-top">
                    <div class="wrap">
                        <div class="content-center">
                            <h2 class="text-landing">Features</h2>
                            <p><code>ul.flexblock</code> = Flexible blocks<br> with auto-fill and equal height.</p>
                        </div>
                        <hr>
                        <ul class="flexblock">
                            <li>
                                <h3>
                                    User Interfaces
                                </h3>
                                Wartbar, schnell anpassbar, nutzerfreundlich
                            </li>
                            <li>
                                <h2>
                                    .flexblock li 2
                                </h2>
                                Multipurpose: benefits, clients, work...
                            </li>
                            <li>
                                <h2>
                                    .flexblock li 3
                                </h2>
                                Multipurpose: news, metrics, plans...
                            </li>
                        </ul>
                    </div>
                </section>
            </article>
        </slide>
    </div>
</template>

<style lang="scss">
</style>

<script>
import { Slideshow } from 'eagle.js'

export default {
  mixins: [Slideshow],

  data: () => ({
    product: {
      title: 'Jeans',
      description: '5-pocket low-rise jeans in washed stretch denim with a button fly and slim legs. The jeans are made partly from recycled cotton.',
      price: 64,
      type: ''
    }
  })
}
</script>
