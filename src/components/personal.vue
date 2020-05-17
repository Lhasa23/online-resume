<template>
  <section class="personal">
    <div class="personal-info">
      <div class="avatar">
        <img :src="imgSrc" alt="image" class="circle" render-type="background">
        <input type="file" accept="image/gif,image/jpeg,image/jpg,image/png" @change="changeImage">
      </div>
      <div
        class="name"
        contenteditable="true"
        v-html="data.name"
        @input="contentChange('name', $event)"
      />
      <div
        class="job"
        contenteditable="true"
        v-html="data.position"
        @input="contentChange('position', $event)"
      />
      <div class="location">
        <div
          class="location-name"
          contenteditable="true"
          v-html="data.location"
          @input="contentChange('location', $event)"
        />
      </div>
    </div>
    <div class="info">
      <ul>
        <li>
          <span
            class="value"
            contenteditable="true"
            v-html="data.sex"
            @input="contentChange('sex', $event)"
          />
          <br />
          <span class="key" contenteditable="true">SEX</span>
        </li>
        <li>
          <span
            class="value"
            contenteditable="true"
            v-html="data.age"
            @input="contentChange('age', $event)"
          />
          <br />
          <span class="key" contenteditable="true">AGE</span>
        </li>
        <li>
          <span
            class="value"
            contenteditable="true"
            v-html="data.degree"
            @input="contentChange('degree', $event)"
          />
          <br />
          <span class="key" contenteditable="true">DEGREE</span>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
import defaultData from '@/config/defaultData'

export default {
  name: 'Personal',
  data() {
    return {}
  }
}
</script>

<style></style>
