<template>
  <v-container>
    <v-layout
      text-xs-center
      wrap
    >
      <v-flex mb-4>
       <quote/>
      </v-flex>

      <v-flex
        mb-5
        xs12
      >
        <h2 class="headline font-weight-bold mb-3">Social media</h2>

        <v-layout justify-center>
          <a
            v-for="(next, i) in socialMedia"
            :key="i"
            :href="next.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ next.text }}
          </a>
        </v-layout>
      </v-flex>

      <v-flex
        xs12
        mb-5
      >
        <h2 class="headline font-weight-bold mb-3">Important Links</h2>

        <v-layout justify-center>
          <a
            v-for="(link, i) in importantLinks"
            :key="i"
            :href="link.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ link.text }}
          </a>
        </v-layout>
      </v-flex>

      <v-flex
        xs12
        mb-5
      >
        <h2 class="headline font-weight-bold mb-3">Other stuff</h2>

        <v-layout justify-center>
          <a
            v-for="(eco, i) in school"
            :key="i"
            :href="eco.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ eco.text }}
          </a>
        </v-layout>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
import quote from "./quotes";
export default {
  components: {
    quote
  },
  data: () => ({
    school: [
      {
        text: "lps lunches",
        href:
          "https://www.myschoolbucks.com/ver2/login/getmain?requestAction=home"
      },
      {
        text: "parent vue",
        href: "https://synergyvue.lps.org/PXP2_Login_Parent.aspx"
      }
    ],
    importantLinks: [
      {
        text: "Current radar",
        href: "https://www.1011now.com/weather/interactiveradar"
      },
      {
        text: "Washington post",
        href: "https://www.washingtonpost.com/"
      }
    ],
    socialMedia: [
      {
        text: "Nextdoor",
        href: "https://nextdoor.com"
      },
      {
        text: "Facebook",
        href: "https://facebook.com"
      },
      {
        text: "Twitter",
        href: "https://twitter.com"
      },
      {
        text: "Reddit",
        href: "https://reddit.com"
      }
    ]
  })
};
</script>

<style>
</style>
