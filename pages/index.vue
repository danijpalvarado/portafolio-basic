<script setup lang="ts">
const { data: posts } = await useAsyncData('latest-posts', () =>
  queryContent('/blog')
    .sort({ data: 1 })
    .limit(3)
    .find()
)
</script>

<template>
  <section>
    <h1 class="text-5xl font-bold mt-20">👋🏻 Hello, I'm Dani JP!</h1>
    <p class="text-base text-gray-900 p-2 italic">Developer JR</p>
  </section>
  <section class="flex flex-col md:flex-row">
    <div class="md:w-3/4">
      <h2 class="text-3xl font-bold mt-8">My Story</h2>
      <p class="text-lg py-2">
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sit, nesciunt excepturi. Fugit labore repellat temporibus! Incidunt libero deleniti impedit. Cupiditate facilis quod, ab aut iste ipsum molestiae reprehenderit voluptates pariatur qui repudiandae repellendus. Iure ut laboriosam obcaecati non earum ipsam architecto neque sit quae. Quae pariatur, labore doloribus eum, ex saepe voluptatum quas ipsam officia, numquam nobis tempora! Amet incidunt rerum dolores laborum perspiciatis saepe ipsum facere, corporis iusto atque iure natus in sint ut provident fugiat suscipit velit repudiandae consequatur nisi veritatis quas voluptate? Quidem distinctio adipisci ab, inventore, vel aperiam quaerat recusandae vitae nam nemo quis eius quasi.
    </p>
      <p class="text-lg py-2">
        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Itaque officia nostrum quisquam voluptatum omnis dolorum ipsum mollitia, a ex magnam, et tempora, maxime perferendis voluptatem necessitatibus repellat nihil incidunt magni ea aliquam rem repellendus id aut. Fuga recusandae numquam enim nisi quod quaerat nobis veniam perspiciatis ab iure cum nulla, aperiam, eveniet ad facilis pariatur quas possimus ratione animi saepe dolorem eius iste. Deleniti accusantium mollitia deserunt maxime fuga voluptates assumenda facilis adipisci numquam eius voluptatum facere culpa rerum quam nesciunt cumque id quibusdam repellendus cum omnis voluptatem cupiditate, illum, autem ex. Voluptatem ab vero quis culpa officia facilis dolorum. Veritatis, accusamus tempora omnis incidunt et quo ipsa aperiam nobis. Dicta modi suscipit ex excepturi commodi eum facere architecto repellat a, quis esse. Dicta alias deleniti modi sapiente rem suscipit pariatur, itaque eaque nisi, incidunt, sunt aperiam fuga omnis quam explicabo ut laboriosam! Culpa, modi eveniet ipsum dolorum hic ab.
      </p>
      <p class="text-lg py-2">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Laudantium culpa porro facilis quibusdam ea, cum id soluta asperiores quae impedit, debitis tempore voluptatem omnis harum. Laudantium rerum facilis saepe mollitia nesciunt dolorem, quidem alias quos! In distinctio veniam quidem mollitia optio eligendi ipsum explicabo itaque cum nemo temporibus et perferendis voluptatibus pariatur illo modi provident suscipit hic, corporis ea placeat!
      </p>
    </div>
    <img src="~/assets/images/freelancer.png" class="w-1/2 object-contain md:max-w-sm p-8 mx-auto" />
  </section>

  <section>
    <h2 class="text-3xl font-bold mt-8">Latest Blog Posts</h2>
    <div class="grid md:grid-cols-3 pt-8 gap-10 mb-20">
      <Post :posts="posts" />
    </div>
  </section>
</template>