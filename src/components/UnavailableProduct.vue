<script>
export default {
    name: 'UnavailableProduct',
    props: {
        nextFunction: { type: Function, required: true },
    },
};
</script>

<template>
    <div class="img-wrapper">
        <img src="../assets/sad-face.svg" alt="Sad Face" />
    </div>
    <div class="wrapper">
        <p>This product is unavailable to show</p>
        <button @click="nextFunction">Next Product</button>
    </div>
</template>

<style scoped>
img {
    width: 100%;
}

.img-wrapper {
    display: flex;
    position: absolute;
    width: 100%;
    justify-content: center;
    align-items: center;
    height: 23rem;
    z-index: -10;
}

.wrapper {
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 1rem;
    height: 23rem;
}

p {
    font-size: 0.9rem;
}

button {
    background-color: transparent;
    border: 2px solid black;
    cursor: pointer;
    font-weight: 500;
}

button:hover {
    background-color: black;
    color: white;
    transition: all 100ms;
}
</style>
