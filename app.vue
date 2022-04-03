<template>
  <div>
    <component :is="contentComponent" />
  </div>
</template>

<script>
export default {
  computed: {
    contentComponent() {
      return {
        name: 'DynamicComponent',
        template: `<hello msg="Welcome to nuxt3!" />
        This is a nuxt3 protype to render custom elements.
        It works great and handles encoding of special chars just fine:
        <hello msg="It&#39;s a great day! &#60;1000&#8364;&#62;" />
        `,
      };
    },
  },
};
</script>
