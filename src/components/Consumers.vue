<script lang="ts">
import { defineComponent } from 'vue';
import ConsumerModel from '@/models/ConsumerModel'

export default defineComponent({
    props: {
        userList: Array<ConsumerModel>,
        includeMe: Boolean
    },
    emits: ['update:includeMe'],
    data() {
        return {};
    },
    methods:
    {
        selectAll() {
            if (!this.userList) return;
            this.userList.forEach(element => {
                element.selected = true;
            });
        },
        deselectAll() {
            if (!this.userList) return;
            this.userList.forEach(element => {
                element.selected = false;
            });
        }
    }
})
</script>

<template>
    <div class="text-center fs-5 my-2">Consumers</div>


    <div class="d-flex flex-row align-items-end p-2 ps-0">
        <input v-model="includeMe" class="form-check-input fs-2" type="checkbox" value="" id="flexCheckChecked">
        <label class="form-check-label ms-2" for="flexCheckChecked">
            Include Me
        </label>
    </div>
    <select class="form-select" multiple aria-label="multiple select example">
        <option v-for="user, index in userList" :value="index" :selected="user.selected">{{ user.name }}</option>
    </select>
    <div class="btn-group w-100 mt-2" role="group" aria-label="Basic example">
        <button type="button" @click="selectAll" class="btn btn-outline-primary">Select All</button>
        <button type="button" @click="deselectAll" class="btn btn-outline-primary">Deselect All</button>
    </div>
</template>