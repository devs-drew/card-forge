<template>
    <div>
        <div class="flex items-center mb-6 space-x-4">
            <h1 class="text-2xl font-semibold font-mono text-[#2d2d3a]">Back-to-Back Card</h1>
            <span
                @click="flip()"
                class="cursor-pointer hover:text-[#00f5fa]"
                >Flip</span
            >
        </div>
        <div class="card">
            <div class="card-inner">
                <div class="card-front">
                    <span class="text-4xl font-semibold font-mono">FRONT</span>
                </div>
                <div class="card-back">
                    <span class="text-4xl font-semibold font-mono">BACK</span>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
const flip = () => {
    document.querySelector('.card-inner').classList.toggle('flipped')
}
</script>

<style lang="postcss" scoped>
.card {
    width: calc(3.37in * 1.5);
    height: calc(2.125in * 1.5);
    transform-origin: center;
    perspective: 1000px;
}
.card-inner.flipped {
    transform: rotateY(-180deg);
}
.card-inner {
    width: 100%;
    height: 100%;
    position: relative;
    transition: transform 0.8s;
    transform-style: preserve-3d;
}
.card-front,
.card-back {
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    border-radius: 12px;
    -webkit-backface-visibility: hidden; /* Safari */
    backface-visibility: hidden;
    @apply flex items-center justify-center shadow-lg;
}

.card-front {
    z-index: 10;
    @apply bg-[#2d2d3a] text-[#00f5fa];
}
.card-back {
    z-index: 20;
    transform: rotateY(180deg);
    @apply text-[#2d2d3a] bg-[#00f5fa];
}
</style>
