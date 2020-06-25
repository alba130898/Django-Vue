<template>
    <div class="container">

            <b-card 
            :title="element.title"
            >
            </b-card>
            <b-card-text>
                {{ element.description }}
            </b-card-text>

    </div>
</template>

<script>
export default {

    created(){
        this.find()
    },
    data(){
        return{
            element: Object
        };
    },
    methods: {
        find: function(){
            fetch('http://127.0.0.1:8000/api/element/1/?format=json')
            .then(res => res.json())
            .then(res => this.element = res)
        }
    },
}
</script>