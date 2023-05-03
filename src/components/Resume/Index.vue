<template>
    <main>
        <label>{{ labelSelected }}</label>
        <h1>{{ visualAmount }}</h1>
    </main>
</template>

<script setup>
import { computed, defineProps } from 'vue';

/* const props = defineProps([
    'label',
    'amount'    
]) */

const props = defineProps({
    label: {
        type: Date,
    },
    generalLabel: String,
    amount: {
        type: Number,
        default: null
    },
    totalAmount: Number,
})

const amountValue = props.amount;
const totalAmountValue = props.totalAmount;

const visualAmount = computed(() => {
    if (amountValue != null) {
        return amountValue
    }
    else {
        return totalAmountValue
    }
})

const labelValue = props.label;
const generalLabelValue = props.generalLabel;

const labelSelected = computed(() => {
    if (labelValue != null) {
        return labelValue
    }
    else {
        return generalLabelValue
    }
})
//---------------------
const emit = defineEmits('label')

//-probar con emitir label selected y label value a home para q los valores sean intecractivos---------------



</script>

<style scoped>
main {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  width: 100%;
}
h1,
p {
  margin: 0;
  text-align: center;
}
h1 {
  margin-top: 14px;
  color: var(--brand-green);
}
.graphic {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  padding: 48px 24px;
  box-sizing: border-box;
}
</style>
