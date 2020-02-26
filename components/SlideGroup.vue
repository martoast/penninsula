<template>
  <div>

    <div>
      <v-sheet
        class="mx-auto"
        max-width="100%"
        height="50%"
      >
        <v-slide-group
          multiple
          show-arrows
          light
        >
          <v-slide-item
            v-for="n in stores"
            :key="n"
            v-slot:default="{ active, toggle }"
          >
            <v-img
              :src="n"
              :input-value="active"
              @click="toggle"
              height="185"
              width="200"
            >

            </v-img>
          </v-slide-item>
        </v-slide-group>
      </v-sheet>
    </div>
  </div>

</template>
<script>
export default {
  data: () => ({
    model: null,
    stores: [
      "https://cdn-us-ec.yottaa.net/555a305b2bb0ac71b9002d22/8da650303f06013513b1026173a6dedd.yottaa.net/v~4b.1a3.0.0/tenantlogos/279.png?yocs=D_H_",
      "https://cdn-us-ec.yottaa.net/555a305b2bb0ac71b9002d22/8da650303f06013513b1026173a6dedd.yottaa.net/v~4b.1a3.0.0/tenantlogos/3661.png?yocs=D_H_",
      "https://cdn-us-ec.yottaa.net/555a305b2bb0ac71b9002d22/8da650303f06013513b1026173a6dedd.yottaa.net/v~4b.1a3.0.0/tenantlogos/2370.png?yocs=D_H_",
      "https://cdn-us-ec.yottaa.net/555a305b2bb0ac71b9002d22/8da650303f06013513b1026173a6dedd.yottaa.net/v~4b.1a3.0.0/tenantlogos/6687.png?yocs=D_H_",
      "https://cdn-us-ec.yottaa.net/555a305b2bb0ac71b9002d22/8da650303f06013513b1026173a6dedd.yottaa.net/v~4b.1a3.0.0/tenantlogos/20592.png?yocs=D_H_",
      "https://cdn-us-ec.yottaa.net/555a305b2bb0ac71b9002d22/8da650303f06013513b1026173a6dedd.yottaa.net/v~4b.1a3.0.0/tenantlogos/8225.png?yocs=D_H_",
      "https://cdn-us-ec.yottaa.net/555a305b2bb0ac71b9002d22/8da650303f06013513b1026173a6dedd.yottaa.net/v~4b.1a3.0.0/tenantlogos/6170.png?yocs=D_H_",
      "https://cdn-us-ec.yottaa.net/555a305b2bb0ac71b9002d22/8da650303f06013513b1026173a6dedd.yottaa.net/v~4b.1a3.0.0/tenantlogos/7614.png?yocs=D_H_"
    ]
  })
};
</script>
