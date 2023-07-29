<template>
    <div>
        <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">Home</a></li>
                <li><a href="#">Home</a></li>
                <li><a href="#">Home</a></li>
            </ul>
        </nav>
    </div>
</template>

<script>
export default {
    name:'Navbar',
    data(){
        return{

        }
    }
}
</script>

<style scoped>
    nav{
        text-align: center;
    }
    nav ul{
        padding: 0;
        margin: 0;
        list-style: none;
    }
    ul li{
        display: inline;
        margin: 0 5px;
    }
    ul li a{
        text-decoration: none;
    }
</style>