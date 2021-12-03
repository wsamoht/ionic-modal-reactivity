<template>
    <div class="ion-padding">
        <p class="ion-text-center">showText: {{ showText }}</p>
        <div v-if="showText.value" class="ion-margin-top ion-text-center">
            Show this text if showText = true
        </div>
        <div v-else class="ion-margin-top ion-text-center">
            Show this text if showText = false
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
    name: "ModalControllerComponent",
    props: {
        showText: {
            required: true,
        },
    },
});
</script>
