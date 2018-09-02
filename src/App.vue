<template>
  <div id="app">
    <slide :steps="35">
      <article>
        <section v-if="step === 1" class="bg-purple aligncenter">
                    <span class="background dark"
                          style="background-image:url('images/slides/intro.jpg')"></span>
          <div class="wrap slow">
            <h1 class="text-landing">Modern Web Development with Vue.js</h1>
            <p class="text-intro">State of the Art. Vue.js Stärken. Konkurrenz. Ausblick.</p>
          </div>
        </section>

        <section v-if="step === 2">
          <div class="wrap">
            <div class="content-center">
              <blockquote>
                <p>&#187;Vue ist ein fortschrittliches Framework für den Aufbau von Benutzeroberflächen. Im Gegensatz zu
                  anderen monolithischen Frameworks ist Vue von Grund auf so konzipiert, dass es inkrementell einsetzbar
                  ist.&#171;<sup>1</sup></p>
                <p><cite><a href="#">Vue.js</a> website</cite></p>
              </blockquote>
            </div>
          </div>
        </section>

        <section class="bg-blue fullscreen" v-if="step === 3">
          <div class="wrap">
            <h2>Quick Facts<sup>2</sup></h2>
            <p class="text-intro">Vue.js in der wilden Landschaft.</p>
            <ul class="flexblock metrics">
              <li>
                <span>112.000</span>
                Github Stars
              </li>
              <li>
                <span>30</span>
                Core Developers
              </li>
              <li>
                <span>2 Mil.</span>
                Monthly Downloads
              </li>
              <li>
                <span>#3</span>
                Github popularity
              </li>
              <li>
                <span>30</span>
                Sponsors
              </li>
              <li>
                <span>12.000</span>
                Related projects
              </li>
            </ul>
          </div>
        </section>

        <section v-if="step === 4">
          <div class="wrap">
            <div class="content-center">
              <blockquote>
                <p>&#187;In den letzten zwei Jahren ist Vue.js schneller gewachsen als alle anderen gängigen
                  JavaScript-Frameworks.&#171;<sup>2</sup></p>
                <p><cite><a href="#">Github</a> trends</cite></p>
              </blockquote>
            </div>
          </div>
        </section>

        <section v-if="step === 5">
          <div class="wrap aligncenter">
            <p class="text-subtitle">Viele börsennotierte Firmen setzen auf Vue.js</p>
            <h2>Important User</h2>
          </div>
        </section>

        <section v-if="step >= 6 && step < 8" class="fullscreen bg-trans-dark">
          <div class="wrap">
            <h2>Anwender</h2>
            <p class="text-intro">Staatliche, Non-Profit und kommerzielle Firmen setzen auf Vue.js.</p>
            <ul class="flexblock">
              <li>
                <div>
                  <h3>Alibaba<sup>3</sup></h3>
                  <ol>
                    <li>Revenue: $39 Mrd.</li>
                    <li>Employees: 66.000</li>
                    <li>Use: Native Apps</li>
                  </ol>
                </div>
              </li>
              <li>
                <div>
                  <h3>Adobe<sup>3</sup></h3>
                  <ol>
                    <li>Revenue: $7 Mrd.</li>
                    <li>Employees: 15.000</li>
                    <li>Use: Adobe Behance</li>
                  </ol>
                </div>
              </li>
              <li>
                <div>
                  <h3>GitLab<sup>3</sup></h3>
                  <ol>
                    <li>Revenue: $6 Mill.</li>
                    <li>Employees: 325</li>
                    <li>Use: User Interface</li>
                  </ol>
                </div>
              </li>
              <li>
                <div>
                  <h3>NASA<sup>4</sup></h3>
                  <ol>
                    <li>Vol.: $18 Mrd.</li>
                    <li>Employees: 17.000</li>
                    <li>Use: Wissenschaf. Seite</li>
                  </ol>
                </div>
              </li>

              <li v-if="step === 7" class="slideInUp">
                <div>
                  <h3>Facebook<sup>3</sup></h3>
                  <ol>
                    <li>Revenue: $40 Mrd.</li>
                    <li>Employees: 27.000</li>
                    <li>Use: Newsfeeds</li>
                  </ol>
                </div>
              </li>
              <li v-if="step === 7" class="slideInUp">
                <div>
                  <h3>Netflix<sup>3</sup></h3>
                  <ol>
                    <li>Revenue: $11 Mrd.</li>
                    <li>Employees: 5.000</li>
                    <li>Use: Cloud-Verwaltung</li>
                  </ol>
                </div>
              </li>
              <li v-if="step === 7" class="slideInUp">
                <div>
                  <h3>Wizz Air<sup>3</sup></h3>
                  <ol>
                    <li>Revenue: $1 Mrd.</li>
                    <li>Employees: 2.000</li>
                    <li>Use: User Interface</li>
                  </ol>
                </div>
              </li>
              <li v-if="step === 7" class="slideInUp">
                <div>
                  <h3>Codeship<sup>3</sup></h3>
                  <ol>
                    <li>Revenue: $3 Mill.</li>
                    <li>Employees: 27</li>
                    <li>Use: Absturzfreie Apps</li>
                  </ol>
                </div>
              </li>
            </ul>
          </div>
        </section>

        <section v-if="step === 8">
          <div class="wrap aligncenter">
            <p class="text-subtitle">Firmen berichten über Vue.js</p>
            <h2>Case Studies<sup>5</sup></h2>
          </div>
        </section>

        <section v-if="step === 9" class="fullscreen bg-white">
          <div class="card-50">
            <figure>
              <span
                      class="background anim"
                      style="background: url('images/slides/behance.png') 50% 5%; opacity: 0.5">
              </span>
            </figure>
            <div class="flex-content">
              <h2>Adobe Behance</h2>
              <p class="text-intro">Portfolios der kreativsten Köpfe</p>

              <ul class="description">
                <li><span class="s-b">Challenges</span>
                  <ul>
                    <li style="padding: 0">Wiederverwendbare Komponenten schaffen</li>
                    <li style="padding: 0">Komponenten über die gesamte Applikation verwenden</li>
                    <li style="padding: 0">Hohe Nutzerfreundlichkeit und Perfomanz gewährleisten
                    </li>
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
                    <li style="padding: 0">Einfache Integration des alten Codes</li>
                    <li style="padding: 0">Schnelles Einfügen neuer Features</li>
                    <li style="padding: 0">Kostengünstige und hochperfomante Apps</li>
                  </ul>
                </li>
              </ul>
            </div>
          </div>
        </section>

        <section v-if="step === 10">
          <div class="wrap">
            <div class="content-center">
              <blockquote>
                <p>&#187;Jedes Mal, wenn ich irgendwelche Probleme hatte, war es normalerweise, weil ich zu komplex
                  dachte und ich war angenehm überrascht, als es wirklich so einfach zu implementieren war.&#171;</p>
                <p><cite><a href="#">Erin Depew</a> Software Engineer at Behance</cite></p>
              </blockquote>
            </div>
          </div>
        </section>

        <section v-if="step === 11" class="fullscreen bg-white">
          <div class="card-50">
            <figure>
              <span
                      class="background anim"
                      style="background: url('images/slides/clemengerbbdo.png') 50% 0%; opacity: 0.5">
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
                    <li style="padding: 0">Strikte Deadlines können nun einfacher eingehalten
                      werden
                    </li>
                    <li style="padding: 0">Händeln von hohem Traffic</li>
                    <li style="padding: 0">Schnelles Onboarding und Projekt-Setup</li>
                  </ul>
                </li>
              </ul>
            </div>
          </div>
        </section>

        <section v-if="step === 12">
          <div class="wrap">
            <div class="content-center">
              <blockquote>
                <p>&#187;Vue.js ermöglicht ein komfortables Entwicklen in unserem Team. Es ist so nah an
                  nativem JavaScript, dass es extrem einfach ist damit zu starten und zu arbeiten.&#171;</p>
                <p><cite><a href="#">Sylvain Simao</a> Technical Lead at Clemenger BBDO Melbourne</cite>
                </p>
              </blockquote>
            </div>
          </div>
        </section>

        <section v-if="step === 13" class="fullscreen bg-white">
          <div class="card-50">
            <figure>
              <span
                      class="background anim"
                      style="background: url('images/slides/codeship.png') 50% 0%; opacity: 0.5">
              </span>
            </figure>
            <div class="flex-content">
              <h2>Codeship</h2>
              <p class="text-intro">Continuous Integration Platform</p>

              <ul class="description">
                <li><span class="s-b">Challenges</span>
                  <ul>
                    <li style="padding: 0">Apps blieben stehen oder stürtzen ab</li>
                    <li style="padding: 0">Ambitionierte Pläne für neue Features und komplexe Apps
                    </li>
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

        <section v-if="step === 14">
          <div class="wrap">
            <div class="content-center">
              <blockquote>
                <p>&#187;Vue.js bietet ein solides Fundament, das beliebig erweitert werden kann und es
                  ist nicht einschränkend bei Tools, mit denen wir außerdem arbeiten.&#171;</p>
                <p><cite><a href="#">Roman Kuba</a> Lead Frontend Developer at Codeship</cite></p>
              </blockquote>
            </div>
          </div>
        </section>

        <section v-if="step === 15">
          <div class="wrap aligncenter">
            <p class="text-subtitle">Entwickler berichten über Vue.js</p>
            <h2>In-Sight Developers</h2>
          </div>
        </section>

        <section v-if="step >= 16 && step < 18" class="fullscreen bg-secondary">
          <div class="wrap">
            <h2>Umfrage<sup>5</sup></h2>
            <p class="text-intro">Entwickler aus 88 Ländern wurden befragt.</p>
            <ul class="flexblock metrics">
              <li>
                <span>96 %</span> würden Vue.js in einem anderen Projekt erneut verwenden
              </li>
              <li>
                <span>94 %</span> nutzten beim Entwickeln die offzielle Hilfe von Vue.js
              </li>
              <li>
                <span>81 %</span> empfanden es als einfach, Vue.js in ihr System zu integrieren
              </li>
              <li v-if="step === 17" class="slideInUp">
                <span>75 %</span> nahmen Vue.js in in den letzten 12 Monaten in ihrem Tech-Stack auf
              </li>
              <li v-if="step === 17" class="slideInUp">
                <span>15 %</span> glauben, dass Apps mit Vue.js schlecht skalierbar sind
              </li>
              <li v-if="step === 17" class="slideInUp">
                <span>54 %</span> glauben, dass Vue.js noch populärer in ihrer Organisation wird
              </li>
            </ul>
          </div>
        </section>

        <section v-if="step === 18">
          <div class="wrap aligncenter">
            <p class="text-subtitle">Was kann das Framework</p>
            <h2>Vue.js in Action</h2>
          </div>
        </section>

        <section v-if="step === 19">
          <header class="bg-white">
            <div class="wrap">
              <div style="text-align: right">
                <div style="display: inline-block">
                  Quantity: <input
                        style="max-width: 50%; border: none; padding: 0; font-weight: 300"
                        v-model="product.amount">
                </div>
                <div style="display: inline-block">
                  Total: ${{total}}
                </div>
              </div>
            </div>
          </header>

          <div class="wrap">
            <div class="grid vertical-align">
              <div class="column">
                <form action="/" method="post">
                  <fieldset>
                    <input style="margin-bottom: 0.83em" v-model="product.title">
                    <input style="margin-bottom: 0.83em" v-model="product.description">
                    <input style="margin-bottom: 0.83em" v-model="product.price">
                  </fieldset>
                </form>
              </div>
              <div class="column">
                <h2>{{product.title}}</h2>
                <p class="text-intro">{{product.description}}</p>
                <p>
                  All our products are self-made and made with love. You won't find better products.
                  Buy this product and you will be happy. We will be!
                </p>
                <p><span class="s-b">Price</span>: ${{product.price}}</p>
              </div>
            </div>
          </div>
        </section>

        <section v-if="step === 20" class="aligncenter">
          <div class="wrap">
            <button
                    :disabled="Object.keys(removedTodo).length === 0"
                    class="button ghost"
                    style="border: none; text-transform: none; margin-bottom: 0.83em"
                    @click="undoTodo">Undo
            </button>
            <ul class="flexblock specs">
              <li style="padding-bottom: 0.83em; padding-top: 0">
                <div>
                  <form @submit.prevent="saveTodo">
                    <fieldset style="padding: 0;">
                      <input placeholder="Write a to do ..." v-model="todo">
                    </fieldset>
                  </form>
                </div>
              </li>
              <li
                      v-if="todos.length > 0"
                      style="padding-bottom: 0.83rem; padding-top: 0"
                      @click="removeTodo(todo.identifier)"
                      v-for="todo in todos"
                      :key="todo.identifier">
                {{todo.text}}
              </li>
            </ul>
            <p v-if="todos.length === 0">There are no to dos, yet.</p>
          </div>
        </section>

        <section v-if="step === 21">
          <div class="wrap">
            <h2>Sign-up</h2>
            <p class="text-intro">Please give us your data.</p>
            <form action="/" method="post">
              <p style="margin-bottom: 0; margin-top: 0" v-if="!isValidEMail">E-Mail is not valid</p>
              <input style="margin-bottom: 0.83em;" placeholder="E-Mail" v-model="user.eMail">
              <p style="margin-bottom: 0; margin-top: 0" v-if="!isValidPassword">
                Password must be at least 8 characters and contain one letter
              </p>
              <input style="margin-bottom: 0.83em" placeholder="Password" v-model="user.password">
            </form>
          </div>
        </section>

        <section v-if="step === 22">
          <div class="wrap aligncenter">
            <p class="text-subtitle">Angular, React und Co.</p>
            <h2>Vue.js-Konkurrenz</h2>
          </div>
        </section>

        <section v-if="step === 23">
          <div class="wrap">
            <h2>Grundlegende Funktionen</h2>
            <p class="text-intro">Vue.js vereint das Beste aus Angular und React.</p>

            <table>
              <thead>
              <tr>
                <th></th>
                <th>Vue.js</th>
                <th>Angular</th>
                <th>React</th>
              </tr>
              </thead>
              <tbody>
              <tr>
                <td class="s-b">JSX</td>
                <td>Yes</td>
                <td>No</td>
                <td>Yes</td>
              </tr>
              <tr>
                <td class="s-b">TypeScript</td>
                <td>Yes</td>
                <td>Yes</td>
                <td>No</td>
              </tr>
              <tr>
                <td class="s-b">Object-orientated</td>
                <td>Yes</td>
                <td>Yes</td>
                <td>No</td>
              </tr>
              <tr>
                <td class="s-b">Functional</td>
                <td>Yes</td>
                <td>No</td>
                <td>Yes</td>
              </tr>
              <tr>
                <td class="s-b">HTML</td>
                <td>Yes</td>
                <td>Yes</td>
                <td>No</td>
              </tr>
              <tr>
                <td class="s-b">Component CSS</td>
                <td>Yes</td>
                <td>Yes</td>
                <td>No</td>
              </tr>
              </tbody>
            </table>
          </div>
        </section>

        <section v-if="step === 24" class="aligncenter">
          <div class="wrap">
            <h2>Mögliche Lernkurven<sup>6</sup></h2>
            <p class="text-intro">Viele Nutzer berichten von einer ähnlichen Lernkurve.</p>
            <learning-curve/>
          </div>
        </section>

        <section v-if="step === 25" class="aligncenter">
          <div class="wrap">
            <h2>Memory usage<sup>7</sup></h2>
            <p class="text-intro">Vue.js verbraucht weniger, jedoch sind die Unterschiede maginal.</p>
            <performance-comparison/>
          </div>
        </section>

        <section v-if="step === 26">
          <div class="wrap aligncenter">
            <p class="text-subtitle">Fragen wir Alice und Bob</p>
            <h2>Immer noch Zweifel?</h2>
          </div>
        </section>

        <section v-if="step === 27" class="bg-primary">
          <div class="wrap">
            <div class="content-left">
              <h2>Alice</h2>
              <p style="margin-bottom: 0">Aber hinter Vue.js steht keine große Firma. Ist das nicht schlecht?</p>
              <small>Just now</small>
            </div>
          </div>
        </section>

        <section v-if="step === 28" class="bg-primary">
          <div class="wrap">
            <div class="content-right" style="text-align: right">
              <h2>Bob</h2>
              <p style="margin-bottom: 0">So wie Linux oder jQuery. Das kann auch ein Vorteil sein. So sind die
                Entwickler nicht starren Firmenzielen unterlegen.</p>
              <small>Just now</small>
            </div>
          </div>
        </section>

        <section v-if="step === 29" class="bg-primary">
          <div class="wrap">
            <div class="content-left">
              <h2>Alice</h2>
              <p style="margin-bottom: 0">Na ja, niemand bei uns kann Vue.js.</p>
              <small>Just now</small>
            </div>
          </div>
        </section>

        <section v-if="step === 30" class="bg-primary">
          <div class="wrap">
            <div class="content-right" style="text-align: right">
              <h2>Bob</h2>
              <p style="margin-bottom: 0">Gefühlt ist Vue.js 55 % reines JavaScript, 15 % HTML, 20 % CSS und 10 %
                Vue.js-spezifisch. Laut Nutzern ist die Lernkurve zudem sehr steil.</p>
              <small>Just now</small>
            </div>
          </div>
        </section>

        <section v-if="step === 31" class="bg-primary">
          <div class="wrap">
            <div class="content-left">
              <h2>Alice</h2>
              <p style="margin-bottom: 0">Aber Bob, das klingt alles wahnsinning wartungsaufwendig.</p>
              <small>Just now</small>
            </div>
          </div>
        </section>

        <section v-if="step === 32" class="bg-primary">
          <div class="wrap">
            <div class="content-right" style="text-align: right">
              <h2>Bob</h2>
              <p style="margin-bottom: 0">Überhaupt nicht, Alice! Vue.js bringt eine CLI mit, welche automatisch
                Code-Qualität gewährleistet, produktionsfähige Apps ohne Konfigurationen erstellt und sogar eine
                grafische Oberfläche bietet.</p>
              <small>Just now</small>
            </div>
          </div>
        </section>

        <section v-if="step === 33">
          <div class="wrap aligncenter">
            <p class="text-subtitle">Es ist noch lange nicht Schluss.</p>
            <h2>Vue.js Zukunft</h2>
          </div>
        </section>

        <section v-if="step === 34" class="fullscreen bg-purple">
          <div class="wrap">
            <h2>Aussicht<sup>2</sup></h2>
            <p class="text-intro">Vue.js hat ehrgeizige Ziele, die in die nächsten Jahre hinein reichen.</p>
            <ul class="flexblock">
              <li>
                <div>
                  <h3>Features</h3>
                  <ol>
                    <li>Neue Features durchgehen RFC-Prozess</li>
                    <li>Major-Changes sechs Monate Vorlauf</li>
                    <li>Minor-Changes mit dreiwöchiger Beta</li>
                  </ol>
                </div>
              </li>
              <li>
                <div>
                  <h3>Sicherheit</h3>
                  <ol>
                    <li>Major-Changes besitzen 18 Monate LTS</li>
                    <li>Danach 18 weitere Monate für Fehler</li>
                    <li>Vue.js besitzt 100 % Testabdeckung</li>
                  </ol>
                </div>
              </li>
              <li>
                <div>
                  <h3>Zukunft</h3>
                  <ol>
                    <li>Support für WebAssembly</li>
                    <li>Dank <code style="display: contents">--modern</code> moderne Browser</li>
                    <li>Unterstützung für Web Components</li>
                  </ol>
                </div>
              </li>
            </ul>
          </div>
        </section>

        <section v-if="step === 35">
          <div class="wrap">
            <h2>Quellen</h2>
            <p class="text-intro">Wer hat's erfunden.</p>
            <p style="margin-bottom: 0"><sup>1</sup> https://vuejs.org</p>
            <p style="margin-bottom: 0"><sup>2</sup> https://github.com</p>
            <p style="margin-bottom: 0"><sup>3</sup> https://www.netguru.co</p>
            <p style="margin-bottom: 0"><sup>4</sup> https://twitter.com</p>
            <p style="margin-bottom: 0"><sup>5</sup> https://www.monterail.com</p>
            <p style="margin-bottom: 0"><sup>6</sup> https://discventionstech.wordpress.com</p>
            <p style="margin-bottom: 0"><sup>7</sup> https://www.stefankrause.net</p>
          </div>
        </section>
      </article>
    </slide>
  </div>
