<script setup lang="ts">
const { data: posts } = await useAsyncData('posts', () =>
  queryContent('/blog').find()
)
</script>

<template>
  <h1 class="text-3xl my-8">Blog Posts</h1>

  Lorem ipsum dolor sit amet consectetur adipisicing elit. Laboriosam exercitationem vitae possimus 
  non consequatur laudantium vero in nobis dolorum expedita amet porro quod alias voluptatum pariatur, 
  asperiores nesciunt qui dolorem magni ullam optio modi sint beatae molestiae? Officiis dignissimos ipsum 
  beatae a cupiditate eligendi libero quisquam aperiam animi optio at quos dicta blanditiis fugit dolore 
  reiciendis odit laudantium totam repellat tenetur, possimus sapiente illo. Voluptatum sequi quo sapiente 
  animi unde recusandae dolorum voluptate dolor suscipit impedit doloribus consequuntur saepe non officia 
  <section class="grid md:grid-cols-3 mt-8 gap-10 mb-20">
    <Post :posts="posts" />
  </section>
</template>