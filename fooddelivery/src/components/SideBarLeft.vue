<template>
    <v-navigation-drawer app color='green accent-3' dark>
        <v-list-item class="px-2 py-5">
            <v-list-item-title class="text-capitalize" align="center">
                <v-icon x-large class="pr-2">fas fa-hamburger</v-icon> Foodify
            </v-list-item-title>
        </v-list-item>
        <v-list shaped>
            <v-list-item-group v-model="selectedItem" color="grey lighten-5">
                <v-list-item v-for="(item, i) in items" :key="i">
                    <v-list-item-icon>
                        <v-icon v-text="item.icon"></v-icon>
                    </v-list-item-icon>
                    <v-list-item-content>
                        <v-list-item-title v-text="item.text"></v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
            </v-list-item-group>
        </v-list>
    </v-navigation-drawer>
</template>

<script>
    export default {
        data: () => ({
            selectedItem: 0,
            items: [
                {icon: 'fas fa-shipping-fast', text: 'Overview', route: '/overview'},
                {icon: 'fas fa-bars', text: 'Menu', route: '/menu'},
                {icon: 'fas fa-dollar-sign', text: 'Transaction', route: '/transaction'},
                {icon: 'fas fa-calendar-alt', text: 'Calendar', route: '/calendar'},
                {icon: 'fas fa-cogs', text: 'Testimonials', route: '/testimonials'},
                {icon: 'fas fa-question', text: 'About Us', route: '/faq'},
            ],
        })
    }
</script>

<style>

</style>