</template>

<script>
import { Slideshow } from 'eagle.js'
import find from 'lodash/find'
import findIndex from 'lodash/findIndex'
import uniqueId from 'lodash/uniqueId'
import cloneDeep from 'lodash/cloneDeep'

import LearningCurve from './components/LearningCurve'
import PerformanceComparison from './components/PerformanceComparison'

Slideshow.methods.handleResize = () => null
Slideshow.methods.click = () => null

export default {
  mixins: [Slideshow],

  components: {
    LearningCurve,
    PerformanceComparison
  },

  data: () => ({
    product: {
      title: 'Jeans',
      description: 'A well fitting Jeans. Modern. Stylish.',
      price: 50,
      amount: 1
    },

    user: {
      eMail: '',
      password: ''
    },

    isValidEMail: true,
    isValidPassword: true,

    todo: '',
    todos: [],

    removedTodo: {}
  }),

  computed: {
    total: {
      get () {
        return this.product.price * this.product.amount
      }
    }
  },

  watch: {
    'user.eMail' () {
      this.isValidEMail = /\S+@\S+\.\S+/.test(this.user.eMail)
    },

    'user.password' () {
      this.isValidPassword = /^(?=.*[A-Za-z])(?=.*\d)[A-Za-z\d]{8,}$/.test(this.user.password)
    }
  },

  methods: {
    removeTodo (identifier) {
      const todo = find(this.todos, ['identifier', identifier])
      const index = findIndex(this.todos, ['identifier', identifier])

      this.removedTodo = todo

      this.todos.splice(index, 1)
    },

    saveTodo () {
      const todo = cloneDeep(this.todo)
      this.todos.push({
        identifier: uniqueId(),
        text: todo
      })

      this.todo = ''
    },

    undoTodo () {
      this.todos.push(this.removedTodo)

      this.removedTodo = {}
    }
  }
}
</script>

