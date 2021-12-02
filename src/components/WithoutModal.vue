<template>
    <div class="ion-padding">
        <p class="ion-text-center">showText: {{ showText }}</p>
        <IonButton expand="block" @click="toggleText">
            Toggle showText
        </IonButton>
        <div v-if="showText" class="ion-margin-top ion-text-center">
            Show this text if showText = true
        </div>
        <div v-else class="ion-margin-top ion-text-center">
            Show this text if showText = false
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import { IonButton } from "@ionic/vue";

export default defineComponent({
    name: "WithoutModal",
    components: {
        IonButton,
    },
    data() {
        return {
            isOpen: false,
            showText: false,
        };
    },
    mounted() {
        this.isOpen = true;
    },
    methods: {
        toggleText(): void {
            this.showText = !this.showText;

            console.log(`showText = ${this.showText}`);
        },
    },
});
</script>
