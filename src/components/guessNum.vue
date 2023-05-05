<script>
export default {
    data(){
        return{
            ans:Math.floor(Math.random()*100)+1,
            title:"請猜一個數字",
            show:"1-100",
            guess:null,
            max:100,
            min:1,
            isAns: true
        }
    },
    methods:{
        fn(){
            if(this.guess > this.max || this.guess < this.min){
                this.title = "請猜 正確範圍 的數字";
            }
            if(this.guess > this.ans && this.max > this.guess){
                this.max = this.guess;
                this.show = this.min + "-" + this.max;
                this.title = "繼續猜";
            }
            if(this.guess < this.ans && this.min < this.guess){
                this.min = this.guess;
                this.show = this.min + "-" + this.max;
                this.title = "繼續猜";
            }
            if(this.guess === this.ans){
                this.show ="答對了!!!";
                alert("恭喜你");
            }
            this.guess=null;
        }

    },
    mounted(){

    }
}
</script>

<template>  
<div class="area">
    <h1 class="title">{{title}}</h1>
    <p>{{ show }}</p>
    <input type="number" v-model="guess">
    <button type="button" v-on:click="fn">click</button>
    <!-- button type="button" class="btn" @click="fn" -->


    <!-- <div v-if="isAns">答對
        <p>

        </p>
    </div>
    <div v-else>答錯</div> -->
</div>

</template>

<style lang="scss" scoped>
.area{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-around;
    width: 50%;
    height: 300px;
    background-color: rgb(122, 246, 246, 0.6);
    border-radius: 20px;
    box-shadow: 5px 5px 5px rgb(0, 0, 0);

    p{
        font-size: 20pt;
    }
}
</style>