<style lang="scss">
  html {
    font-size: 100%;
    hyphens: auto;
    overflow: hidden;
  }

  button:hover, button:active {
    box-shadow: none;
    border: none;
    outline: none;
  }

  table {
    margin: 0;
  }

  thead {
    background-color: transparent;
  }

  table td, th, thead {
    border: none;
  }

  tr:nth-child(even) > td {
    background: none;
  }

  thead th, th {
    text-transform: none;
  }

  .specs li:after {
    background: transparent;
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

  .metrics li {
    width: 33.33333%;
  }

  @media (min-width: 768px) {
    .fullscreen [class*='card'] .flex-content, .fullscreen [class*='card'] blockquote {
      /*padding: 3rem;*/
    }
  }

  .flexblock li.active a, .metrics li:hover, .specs li:hover, .reasons li:hover {
    background-color: transparent;
  }

  fieldset {
    background-color: transparent;
    border: none;
  }

  input:hover, select:hover {
    -webkit-box-shadow: none;
    box-shadow: none;
  }

  button, input, select, textarea, button[type='submit'], input[type='submit'], .button, .button:hover, button[type='submit']:hover, input[type='submit']:hover {
    border: 1px solid #626364;
    outline: none;
  }

  a.button, [class*='badge-'], button[type='submit'], input {
    -webkit-box-shadow: none;
    box-shadow: none;
  }

  input:focus, textarea:focus {
    background-color: transparent;
    -webkit-box-shadow: none;
    box-shadow: none;
  }

  .logo {
    text-transform: none;
  }

  input, textarea {
    background-color: transparent;
  }
</style>
