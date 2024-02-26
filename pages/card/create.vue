<template>
    <div class="space-y-4 h-full">
        <h1 class="text-4xl text-primary-500 font-semibold">Card Forge Title</h1>
        <p class="text-base text-white">Card Forge Description</p>
        <div class="border rounded-2xl h-1/2 w-full flex items-center">
            <div class="border border-green-500 h-[500px] w-full aspect-video">"SAMPLE"</div>
            <ul class="px-4 space-y-4">
                <li class="border border-primary-500 rounded-lg p-2 px-3">
                    <Icon
                        name="mdi:rotate-3d-variant"
                        color="#38bdf8"
                        size="24px"
                    />
                </li>
                <li class="border border-primary-500 rounded-lg p-2 px-3">
                    <Icon
                        name="mdi:rotate-3d"
                        color="#38bdf8"
                        size="24px"
                    />
                </li>
                <li class="border border-primary-500 rounded-lg p-2 px-3">
                    <Icon
                        name="mdi:add"
                        color="#38bdf8"
                        size="24px"
                    />
                </li>
            </ul>
        </div>
    </div>
</template>
