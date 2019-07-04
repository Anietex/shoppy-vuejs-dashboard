<template>
    <div class="page-container">
        <div class="left-content">
            <div class="mother-grid-inner">
                <app-header/>
                <div class="inner-block">
                    <router-view/>
                </div>
                <app-footer/>
            </div>
        </div>
        <sidebar/>
        <div class="clearfix"> </div>
    </div>
</template>

<script>
    import AppHeader from "./AppHeader";
    import Sidebar from "./Sidebar";
    import AppFooter from "./AppFooter";
    export default {
        name: "AppLayout",
        components: {AppFooter, Sidebar, AppHeader}
    }
</script>

<style scoped>

</style>