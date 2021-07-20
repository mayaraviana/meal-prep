<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
    <q-toolbar class="bg-brown-8 text-white shadow-2 rounded-borders">
      <q-btn flat label="Meal Prep" />
      <q-space />

      <!--
        notice shrink property since we are placing it
        as child of QToolbar
      -->
      <q-tabs v-model="tab" shrink class="md">
        <q-tab name="menu" label="menu" />
        <q-tab name="signin" label="Sign in" />
        <q-btn color="brown-5" name="join" label="Join" />
      </q-tabs>
      <q-btn flat round dense icon="menu" class="q-mr-sm lt-md" />
    </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'MainLayout',
})
</script>
