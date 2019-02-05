<template>
  <q-page>
    <q-list class="careerContent" id="workingEksperience">
      <q-list-header>Working Experience</q-list-header>
      <q-item>
        <q-item-main>
          <q-timeline responsive color="secondary" style="padding: 0 24px;">
            <!-- <q-timeline-entry heading>Working Experience</q-timeline-entry> -->
            <q-timeline-entry
              title="MGG Software Pte.Ltd"
              subtitle="1 February 2018 - Current"
              side="left"
            >
              <div>
                MGG is a software company founded by Steven Tan, which headquartered in Singapore. MGG's flagship product is Snaapp, school notification and attendance app. Snaapp widely used at schools in Singapore. I work here as Full Stack Javascript Programmer.
              </div>
            </q-timeline-entry>
            <q-timeline-entry
              title="KapanLagi Network"
              subtitle="April 2015"
              side="right"
            >
              <div>
                Write “clean”, well designed PHP Framework code, HTML, CSS, jQuery and AJAX. Produce detailed specifications. Troubleshoot, test and maintain the core product software and databases to ensure strong optimization and functionality. Contribute in all phases of the development lifecycle. Follow industry best practices. Develop and deploy new features to facilitate related procedures and tools if necessary. Implement staging development environment product.
              </div>
            </q-timeline-entry>
            <q-timeline-entry
              title="PT Omron Manufacturing of Indonesia"
              subtitle="20 September 2010"
              side="left"
            >
              <div>
                Production Maintenance Production Switch.<br /> Responsibilities to maintain and improve machine performance. include Programming Omron PLC. Establish production maintenance system whether emergency or preventive maintenance. Making schedule of maintenance activity. Coordinate with production side to implement maintenance activity & improvement. Controlling implementation of maintenance system. Controlling machine performance. Skillup subordinates. Ensure "Safety First" in all activity & machinery. Make downtime machinery report.
              </div>
            </q-timeline-entry>
          </q-timeline>
        </q-item-main>
      </q-item>
      <q-list-header>
          Portfolio
      </q-list-header>
      <q-item id="portfolio">
        <q-item-main>
          Here is some of them..
        </q-item-main>
      </q-item>
      <q-item>
        <q-item-main>
          <q-card inline class="cardProject">
            <q-card-media>
              <img src="~assets/klsingapore.jpg">
            </q-card-media>
            <q-card-title>
              KapanlagiKeSingapura
              <q-rating slot="subtitle" v-model="content.project.one" :max="5" />
              <div slot="right" class="row items-center">
                <!-- <q-icon name="place" /> 250 ft -->
              </div>
            </q-card-title>
            <q-card-main>
              <p>Singapore Tourism Board</p>
              <p class="text-faded">Build with Php CI, Html, Css, jQuery</p>
            </q-card-main>
            <q-card-separator />
            <q-card-actions>
              <q-btn flat round dense icon="event" />
              <q-btn flat label="Copyright 2018" />
            </q-card-actions>
          </q-card>
          <q-card inline class="cardProject">
            <q-card-media>
              <img src="~assets/garnier.jpg">
            </q-card-media>
            <q-card-title>
              #GarnierSuperready
              <q-rating slot="subtitle" v-model="content.project.two" :max="5" />
              <div slot="right" class="row items-center">
                <!-- <q-icon name="place" /> 250 ft -->
              </div>
            </q-card-title>
            <q-card-main>
              <p>Garnier Commercial Campaign</p>
              <p class="text-faded">Build with Php CI, Html, Css, jQuery, Instagram API</p>
            </q-card-main>
            <q-card-separator />
            <q-card-actions>
              <q-btn flat round dense icon="event" />
              <q-btn flat label="Copyright 2017" />
            </q-card-actions>
          </q-card>
          <q-card inline class="cardProject">
            <q-card-media>
              <img src="~assets/pixy.jpg">
            </q-card-media>
            <q-card-title>
              Pixy Asian Beauty
              <q-rating slot="subtitle" v-model="content.project.three" :max="5" />
              <div slot="right" class="row items-center">
                <!-- <q-icon name="place" /> 250 ft -->
              </div>
            </q-card-title>
            <q-card-main>
              <p>Pixy Commercial Campaign</p>
              <p class="text-faded">Build with Php CI, Html, Css, jQuery, Facebook Auth, Twitter Auth</p>
            </q-card-main>
            <q-card-separator />
            <q-card-actions>
              <q-btn flat round dense icon="event" />
              <q-btn flat label="Copyright 2018" />
            </q-card-actions>
          </q-card>
          <q-card inline class="cardProject">
            <q-card-media>
              <img src="~assets/snaappapp.jpg">
            </q-card-media>
            <q-card-title>
              SNAAPP
              <q-rating slot="subtitle" v-model="content.project.one" :max="5" />
              <div slot="right" class="row items-center">
                <!-- <q-icon name="place" /> 250 ft -->
              </div>
            </q-card-title>
            <q-card-main>
              <p>School Notification and Attendance App</p>
              <p class="text-faded">Build with NodeJs, VueJs+Quasar Framework, AngularJs*</p>
            </q-card-main>
            <q-card-separator />
            <q-card-actions>
              <q-btn flat round dense icon="event" />
              <q-btn flat label="Copyright 2018" />
            </q-card-actions>
          </q-card>
        </q-item-main>
      </q-item>
    </q-list>
    <q-list class="personalContent">
      <div id="about">
      <!-- <q-list-header>About</q-list-header> -->
      <q-item>
        <q-item-main>
          {{ content.aboutPage }}
        </q-item-main>
      </q-item>
      <q-list-header>
        I am
      </q-list-header>
      <q-item v-for="(val, k) in content.basicInfo" :key="k">
        <q-item-side>{{ k | capitalize }}</q-item-side><q-item-side />
        <q-item-main>{{ val | capitalize }}</q-item-main>
      </q-item>
      <q-list-header>
        Education
      </q-list-header>
      <q-item v-for="(val, k) in content.education" :key="k">
        <q-item-side>{{ k | capitalize }}</q-item-side><q-item-side />
        <q-item-main>{{ val | capitalize }}</q-item-main>
      </q-item>
      <q-list-header>
        Technical Skill
      </q-list-header>
      <q-item v-for="(v, k) in content.skills" :key="k">
        <q-item-side class="skilltitle">{{ k }}</q-item-side>
        <q-item-main class="skillbar">
          <q-progress :percentage="v.val" :color="v.color" />
        </q-item-main>
      </q-item>
      <q-item><q-item-main>&nbsp;</q-item-main></q-item>
    </div>
    </q-list>
  </q-page>
