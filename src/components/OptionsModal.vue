<template>
    <IonModal :is-open="isOpen" @did-dismiss="isOpen = false">
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
    </IonModal>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import { IonButton, IonModal } from "@ionic/vue";

export default defineComponent({
    name: "OptionsModal",
    components: {
        IonButton,
        IonModal,
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
