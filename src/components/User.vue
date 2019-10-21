<template>
  <div>
    <b-list-group>
      <b-list-group-item>
        {{ user.id }}.- {{ user.attributes.name }}
        {{ user.relationships.articles }}
      </b-list-group-item>
    </b-list-group>
  </div>
</template>

<script>
export default {
  props: ["user"]
};
</script>