<template>
    <ion-page>
        <ion-header>
            <ion-toolbar>
                <ion-title>Without Modal</ion-title>
            </ion-toolbar>
        </ion-header>
        <ion-content :fullscreen="true">
            <ion-header collapse="condense">
                <ion-toolbar>
                    <ion-title size="large">Without Modal</ion-title>
                </ion-toolbar>
            </ion-header>
            <WithoutModal />
        </ion-content>
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
import WithoutModal from "@/components/WithoutModal.vue";

export default {
    name: "Tab3",
    components: {
        IonHeader,
        IonToolbar,
        IonTitle,
        IonContent,
        IonPage,
        WithoutModal,
    },
};
</script>