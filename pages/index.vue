<template>
  <div>
    <SfSteps v-model="active" :steps="steps" :can-go-back="canGoBack">
      <SfStep v-for="(step, key) in steps" :key="key" :name="step">
        <div
          style="
            display: flex;
            align-items: center;
            justify-content: center;
            height: 18.75rem;
            background-color: #f2f2f2;
          "
        >
          {{ step }}
        </div>
      </SfStep>
    </SfSteps>
  </div>
</template>
<script>
import { SfSteps } from '@storefront-ui/vue'
export default {
  components: {
    SfSteps,
  },
  data() {
    return {
      active: 0,
      steps: ['Personal details', 'Shipping', 'Billing address'],
      canGoBack: true,
    }
  },
}
</script>
