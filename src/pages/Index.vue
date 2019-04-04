<template>
  <q-page style="position: relative;">
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
                <i class="secondaryText">Full Stack Javascript Programmer</i> <br/>MGG is a software company founded by Steven Tan, which headquartered in Singapore. MGG's flagship product is Snaapp, school notification and attendance app. Snaapp widely used at schools in Singapore.
              </div>
            </q-timeline-entry>
            <q-timeline-entry
              title="KapanLagi Network"
              subtitle="April 2015"
              side="right"
            >
              <div>
                <i class="secondaryText">Backend PHP Programmer</i> <br />Write “clean”, well designed PHP Framework code, HTML, CSS, jQuery and AJAX. Produce detailed specifications. Troubleshoot, test and maintain the core product software and databases to ensure strong optimization and functionality. Contribute in all phases of the development lifecycle. Follow industry best practices. Develop and deploy new features to facilitate related procedures and tools if necessary. Implement staging development environment product.
              </div>
            </q-timeline-entry>
            <q-timeline-entry
              title="PT Omron Manufacturing of Indonesia"
              subtitle="20 September 2010"
              side="left"
            >
              <div>
                <i class="secondaryText">Production Maintenance Leader</i><br /> Responsibilities to maintain and improve machine performance. include Programming Omron PLC. Establish production maintenance system whether emergency or preventive maintenance. Making schedule of maintenance activity. Coordinate with production side to implement maintenance activity & improvement. Controlling implementation of maintenance system. Controlling machine performance. Skillup subordinates. Ensure "Safety First" in all activity & machinery. Make downtime machinery report.
              </div>
            </q-timeline-entry>
          </q-timeline>
        </q-item-main>
      </q-item>
      <q-list-header id="portfolio">
          Portfolio
      </q-list-header>
      <q-item>
        <q-item-main>
          <p class="secondaryText">Here is some of them..</p>
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
              <q-rating slot="subtitle" v-model="content.project.one" :max="5" disable />
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
              <q-rating slot="subtitle" v-model="content.project.two" :max="5" disable />
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
              <q-rating slot="subtitle" v-model="content.project.three" :max="5" disable />
              <div slot="right" class="row items-center">
              </div>
            </q-card-title>
            <q-card-main>
              <p>Pixy Commercial Campaign</p>
              <p class="text-faded">Build with Php CI, Html, Css, jQuery, Facebook Auth, Twitter OAuth</p>
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
              <q-rating slot="subtitle" v-model="content.project.one" :max="5" disable />
              <div slot="right" class="row items-center">
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
          <q-card inline class="cardProject">
            <q-card-media>
              <img src="~assets/gettygoal.jpg">
            </q-card-media>
            <q-card-title>
              GettyGoal
              <q-rating slot="subtitle" v-model="content.project.one" :max="5" disable />
              <div slot="right" class="row items-center">
              </div>
            </q-card-title>
            <q-card-main>
              <p>Football Portal</p>
              <p class="text-faded">Build with CI, HTML, CSS, Javascript, Livescore API</p>
            </q-card-main>
            <q-card-separator />
            <q-card-actions>
              <q-btn flat round dense icon="event" />
              <q-btn flat label="Copyright 2017" />
            </q-card-actions>
          </q-card>
          <q-card inline class="cardProject">
            <q-card-media>
              <img src="~assets/samsung4g.jpg">
            </q-card-media>
            <q-card-title>
              Samsung 4G
              <q-rating slot="subtitle" v-model="content.project.two" :max="5" disable />
              <div slot="right" class="row items-center">
              </div>
            </q-card-title>
            <q-card-main>
              <p>Gerakan mendukung 4G di Indonesia oleh Samsung</p>
              <p class="text-faded">Build with CI, HTML, CSS, Javascript, Facebook Auth, Twitter Oauth</p>
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
      <q-list-header id="about">About Us</q-list-header>
      <q-item>
        <q-item-main>
          {{ content.aboutPage }}
        </q-item-main>
      </q-item>
      <q-item>
        <q-item-main>
          <div class="divByTwo left">
            <q-item v-for="(val, k) in content.basicInfo" :key="k">
              <q-item-side>{{ k | capitalize }}</q-item-side><q-item-side />
              <q-item-main>{{ val | capitalize }}</q-item-main>
            </q-item>
          </div>
          <div class="divByTwo">
            <q-item v-for="(val, k) in content.education" :key="k">
              <q-item-side>{{ k | capitalize }}</q-item-side><q-item-side />
              <q-item-main>{{ val | capitalize }}</q-item-main>
            </q-item>
          </div>
        </q-item-main>
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
    </q-list>
    <q-page-sticky position="bottom-right" :offset="[18, 30]" style="position: absolute; right: 20px; bottom: 30px;">
      <q-btn fab color="info" icon="cloud_download" class="animate-pop" @click="downloadCV()"/>
    </q-page-sticky>
  </q-page>
</template>

<script>

import { openURL } from 'quasar'

export default {
  name: 'Index',
  data () {
    return {
      content: {
        aboutPage: 'Hi, i am a Software Engineer. My daily work as javascript programmer. Experienced in developing modern SPA web App and Hybrid websites. I am fast learner and loved new things in software development technologies that can solve our problem in better way.',
        basicInfo: {
          name: 'Indra Kurneamin',
          age: '29'
        },
        education: {
          diploma: 'Manajemen Informatika - Politeknik Negeri Malang',
          bachelor: 'Computer Science - Universitas Mercubuana'
        },
        project: {
          one: 4,
          two: 3,
          three: 5
        },
        skills: {
          NodeJs_FeathersJs: { val: 75, color: 'secondary' },
          VueJs: { val: 75, color: 'secondary' },
          Quasar_Framework: { val: 75, color: 'secondary' },
          AngularJs: { val: 85, color: 'secondary' },
          ReactJs: { val: 50, color: 'secondary' },
          CodeIgniter: { val: 80, color: 'secondary' },
          GIT: { val: 75, color: 'secondary' },
          PLC_Omron: { val: 50, color: 'secondary' }
          // CSS: { val: 70, color: 'secondary' },
        }
      },
      openURL
    }
  },
  filters: {
    capitalize: function (value) {
      if (!value) return ''
      value = value.toString()
      return value.charAt(0).toUpperCase() + value.slice(1)
    }
  },
  methods: {
    downloadCV () {
      // this.openURL('../downloads/indro-cv-march-2019.pdf') // local
      this.openURL('https://github.com/idr17/portfolio/blob/master/src/downloads/indro-cv-march-2019.pdf')
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
.q-list-header { color: #00deb3; border-bottom: solid 2px #00deb3; }
.divByTwo { width: 40%; display: inline; }
.left { float: left; }
.secondaryText { color: #737373; }
@media screen and (max-width: 400px) {
  .divByTwo { width: 100%; display: block; }
}
</style>
