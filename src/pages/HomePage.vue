<template>

</template>

<script>
import { onMounted } from "vue"
import {giftsService} from '../services/GiftsService.js'
import Pop from "../utils/Pop.js"

export default {
  setup() {
onMounted(() => getGifts())


async function getGifts(){
try {
  await giftsService.getGifts()
} catch (error) {
Pop.error(error)
}
}

    return {}
  }
}
</script>

<style scoped lang="scss">
</style>
