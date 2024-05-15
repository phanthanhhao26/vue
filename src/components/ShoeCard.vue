<script setup>

</script>

<template>
    <div>
        <div class="border-2 rounded-xl border-red-400 border-transparent
            cursor-pointer max-sm:flex-1">
            <div class="flex justify-center items-center bg-card bg-center
                bg-cover sm:w-40 sm:h-40 rounded-xl max-sm:p-4">
                <img
                    :src="item.thumbnail"
                    alt="shoe collection"
                    width="127"
                    height="103"
                >
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props: {
            item: {
                type: Object,
                required: true
            }
        }
    }
</script>