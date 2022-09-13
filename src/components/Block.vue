 <template >
    <div class="block" v-if="showBlock">
      click me  
    </div>
 </template>


 <script>
 export default {
    props: ['delay'],
    data() {
        return {
            showBlock: false
        }
    },
    mounted() {
        console.log('Mounted')
        setTimeout(() => {
            this.showBlock = true
        }, this.delay);
    },
 }
 </script>


 <style>
    .block{
        width: 400px;
        border-radius: 40px;
        color: white;
        background: #0faf87;
        text-align: center;
        padding: 100px 0;
        margin: 40px auto;
    }
 </style>