<template>
<div class="pill">
    <span class="word">{{ word }}</span>
    <span class="amount">{{ amount }}</span>
</div>
</template>

<script>
export default {
    name: 'PillComponent',
    props:['word', 'amount']

}
</script>

<style scoped>

.pill{
    margin:10px;
    height: 55px;
    border-radius:35px;
    color:#ffffff;
    font-size:1.3rem;
    font-weight: bold;
    display:flex;
    align-items: center;
    background-color: red;
    width:fit-content

}

.pill .word{
    margin-left: 15px;
}

.pill .amount{
    margin:10px;
    height: 40px;
    border-radius:50%;
    color:red;
    width: 40px;
    margin:10px;
    padding: 4px;
    font-size:1.3rem;
    justify-content: center;
    display:flex;
    align-items: center;
    background-color: #ffffff;


}
</style>