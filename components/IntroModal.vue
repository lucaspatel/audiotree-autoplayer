<template>
    <div v-if="modal.visible" @click.self="modal.visible = false" class="h-screen w-full absolute flex items-center justify-center bg-modal">
        <div class="bg-white rounded shadow p-8 m-4 max-w-xs max-h-full text-center overflow-y-scroll">
            <div class="mb-4">
                <h1>Welcome!</h1>
            </div>
            <div class="mb-8">
                <p>Ready to get started? Keep scrolling to see some great components.</p>
            </div>
            <div class="flex justify-center">
                <button class="flex-no-shrink text-white py-2 px-4 rounded bg-teal hover:bg-teal-dark">Let's Go</button>
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style>

</style>
