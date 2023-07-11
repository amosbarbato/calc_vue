<script>

</script>


<template>
    <div class="container">
        
        <div class="row">
            <div class="col-md-6">##</div>
            <div class="col-md-6">
                <div class="calculator">
                    <div class="content">
                        <input v-model="num1" type="number" placeholder="Digite um número">
                        <select v-model="operator">
                            <option value="+">+</option>
                            <option value="-">-</option>
                            <option value="*">*</option>
                            <option value="/">/</option>
                        </select>
                        <input v-model="num2" type="number" placeholder="Digite um número">
                        <p>Resultado: {{ result }}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
    .container {
        margin: 150px auto;
        background-color: white;
        border-radius: 20px;
    }

    .calculator {
        border-radius: 15px;
        margin: 30px 18px 30px 0;
        padding: 30px;
        background-color: darkslategrey;
    }
</style>