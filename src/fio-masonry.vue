<template>
  <div id="masonry-container" :style="{'column-count':howManyToShowInHorizontally}">
    <div v-for="(item, index) in masonryItem" class="item" v-bind:key="index" @click="masontyItemIsClicked(item)">
        <div class="item-image-container">
            <img class="item-image" :src="item.image" alt="*">
        </div>
        <div class="item-text-container">
            <div>
                <span class="item-text-title"> {{item.title}} </span>
            </div>
            <div>
                <span class="item-text-desc"> {{item.desc}} </span>
            </div>
        </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'fio-masonry',
  props: ['items', 'horizontalCount'],
  data: function () {
    return {
        masonryItem: [],
        howManyToShowInHorizontally: ''
    }
  },

  created: function () {
    this.howManyToShowInHorizontally = this.$props.horizontalCount;
    this.masonryItem = this.$props.items;
  },

  methods: {
    masontyItemIsClicked: function (item) {
      this.$emit('clickedItem', item)
    }
  }

}
</script>

<style scoped>
#masonry-container {
  column-gap: 1em;
}

.item {
  background-color: #FFFFFF;
  break-inside: avoid;
  margin: 0 0 1em;
  cursor: pointer;
}

.item:hover {
    transform: scale(1.05);
}

.item-image-container {
  width: 100%;
}

.item-image {
  width:100%;
  height:100%;
}

.item-text-container {
  margin: 10px;
}

.item-text-title {
  font-weight: 600;
  font-size: 14px;
}

.item-text-desc {
  font-size: 12px;
}

</style>
