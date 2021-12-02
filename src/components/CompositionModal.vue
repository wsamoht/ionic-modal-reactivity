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
import { defineComponent, ref } from "vue";
import { IonButton, IonModal } from "@ionic/vue";

export default defineComponent({
    name: "CompositionModal",
    components: {
        IonButton,
        IonModal,
    },
    setup() {
        const isOpen = ref(false);
        const showText = ref(false);

        isOpen.value = true;

        const toggleText = (): void => {
            showText.value = !showText.value;

            console.log(`showText = ${showText.value}`);
        };

        return {
            isOpen,
            showText,

            toggleText,
        };
    },
});
</script>
