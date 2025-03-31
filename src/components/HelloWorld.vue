<template>
<div class="home"> 
    <v-form>
        <v-file-input label="Selecione as legendas"
        prepend-icon="mdi-message-text"
        append-icon="mdi-send"
        outlided
        multiple
        v-model="files"
        @click:append="processSubtitles"
        >
    </v-file-input>
    </v-form>

     <div class="pills">
            <PillComponent v-for="item in groupedWords" :word="item.word"
            :amount="item.amount" :key="item.word"/>
        
         
        </div>
    </div>
</template>

<script>
import PillComponent from './PillComponent';
const {IpcRenderer} =window.require('electron')
export default {
    name:'HomeComponent',
    components:{ PillComponent},
    data:function(){
        return{
            files:[],
            groupedWords: [
            {word:'i',amount:547},
                {word: 'it', amount:300},            
                {word: 'do', amount:100}, {word:'i',amount:547},
            
              ]      
        }
    },
    methods:{
        processSubtitles(){
            IpcRenderer.send("blabla", "alo")
            console.log(this.files)

        }
    }

    
    

        
    }
</script>

<style>
.home{
    margin: 20px;
}


.pills{
    display:flex;
    flex-wrap:wrap;
    justify-content:center;

}
</style >
