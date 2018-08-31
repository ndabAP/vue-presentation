<template>
  <div id="app">
    <slide :steps="20">
      <article>
        <section v-if="step === 1" class="bg-purple aligncenter">
                    <span class="background dark"
                          style="background-image:url('images/slides/intro.jpg')"></span>
          <div class="wrap">
            <h1 class="text-landing">Modern Web Development with Vue.js</h1>
            <p class="text-intro">State of the Art. Vue.js Stärken. Ausblick.</p>
          </div>
        </section>

        <section v-if="step === 2">
          <div class="wrap">
            <div class="card-50">
              <figure style="padding: 4.8rem"><img src="images/logos/vue.png" width="450"></figure>
              <blockquote>
                <p>&#187;Vue is a progressive framework for building user interfaces. Unlike other
                  monolithic frameworks, Vue is designed from the ground up to be incrementally
                  adoptable.&#171;</p>
                <p><cite>Vue.js website</cite></p>
              </blockquote>
            </div>
          </div>
        </section>

        <section v-if="step >= 3 && step < 5" class="fullscreen">
          <div class="wrap">
            <h2>Anwender</h2>
            <p class="text-intro">Staatliche, Non-Profit und kommerzielle Firmen setzen auf Vue.js.</p>
            <ul class="flexblock blink border">
              <li class="bg-green">
                <a href="">
                  <div>
                    <h3>Alibaba</h3>
                    <ol>
                      <li>Revenue: $39 Mrd.</li>
                      <li>Employees: 66.000</li>
                      <li>Use: Native Apps</li>
                    </ol>
                  </div>
                </a>
              </li>
              <li class="bg-purple">
                <a href="">
                  <div>
                    <h3>Adobe</h3>
                    <ol>
                      <li>Revenue: $7 Mrd.</li>
                      <li>Employees: 15.000</li>
                      <li>Use: Adobe Behance</li>
                    </ol>
                  </div>
                </a>
              </li>
              <li class="bg-red">
                <a href="">
                  <div>
                    <h3>GitLab</h3>
                    <ol>
                      <li>Revenue: $6 Mill.</li>
                      <li>Employees: 325</li>
                      <li>Use: User Interface</li>
                    </ol>
                  </div>
                </a>
              </li>
              <li class="bg-trans-dark">
                <a href="">
                  <div>
                    <h3>NASA</h3>
                    <ol>
                      <li>Haushaltsvol.: $18 Mrd.</li>
                      <li>Employees: 17.000</li>
                      <li>Use: Wissenschaf. Seite</li>
                    </ol>
                  </div>
                </a>
              </li>

              <li v-if="step === 4" class="bg-secondary">
                <a href="">
                  <div>
                    <h3>Facebook</h3>
                    <ol>
                      <li>Revenue: $40 Mrd.</li>
                      <li>Employees: 27.000</li>
                      <li>Use: Newsfeeds</li>
                    </ol>
                  </div>
                </a>
              </li>
              <li v-if="step === 4" class="bg-trans-light">
                <a href="">
                  <div>
                    <h3>Netflix</h3>
                    <ol>
                      <li>Revenue: $11 Mrd.</li>
                      <li>Employees: 5.000</li>
                      <li>Use: Cloud-Verwaltung</li>
                    </ol>
                  </div>
                </a>
              </li>
              <li v-if="step === 4" class="bg-primary">
                <a href="">
                  <div>
                    <h3>Wizz Air</h3>
                    <ol>
                      <li>Revenue: $1 Mrd.</li>
                      <li>Employees: 2.000</li>
                      <li>Use: User Interface</li>
                    </ol>
                  </div>
                </a>
              </li>
              <li v-if="step === 4" class="bg-black">
                <a href="">
                  <div>
                    <h3>Codeship</h3>
                    <ol>
                      <li>Umsatz.: $3 Mill.</li>
                      <li>Employees: 27</li>
                      <li>Use: Absturzfreie Apps</li>
                    </ol>
                  </div>
                </a>
              </li>
            </ul>
          </div>
        </section>

        <section v-if="step === 5">
          <div class="wrap aligncenter">
            <p class="text-subtitle">Firmen berichten über Vue.js</p>
            <h2>Case Studies</h2>
          </div>
        </section>

        <section v-if="step === 6" class="fullscreen bg-white">
          <div class="card-50">
            <figure>
              <span
                      class="background anim dark"
                      style="background: url('images/slides/behance.png') 50% 5%;">
              </span>
            </figure>
            <div class="flex-content">
              <h2>Adobe Behance</h2>
              <p class="text-intro">Kreative Arbeiten, Präsentieren und Entdecken</p>

              <ul class="description">
                <li><span class="s-b">Challenges</span>
                  <ul>
                    <li style="padding: 0">Wiederverwendbare Komponenten schaffen</li>
                    <li style="padding: 0">Komponenten über die gesamte Applikation verwenden</li>
                    <li style="padding: 0">Hohe Nutzerfreundlichkeit und Perfomanz gewährleisten</li>
                  </ul>
                <li><span class="s-b">Solutions</span>
                  <ul>
                    <li style="padding: 0">Vue.js-Schulungen der Teams</li>
                    <li style="padding: 0">Wechsel zu Vue.js</li>
                    <li style="padding: 0">Die vorhanden Codebase migrieren</li>
                  </ul>
                </li>
                <li><span class="s-b">Results</span>
                  <ul>
                    <li style="padding: 0">Einfache Integration des alten Cods</li>
                    <li style="padding: 0">Schnelles Einfügen neuer Features</li>
                    <li style="padding: 0">Kostengünstige und hochperfomante Apps</li>
                  </ul>
                </li>
              </ul>
            </div>
          </div>
        </section>

        <section v-if="step === 7">
          <div class="wrap">
            <div class="content-center">
              <blockquote>
                <p>&#187;Jedes Mal, wenn ich irgendwelche Probleme hatte, war es normalerweise, weil ich es zerdacht habe und
                  ich war angenehm überrascht, als es wirklich so einfach zu implementieren war.&#171;</p>
                <p><cite><a href="">Erin Depew</a> Software Engineer at Behance</cite></p>
              </blockquote>
            </div>
          </div>
        </section>

        <section v-if="step === 8" class="fullscreen bg-white">
          <div class="card-50">
            <figure>
              <span
                      class="background anim dark"
                      style="background: url('images/slides/clemengerbbdo.png') 50% 0%;">
              </span>
            </figure>
            <div class="flex-content">
              <h2>Clemenger BBDO</h2>
              <p class="text-intro">Full Service-Agentur</p>

              <ul class="description">
                <li><span class="s-b">Challenges</span>
                  <ul>
                    <li style="padding: 0">Projekte mit kurzen Zeitspannen</li>
                    <li style="padding: 0">Arbeiten mit vielen Animationen und Übergängen</li>
                    <li style="padding: 0">Schnelles Laden auf mobilen Geräten</li>
                  </ul>
                <li><span class="s-b">Solutions</span>
                  <ul>
                    <li style="padding: 0">Vue.js Pre-Rendering-Technologien</li>
                    <li style="padding: 0">Allgemeine Module statt framework-spezifische</li>
                    <li style="padding: 0">Hohe Flexibilität mit Vue.js Transitions</li>
                  </ul>
                </li>
                <li><span class="s-b">Results</span>
                  <ul>
                    <li style="padding: 0">Strikte Deadlines können nun einfacher eingehalten werden</li>
                    <li style="padding: 0">Händeln von hohem Traffic</li>
                    <li style="padding: 0">Schnelles Onboarding und Projekt-Setup</li>
                  </ul>
                </li>
              </ul>
            </div>
          </div>
        </section>

        <section v-if="step === 9">
          <div class="wrap">
            <div class="content-center">
              <blockquote>
                <p>&#187;Vue.js ermöglicht ein komfortables Entwicklen in unserem Team. Es ist so nah an nativem JavaScript, dass
                  es extrem einfach ist damit zu starten und zu arbeiten.&#171;</p>
                <p><cite><a href="">Sylvain Simao</a> Technical Lead at Clemenger BBDO Melbourne</cite></p>
              </blockquote>
            </div>
          </div>
        </section>

        <section v-if="step === 10" class="fullscreen bg-white">
          <div class="card-50">
            <figure>
              <span
                      class="background anim dark"
                      style="background: url('images/slides/codeship.png') 50% 0%;">
              </span>
            </figure>
            <div class="flex-content">
              <h2>Codeship</h2>
              <p class="text-intro">Continuous Integration Platform</p>

              <ul class="description">
                <li><span class="s-b">Challenges</span>
                  <ul>
                    <li style="padding: 0">Apps blieben stehen oder stürtzen ab</li>
                    <li style="padding: 0">Ambitionierte Pläne für neue Features und komplexe Apps</li>
                    <li style="padding: 0">Unit Tests unter Angular gestalteten sich schwierig</li>
                  </ul>
                <li><span class="s-b">Solutions</span>
                  <ul>
                    <li style="padding: 0">Proof of concept von Vue.js</li>
                    <li style="padding: 0">Weg von ausschließlichen Akzeptanztests</li>
                    <li style="padding: 0">Refactoring der Seiten</li>
                  </ul>
                </li>
                <li><span class="s-b">Results</span>
                  <ul>
                    <li style="padding: 0">Keine Seitenabstürze mehr</li>
                    <li style="padding: 0">Verlässlicher, resistenter, leicht zu wartender Code</li>
                    <li style="padding: 0">Positives Kundenfeedback wegen der neuen UX</li>
                  </ul>
                </li>
              </ul>
            </div>
          </div>
        </section>

        <section v-if="step === 11">
          <div class="wrap">
            <div class="content-center">
              <blockquote>
                <p>&#187;Vue.js bietet ein solides Fundament das beliebig erweitert werden kann und es ist nicht einschränkend
                  bei Tools, mit denen wir außerdem unsere Ziele verfolgen.&#171;</p>
                <p><cite><a href="">Roman Kuba</a> Lead Frontend Developer at Codeship</cite></p>
              </blockquote>
            </div>
          </div>
        </section>
      </article>
    </slide>
  </div>
