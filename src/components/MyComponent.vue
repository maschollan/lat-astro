<template>
    <div>
        <h1>Test Halaman Vue</h1>
        <p>Hasil input : {{ teks }}</p>

        <input type="text" v-model="teks"/>
        <ol>
            <li v-for="h in hobi" :key="h">{{ h }}</li>
        </ol>
    </div>
</template>

<script>
import "../styles/global.css";

export default {
    name: "MyComponent",
    data() {
        return {
            teks: "",
            hobi: ["makan", "tidur", "nyanyi"],
        };
    },
};
</script>
