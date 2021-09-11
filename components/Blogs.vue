<template>
    <div class="blogs-page">
        <div class="blogs">
            <Blog v-for="blog in blogs" :key="blog.id" :blog="blog"/>
        </div>
    </div>
</template>

<script>
import axios from 'axios'

export default {

    data(){
        return {
            blogs: []
        }
    },
    methods: {
        async fetchBlogs(){
            try {
                const req = await axios.get('https://jsonplaceholder.typicode.com/posts');
                const posts = await req.data;
                this.blogs = posts;
            } catch ( err ) {
                console.log(err);
            }
        }
    },
    mounted() {
        this.fetchBlogs();
    }

}
</script>

<style>
.blogs {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 10px;
    width:100%;
}

.blogs__card {
    padding: 30px;
    background: #000;
    color: #fff;
    width:250px;
}


.blogs__card h1 {
    font-size: 20px;
    font-weight: 700;
}

.blogs__card p {
    font-size: 12px;
    font-weight: 400;
    margin-bottom: 20px;
}



.btn a {
    padding: 10px 20px;
    background: #801b1bde;
    margin-top: 44px !important;
}




</style>