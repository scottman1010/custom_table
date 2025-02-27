<script>
export default {
  setup(props) {
    const { id: rowId } = props.params.node;
    const { data, dataType, wwElement, dataPath } = props.params;
    return {
      rowId,
      data,
      dataType,
      wwElement,
      dataPath,
    };
  },
  computed: {
    wwProps() {
      const resolvedData = _.get(this.data, this.dataPath);
      switch (this.dataType) {
        case "text-element":
          return {
            text: resolvedData ?? "",
          };
        case "image-element":
          return {
            url: resolvedData,
          };
        default:
          return undefined;
      }
    },
    shouldRender() {
      switch (this.dataType) {
        case "image-element":
          return Boolean(this.wwProps.url);
        default:
          return true;
      }
    },
  },
}
</script>

<template>
  <wwElement
      v-if="wwElement && wwElement.uid && shouldRender"
      :uid="wwElement.uid"
      :ww-props="wwProps"
  ></wwElement>
</template>

<style scoped lang="scss">
</style>
