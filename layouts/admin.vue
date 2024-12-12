<!-- layouts/admin.vue -->
<template>
  <div class="admin-layout">
    <header>
      <!-- Header ของ admin -->
      <h1>Admin Header</h1>
    </header>
    <main>
      <!-- ส่วนที่จะแสดงเนื้อหาของหน้า -->
      <slot />
    </main>
    <footer>
      <!-- Footer ของ admin -->
      <p>Admin Footer</p>
    </footer>
  </div>
</template>

<script setup>
// หากต้องการทำสิ่งที่เฉพาะเจาะจงสำหรับ layout นี้สามารถทำได้ที่นี่
</script>
