<script>
export default {
    name: 'ProductSkeleton',
};
</script>

<template>
    <div class="loading">
        <div class="img-box"></div>
        <div class="detail-wrapper">
            <div class="text-wrapper">
                <div class="title"></div>
                <div class="description">
                    <div></div>
                    <div></div>
                    <div></div>
                    <div></div>
                </div>
            </div>
            <div class="btn-wrapper">
                <div></div>
                <div></div>
            </div>
        </div>
    </div>
</template>

<style scoped>
@import url(../assets/style/page.css);

.loading {
    display: flex;
    gap: 3rem;
    align-items: center;
    height: 23rem;
}

.img-box {
    background-color: var(--light-grey);
    height: 100%;
    flex-basis: 35%;
    border-radius: 0.5rem;
    animation: pulse 2s cubic-bezier(0.4, 0, 0.6, 1) infinite;
}

.detail-wrapper {
    display: flex;
    justify-content: space-between;
    flex-grow: 1;
    height: 100%;
    animation: pulse 2s cubic-bezier(0.4, 0, 0.6, 1) infinite;
}

.text-wrapper {
    display: flex;
    flex-direction: column;
    gap: 1rem;
}

.title {
    background-color: var(--light-grey);
    width: 100%;
    height: 1.2rem;
    border-radius: 20rem;
}

.description {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
}

.description > div {
    height: 0.8rem;
    background-color: var(--light-grey);
    border-radius: 20rem;
}

.btn-wrapper {
    display: flex;
    gap: 1rem;
}

.btn-wrapper > div {
    width: 50%;
    height: 2rem;
    background-color: var(--light-grey);
    border-radius: 5px;
    -webkit-border-radius: 5px;
    -moz-border-radius: 5px;
    -ms-border-radius: 5px;
    -o-border-radius: 5px;
}

@keyframes pulse {
    0%,
    100% {
        opacity: 1;
    }
    50% {
        opacity: 0.5;
    }
}
</style>
