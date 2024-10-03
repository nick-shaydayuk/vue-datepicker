<template>
    <div class="wrapper">
        <Datepicker
         v-model="selectedDate" 
         placeholder="Select Date" 
         locale="ru" 
         select-text="Выбрать" 
         cancel-text="Отменить" 
         :range="{ 
            maxRange: 729, 
            disableTimeRangeValidation: false,
            inPeriodRange: true,
         }" 
         :min-date="new Date('01/01/2023')" 
         :max-date="new Date('11/01/2024')" 
         month-picker
         />
    </div>
</template>

<script lang="ts" setup>
    import { ref } from 'vue';
    import Datepicker from '../src/VueDatePicker/VueDatePicker.vue';

    const selectedDate = ref();
</script>

<style lang="scss">
    @import 'src/VueDatePicker/style/main';
    .wrapper {
        padding: 200px;
    }
</style>
