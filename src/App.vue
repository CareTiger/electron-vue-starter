<template>
    <div class="min-h-screen text-zinc-900 dark:text-zinc-50 bg-zinc-100 dark:bg-zinc-800">
        <header>
            <div>
                <nav>
                    <div class="relative card z-2">
                        <Menubar :model="items" />
                    </div>
                </nav>
            </div>
        </header>

        <RouterView />
    </div>
</template>

<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
import { ref } from "vue";
import Menubar from "primevue/menubar";

const items = ref([
    {
        label: "Edit",
        icon: "pi pi-fw pi-pencil",
        items: [
            {
                label: "Left",
                icon: "pi pi-fw pi-align-left",
                onclick: () => {
                    console.log("Left");
                }
            },
            {
                label: "Right",
                icon: "pi pi-fw pi-align-right"
            }
        ]
    },
    {
        label: "Quit",
        icon: "pi pi-fw pi-power-off"
    }
]);
</script>
