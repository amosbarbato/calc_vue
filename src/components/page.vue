<script>
    export default {
        data() {
            return {
            result: null,
            operand1: 0,
            operand2: 0
            };
        },
        methods: {
            performOperation(operation) {
                switch (operation) {
                    case '+':
                    this.result = this.operand1 + this.operand2;
                    break;
                    case '-':
                    this.result = this.operand1 - this.operand2;
                    break;
                    case '*':
                    this.result = this.operand1 * this.operand2;
                    break;
                    case '/':
                    this.result = this.operand1 / this.operand2;
                    break;
                }
            }
        }
    };
</script>

<template>
    <div class="container px-5 py-5 shadow">       
        <div class="row align-items-center">
            <div class="col-10 col-sm-8 col-lg-6">
                <div class="hero content">
                    <img src="../assets/img/operations-colored-icons-by-Vexels.png" class="d-block pe-4 img-fluid" alt="Bootstrap Themes" width="600" height="500" loading="lazy">
                </div>                
            </div>
            <div class="col-lg-6">
                <div class="calculator">
                    <div class="content">
                        <div class="calc-num">
                            <label class="calc-header">Digite um número</label>
                            <input v-model="operand1" type="number" placeholder="Digite aqui">
                        </div>
                        <div class="calc-num">
                            <label class="calc-header">Digite um número</label>
                            <input v-model="operand2" type="number" placeholder="Digite aqui">
                        </div>
                        <div class="calc-operator">
                            <button @click="performOperation('+')">+</button>
                            <button @click="performOperation('-')">-</button>
                            <button @click="performOperation('*')">x</button>
                            <button @click="performOperation('/')">/</button>
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
        background-color: white;
        border-radius: 20px;
        position:absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%,-50%);
    }
    .calculator {
        border-radius: 15px;
        padding: 40px;
        background-color: var(--dark-primary);
        height: 450px;
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
        margin-top: 138px;
        background-color: var(--secondary);
        color: var(--primary);
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