<script>
export default{
    data(){
        return{
            num1:0,
            num2:0,
            calType:"",
            result:0
        }
    },
    methods:{
        count(){
            switch(this.calType){
                case "1":
                    this.result = this.num1 + this.num2;
                    break;
                case "2":
                    this.result = this.num1 - this.num2;
                    break;
                case "3":
                    this.result = this.num1 * this.num2;
                    break;
                case "4":
                    this.result = this.num1 / this.num2;
                    break;
            }
            
        }
    },
    mounted() {
        
    },
}
</script>

<template>
    <div class="calculator">
        <h1>計算機</h1>
        <div class="cal">
            <input class="input" type="number" v-model="num1">
            <select name="" id="" v-model="calType">
                <option value="1">+</option>
                <option value="2">-</option>
                <option value="3">*</option>
                <option value="4">/</option>
            </select>
            <input class="input" type="number" v-model="num2">
            <p>Ans = {{ result }}</p>
        </div>
        <button type="button" v-on:click="count">Cool</button>
    </div>

</template>

<style lang="scss" scoped>
.calculator{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
    width: 50%;
    height: 300px;
    background-color: rgb(122, 246, 246, 0.6);
    border-radius: 20px;
    box-shadow: 5px 5px 5px rgb(0, 0, 0);

    .input{
        margin: 10px 10px;
    }

    p{
        color: white;
    }

    button{
        margin-bottom: 15px;
        border-radius: 5px;

        &:hover{
            background-color: cadetblue;
            transition: 0.6s;
            box-shadow: 3px 3px 3px black;
        }
    }
}
</style>
