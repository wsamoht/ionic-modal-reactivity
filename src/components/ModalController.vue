<script lang="ts">
import { defineComponent, ref } from "vue";
import { modalController } from "@ionic/vue";
import ModalControllerComponent from "./ModalControllerComponent.vue";

export default defineComponent({
    name: "ModalController",
    async setup() {
        const showText = ref(false);

        const toggleText = (): void => {
            showText.value = !showText.value;

            console.log(`showText = ${showText.value}`);
        };

        const modal = await modalController.create({
            component: ModalControllerComponent,
            componentProps: {
                showText: showText,
            },
        });

        modal.present();

        const interval = setInterval(() => {
            toggleText();
        }, 2000);

        setTimeout(() => {
            clearInterval(interval);
        }, 10000);
    },
});
</script>
