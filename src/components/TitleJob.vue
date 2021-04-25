<template>
    <div id="titleJob">
        <h3>{{name}}</h3>
        <button type="button" class="btn" @click="showModal">Detail</button>
        <Modal v-show="isModalVisible" @close="closeModal" v-bind:description="description" v-bind:name="name"/>
    </div>
</template>
<script>
    import Modal from './Modal.vue';
    export default {
        name: "TitleJob",
        props: {
            img: String,
            name: String,
            description: String,
            title: String,
        },
        data() {
            return {
                isModalVisible: false,
            };
        },
        methods: {
            showModal() {
                this.isModalVisible = true;
            },
            closeModal() {
                this.isModalVisible = false;
            }
        },
        components: {
            Modal,
        },
    }
</script>
<style scoped>
    #titleJob {
        box-shadow: 0px 5px 15px rgba(0,0,0,0.3);
        width: 85%;
        height: 100px;
        border-radius: 10px;
        margin: 20px 50px 10px 50px;
        transition: all 0.3s ease-in-out;
        
    }
    #titleJob:after {
  position: absolute;
  width: 85%;
  height: 100%;
  opacity: 0;
  border-radius: 5px;
  box-shadow: 0 5px 15px rgba(0,0,0,0.3);
  transition: opacity 0.3s ease-in-out;
}
#titleJob:hover {
    transform: scale(1.1, 1.1);
}
h3 {
    padding: 10px 0px 0px 20px;
}
.btn {
    width: 100px;
    height: 40px;
    color: white;
    background-color: #db5669;
    border: none;
    margin: 0px 0px 0px 20px;
    border-radius: 8px;
    outline: none;
}
</style>