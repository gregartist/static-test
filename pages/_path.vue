<template>
    <div>
        <h1>{{ this.path }}</h1>
        <p>{{ this.message }}</p>
    </div>
    
</template>

<script>
export default {
    async asyncData({ params, $http }) {
        // return new Promise((resolve, reject) => {
        //     resolve({
        //         path: params.path,
        //         message: "test"
        //     })
        // })
        const data = await $http.$get(`/api/GetMessage`)
        return {
            path: params.path,
            message: data.message
        }
        // return axios.get('/api/GetMessage')
        //     .then(function(response){
        //         return {
        //             path: param.path,
        //             message: response
        //             }
        //     })
    }
}
</script>