</template>

<script>
export default {
  name: 'Index',
  data () {
    return {
      content: {
        aboutPage: 'Hi, saya biasa dipanggil indro. Saya suka belajar & fastlearner yang terobsesi dengan software development.',
        basicInfo: {
          name: 'Indra Kurneamin',
          age: '29 Years Old',
          hobby: 'Coding, Football, Coffee'
        },
        education: {
          diploma: 'Manajemen Informatika - Politeknik Negeri Malang',
          bachelor: 'Fasilkom - Universitas Mercubuana'
        },
        project: {
          one: 4,
          two: 3,
          three: 5
        },
        skills: {
          NodeJs_FeathersJs: { val: 75, color: 'info' },
          VueJs: { val: 75, color: 'green' },
          Quasar_Framework: { val: 75, color: 'warning' },
          AngularJs: { val: 85, color: 'blue' },
          ReactJs: { val: 50, color: 'green' },
          CodeIgniter: { val: 80, color: 'primary' },
          YII: { val: 50, color: 'yellow' },
          CSS: { val: 70, color: 'secondary' },
          GIT: { val: 75, color: 'red' }
        }
      }
    }
  },
  filters: {
    capitalize: function (value) {
      if (!value) return ''
      value = value.toString()
      return value.charAt(0).toUpperCase() + value.slice(1)
    }
  }
}
</script>

<style scoped>
.q-list { border: none; }
.personalContent { padding: 50px 30px; }
.careerContent { padding: 0 30px; }
.q-list-header { font-size: 30px; margin: 30px 0 20px 0;  }
.skillbar { margin-left: 10px; }
.skilltitle { width: 150px; }
.cardProject { width: 290px; margin: 0 10px 15px 0; }
</style>
