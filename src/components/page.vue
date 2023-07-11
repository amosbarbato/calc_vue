<script>

</script>


<template>
    <div class="container">
        
        <div class="row">
            <div class="col-md-6">##</div>
            <div class="col-md-6">
                <div class="calculator">
                    <div class="content">
                        <div class="calc-num">
                            <label class="calc-header">Digite um número</label>
                            <input v-model="num1" type="number" placeholder="Digite aqui">
                        </div>
                        <div class="calc-operator">
                            <button value="+" class="oper-toggle" @click="toggle">+</button>
                            <button value="-" class="oper-toggle" @click="toggle">-</button>
                            <button value="*" class="oper-toggle" @click="toggle">x</button>
                            <button value="/" class="oper-toggle" @click="toggle">/</button>
                        </div> 
                        <div class="calc-num">
                            <label class="calc-header">Digite um número</label>
                            <input v-model="num1" type="number" placeholder="Digite aqui">
                        </div>
                        <div class="calc-result">
                            <h6 class="calc-header">
                                Resultado: {{ result }}
                            </h6>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
    .container {
        margin: 100px auto;
        background-color: white;
        border-radius: 20px;
    }
    .calculator {
        border-radius: 15px;
        margin: 30px 18px 30px 0;
        padding: 40px;
        background-color: #004749;
    }
    .calc-num {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 25px;
    }
    .calc-num label {
        color: white;
    }
    .calc-operator {
        display: flex;
        justify-content: space-between;
        gap: 15px;
        margin-bottom: 25px;
    }

    .calc-result{
        background-color: #26C1AF;
        color: #013e41;
        font-weight: 700;
        text-align: center;
        border: none;
        border-radius: 8px; 
        padding: 15px;
        outline: none;
    }

    .calc-result h6 {
        margin: 0;
        text-transform: uppercase;
    }
</style>