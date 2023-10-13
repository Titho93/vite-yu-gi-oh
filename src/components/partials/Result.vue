<script>

import { store } from '../../data/store';

export default {
    name: 'Result',
    data() {
        return{
            store
        }
    },
    computed: {
        outputResult(){
            if(store.cardsList.length > 0) {
                return 'Found ' + store.cardsList.length + ' Cards';
            }
            return 'Cards Not Found';
        }
    }
}
</script>

<template>
    <div class="row">
        <div class="col-12">
            <p>{{ outputResult }}</p>
        </div>
    </div>
  
</template>

<style lang="scss" scoped>

p {
    background-color: black;
    width: 100%;
    padding: 20px;
    color: white;
}
.row{
        padding: 0px 20px;
        padding-top: 50px;
    }
</style>