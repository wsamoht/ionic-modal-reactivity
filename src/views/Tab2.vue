<template>
    <ion-page>
        <ion-header>
            <ion-toolbar>
                <ion-title>Composition API</ion-title>
            </ion-toolbar>
        </ion-header>
        <ion-content :fullscreen="true">
            <ion-header collapse="condense">
                <ion-toolbar>
                    <ion-title size="large">Composition API</ion-title>
                </ion-toolbar>
            </ion-header>
        </ion-content>
        <CompositionModal />
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
import CompositionModal from "@/components/CompositionModal.vue";

export default {
    name: "Tab2",
    components: {
        IonHeader,
        IonToolbar,
        IonTitle,
        IonContent,
        IonPage,
        CompositionModal,
    },
};
</script>