<template>
    <Navbar />
    <div class="d-flex">
        <div class="col-4">
            <EntryList />
        </div>
        <div class="col"> <!--con ese col toma todo el tamaño restante-->
            <router-view />
        </div>
    </div>
</template>

<script>

import { defineAsyncComponent } from "vue";
    export default {
        components: {
            Navbar: defineAsyncComponent(()=> import('../components/Navbar.vue')),
            EntryList: defineAsyncComponent(()=> import('../components/EntryList.vue')),
        }
    }
</script>