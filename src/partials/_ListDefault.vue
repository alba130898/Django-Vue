<template>
    <div>
        <router-link to="/detail">Detail</router-link>

        <div v-for="e in elements" v-bind:key="e.id">
            <router-link :to=" '/detail/' + e.id ">
                <b-card 
                :title="e.title"
                >
                <b-card-text>
                    {{ e.description }}
                </b-card-text>
                </b-card>
            </router-link>
        </div>

    </div>
</template>

<script>
export default {
    data(){
        return{
            elements: []
        };
    },
    methods: {
        
    },
}
</script>