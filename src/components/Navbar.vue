<template>
    <div>
        <nav>
            <div>
                <ul>
                    <li><a href="">Home</a></li>
                    <li><a href="">Profile</a></li>
                    <li><a href="">About</a></li>
                    <li><a href="">Contacts</a></li>
                </ul>
            </div>
        </nav>
    </div>
</template>

<script>
export default {
    name:'Navbar',
    data(){
        return {

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
}
nav li{
    padding: 8px;
    margin: 0;
    display: inline-block;
    list-style-type: none;
    
}

</style>
