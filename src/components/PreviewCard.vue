<template>
  <section :class='backgroundColor' class='preview-card'>
    <article>
      <header>
        <div class='icon'>
          <slot name='headerIcon'></slot>
        </div>

        <h1>
          {{ headerTitle }}
        </h1>
      </header>

      <p class='description text-regular'>
        {{ description }}
      </p>

      <footer>
        <button class='btn btn--primary'>
          <a :href='link' target='_blank'>Learn More</a>
        </button>
      </footer>
    </article>
  </section>
</template>

<script>
export default {
  name: 'PreviewCard',
  props: {
    link: {
      type: String,
      default: ''
    },
    description: {
      type: String,
      default: ''
    },
    headerTitle: {
      type: String,
      default: ''
    },
    backgroundColor: {
      type: String,
      default: ''
    }
  }
};
</script>
