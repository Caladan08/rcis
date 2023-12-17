<script lang="ts">
  import { Carousel, Indicator } from "flowbite-svelte";

  const images = [
    {
      alt: "test",
      src: "https://rcis.in/wp-content/uploads/2023/11/banner-001-painting-1920x1080-1.jpg",
      title: "test"
    },
    {
      alt: "test2",
      src: "https://rcis.in/wp-content/uploads/2023/11/banner-science-lab-1920x1080-003.jpg",
      title: "test2"
    },
    {
      alt: "test2",
      src: "https://rcis.in/wp-content/uploads/2023/11/banner-001-fully-carpeted-terrace-for-sports-1920x1080-1.jpg",
      title: "test2"
    },
    {
      alt: "test2",
      src: "https://rcis.in/wp-content/uploads/2023/11/banner-003-robotics-1920x1080-2.jpg",
      title: "test2"
    },
    {
      alt: "test2",
      src: "https://rcis.in/wp-content/uploads/2023/11/banner-m-001-amphitheater-1920x1080-1.jpg",
      title: "test2"
    },
  ]
</script>

<div class="wrapper">
  <Carousel {images} duration={3000} let:Controls let:Indicators>
    <Controls />
    <Indicators />
  </Carousel>
</div>