</template>

<style lang="scss">
  html {
    font-size: 100%;
    hyphens: auto;
  }

  .s-b {
    font-weight: 400;
  }

  .v-c {
    position: relative;
    top: 50%;
    -webkit-transform: translateY(-50%);
    -ms-transform: translateY(-50%);
    transform: translateY(-50%);
  }

  .gray {
    -webkit-filter: grayscale(100%); /* Safari 6.0 - 9.0 */
    filter: grayscale(100%);
  }

  .background.anim {
    animation: anim 150s linear infinite;
    background-size: auto;
  }

  .description > li {
    border: none;
  }
</style>

<script>
import { Slideshow } from 'eagle.js'

Slideshow.methods.handleResize = () => null

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

  // mounted () {
  //   setInterval(() => {
  //     const images = document.getElementsByClassName('anim')
  //
  //     if (images.length > 0) {
  //       for (let image of images) {
  //         setInterval(() => {
  //           let x = Math.random() * 100
  //           let y = Math.random() * 100
  //           let distance = Math.sqrt(Math.pow(x - x, 2) + Math.pow(y - y, 2))
  //           let time = 10000 * (distance / 100)
  //           image.setAttribute('style', `background-position: `)
  //         })
  //       }
  //     }
  //   }, 1000)
  // }
}
</script>
