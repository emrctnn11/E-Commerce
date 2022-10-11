

<template>
    <div id="sideBar" class="sidebar" :style="{width: sidebarWidth}">
        <SidebarLink to="/" icon="fa fa-home">Ana Sayfa</SidebarLink>
        <SidebarLink to="/ShowCategory" icon="fa fa-columns">Ürün Ekleme</SidebarLink>
        <SidebarLink to="/AddCategory" icon="fa fa-image">Ürün Listeleme</SidebarLink>

        <span class="collapse-icon" :class="{ 'rotate-180': collapsed}" @click="toggleSidebar">
            <i class="fa fa-angle-double-left"></i>
        </span>
    </div>
</template>

<script>
import {collapsed, toggleSidebar, sidebarWidth} from './/state.js'
import SidebarLink from './SidebarLink.vue';


export default {
    props: {},
    components: { SidebarLink },
    setup() {
        return { collapsed, toggleSidebar, sidebarWidth };
    },
    
}
</script>

<style>
:root {
    --sidebar-bg-color: #852f2f;
    --sidebar-item-hover: #642626;
    --sidebar-item-active: #672727;
}
</style>

<style scoped>

#sideBar {
    position: sticky;
    height: calc(100vh);
}
.sidebar {
    color: white;
    background-color: var(--sidebar-bg-color);

    height: calc(100vh);
    position: sticky;

    float: left;
    position: fixed;
    z-index: 1;
    top: 0;
    left: 0;
    bottom: 0;
    padding: 0.5em;

    transition: 0.3s ease;

    display: flex;
    flex-direction: column;
}
.collapse-icon {
    position: absolute;
    bottom: 0;
    font-size: 50px;

    color: rgba(255, 255, 255, 0.7);

    transition: 0.2s linear;
}

.rotate-180 {
    transform: rotate(180deg);
    transition: 0.2s linear;
}
</style>