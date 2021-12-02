<template>
    <ion-page>
        <ion-header>
            <ion-toolbar>
                <ion-title>With Modal Controller</ion-title>
            </ion-toolbar>
        </ion-header>
        <ion-content :fullscreen="true">
            <ion-header collapse="condense">
                <ion-toolbar>
                    <ion-title size="large">With Modal Controller</ion-title>
                </ion-toolbar>
            </ion-header>
        </ion-content>
        <ModalController />
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
import ModalController from "@/components/ModalController.vue";

export default {
    name: "Tab4",
    components: {
        IonHeader,
        IonToolbar,
        IonTitle,
        IonContent,
        IonPage,
        ModalController,
    },
};
</script>