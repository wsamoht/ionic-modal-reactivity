<template>
    <ion-page>
        <ion-header>
            <ion-toolbar>
                <ion-title>Options API</ion-title>
            </ion-toolbar>
        </ion-header>
        <ion-content :fullscreen="true">
            <ion-header collapse="condense">
                <ion-toolbar>
                    <ion-title size="large">Options API</ion-title>
                </ion-toolbar>
            </ion-header>
        </ion-content>
        <OptionsModal />
    </ion-page>
</template>

<script lang="ts">
import {
    IonPage,
    IonHeader,
    IonToolbar,
    IonTitle,
    IonContent,
} from "@ionic/vue";
import OptionsModal from "@/components/OptionsModal.vue";

export default {
    name: "Tab1",
    components: {
        IonHeader,
        IonToolbar,
        IonTitle,
        IonContent,
        IonPage,
        OptionsModal,
    },
};
</script>