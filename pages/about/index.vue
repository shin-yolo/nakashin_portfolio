<template>
  <v-row>
    <v-col
      v-for="about in abouts"
      :key="about.name"
      class="mb-8"
      min-height="300"
      cols="12"
      md="6"
      offset-md="3"
    >
      <v-card>
        <v-card-title class="subheading font-weight-bold">{{about.title}}</v-card-title>
        <v-divider></v-divider>
        <v-list>
          <v-list-item dense>
            <v-list-item-content>Name:</v-list-item-content>
            <v-list-item-content class="align-end">{{about.name}}</v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>Date of birth:</v-list-item-content>
            <v-list-item-content class="align-end">{{about.age}}</v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>Country:</v-list-item-content>
            <v-list-item-content class="align-end">{{about.country}}</v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>Profession:</v-list-item-content>
            <v-list-item-content class="align-end">{{about.profession}}</v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>Hobby:</v-list-item-content>
            <v-list-item-content class="align-end">{{about.hobby}}</v-list-item-content>
          </v-list-item>
        </v-list>
      </v-card>
    </v-col>
    <v-col
      v-for="item in education"
      :key="item.uni"
      class="mb-8"
      min-height="300"
      cols="12"
      md="6"
      offset-md="3"
    >
      <v-card>
        <v-card-title class="subheading font-weight-bold">{{item.education_title}}</v-card-title>
        <v-divider></v-divider>
        <v-list>
          <v-list-item dense>
            <v-list-item-content>University:</v-list-item-content>
            <v-list-item-content class="align-end">{{item.uni}}</v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>Major:</v-list-item-content>
            <v-list-item-content class="align-end">{{item.major}}</v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>Period:</v-list-item-content>
            <v-list-item-content class="align-end">{{item.period}}</v-list-item-content>
          </v-list-item>
        </v-list>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data() {
    return {
      abouts: [
        {
          title: "Personal Details",
          name: "Shinya Nakano",
          age: "October 6, 1999",
          country: "Japan",
          profession: "Student",
          hobby: "Work out"
        }
      ],
      education: [
        {
          education_title: "Education",
          uni: "Toyo University",
          major: "Business Administration",
          period: "April 2018 - March 2022 (expected)"
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
.card-container {
  width: 95%;
  margin: 0 auto;
  max-width: $contentMaxWidth;
}
.nested {
  display: grid;
  grid-template-columns: 1fr 2fr;
  grid-gap: 10px;
}

@media screen and (max-width: 400px) {
  .nested {
    grid-template-columns: 1fr;
  }
}
</style>
