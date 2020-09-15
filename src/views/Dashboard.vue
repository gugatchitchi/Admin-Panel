<template>
  <div class="dashboard">
    <PanelHeader :name="'Dashboard'" />
    <ColorfulBlock :color="'#3d8be3'" :name="'Revenue LM'" :value="100000" />
    <ColorfulBlock :color="'#26A243'" :name="'Profit LM'" :value="35000" />
    <ColorfulBlock :color="'#F7BB09'" :name="'Cogs LM'" :value="65000" />
    <ColorfulBlock :color="'#D53343'" :name="'Salaries LM'" :value="1000" />
  </div>
</template>

<script>
import PanelHeader from '@/components/PanelHeader.vue'
import ColorfulBlock from '@/components/ColorfulBlock.vue'
export default {
  name: 'Dashboard',
  components: {
    PanelHeader,
    ColorfulBlock,
  },
}
</script>

<style scoped>
h1 {
  color: black;
}
</style>
