<template>
  <div class="admin-post-page">
    <section class="update-form">
      <AdminPostForm :post="loadedPost" />
    </section>
  </div>
</template>

<script>
import AdminPostForm from '@/components/Admin/AdminPostForm'

export default {
  components: {
    AdminPostForm,
  },
  data() {
    return {
      loadedPost: {
        author: 'keroken',
        title: 'Hello World!',
        content: 'Hello! This is my awesome blog post!',
        thumbnail:
          'https://federallabs.org/news/white-paper-released-for-if-the-sky-were-the-limit',
      },
    }
  },
}
</script>

<style scoped>
.update-form {
  width: 90%;
  margin: 20px auto;
}
@media (min-width: 768px) {
  .update-form {
    width: 500px;
  }
}
</style>
