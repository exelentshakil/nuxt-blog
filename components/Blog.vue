<template>
    <div class="blogs__card">
        <h1>{{ blog.title }}</h1>
        <p class="description">{{blog.body}}</p>
        <p class="btn"><NuxtLink :to="'/blogs/' + blog.id">Learn More</NuxtLink></p>
    </div>
</template>
<script>
export default {
    loading: {
        color: 'red',
        height:'30'
    },
    props: {
        blog: {
            type: Object,
            required: true
        }
    }
}
</script>