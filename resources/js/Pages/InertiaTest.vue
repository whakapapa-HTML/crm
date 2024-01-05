<script setup>
import { Link } from '@inertiajs/vue3';
</script>

<template>
Inertiaテスト<br>
<a href="/">aタグ経由</a><br>
<Link href="/">Link経由</Link><br>
<Link :href="route('inertia.index')">名前付きルート</Link><br>
<Link :href="route('inertia.show', {id: 50})">ルートパラメータテスト</Link>
</template>
