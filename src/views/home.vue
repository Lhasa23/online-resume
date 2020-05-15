<template>
    <section>
        hello
        <contact>
        </contact>
        <education></education>
        <experience></experience>
        <personal></personal>
    </section>
</template>

<script>
import contact from '@/components/contact'
import education from '../components/education'
import experience from '../components/experience'
import personal from '../components/personal'

export default {
    name: 'Home',
    components: {
        contact,
        education,
        experience,
        personal
    }
}
</script>

<style>

</style>