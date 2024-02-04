<script setup>
import { Inertia } from '@inertiajs/inertia';
defineProps({
  id : String,
  blog: Object
})

const deleteConfirm = id => {
    // console.log(id)
    Inertia.delete(`/inertia/${id}`, {
        onBefore: () => confirm('削除？')
    })
}
</script>

<template>
<div>
  {{ id }} <br>
  {{ blog.title }}
  <button @click="deleteConfirm(blog.id)">削除</button>
</div>

</template>
