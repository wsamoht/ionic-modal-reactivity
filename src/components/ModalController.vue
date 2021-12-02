<script lang="ts">
import { defineComponent, ref } from "vue";
import { modalController } from "@ionic/vue";
import ModalControllerComponent from "./ModalControllerComponent.vue";

export default defineComponent({
    name: "ModalController",
    async setup() {
        let showText = false;

        const toggleText = (): void => {
            showText = !showText;

            console.log(`showText = ${showText}`);
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
