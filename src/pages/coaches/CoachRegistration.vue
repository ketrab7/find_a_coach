<template>
    <section>
        <base-card>
            <h2>Register as a coach now!</h2>
            <coach-filter @save-data="saveData"></coach-filter>
        </base-card>
    </section>
</template>

<script>
import CoachFilter from '../../components/coaches/CoachForm.vue';

export default {
    components: {
        CoachFilter
    },
    methods: {
        saveData(data) {
            this.$store.dispatch('coaches/registerCoach', data);
            this.$router.replace('/coaches');
        }
    }
}
</script>