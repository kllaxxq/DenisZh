<script setup>
    import {useRouter} from 'vue-router'
    const router = useRouter()
    const logout = () => {
        localStorage.removeItem('token')
        router.push({ name: 'Login' })
    }
</script>
<template>
  <div>
    <h1>Панель управления (защищено)</h1>
    <p>Вы успешно авторизированы</p>
    <button @click="logout" class="btn-danger">Выйти</button>
  </div>
</template>
<style scoped>
.btn-danger{
    padding: 0.5rem 1rem;
    background: #c62828;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}
</style>