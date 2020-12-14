<template>
    <h1>{{ this.path }}</h1>
</template>

<script>
export default {
    async asyncData({ params }) {
        return new Promise((resolve, reject) => {
            resolve({
                path: params.path
            })
        })
    }
}
</script>