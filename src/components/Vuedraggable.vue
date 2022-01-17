<template>
  <div>
    <div class="content">
      <!-- 左侧-->
      <draggable class="content-draggable" v-model='list1' :options="{group:'people',animation:500}" style="margin-left: 0;">
        <div v-for='i in list1' :key='i.id' class='dragItem'>{{ i.name }}</div>
      </draggable>

      <!-- 中间-->
      <draggable class="content-draggable" v-model='list2' :options="{group:'people',animation:500}">
        <div v-for='i in list2' :key='i.id' class='dragItem'>{{ i.name }}</div>
      </draggable>

      <!-- 右侧-->
      <draggable class="content-draggable" v-model='list3' :options="{group:'people',animation:500}">
        <div v-for='i in list3' :key='i.id' class='dragItem'>{{ i.name }}</div>
      </draggable>
    </div>
    <button slot="footer" @click="handleAdd">提交</button>
  </div>
</template>
<script>
import draggable from "vuedraggable"

export default {
  components: {
    draggable
  },
  data() {
    return {
      list1: [
        {id: 1, name: 'aaa'},
        {id: 2, name: 'bbb'},
        {id: 3, name: 'ccc'}
      ],
      list2: [
        {id: 4, name: 'ddd'},
        {id: 5, name: 'eee'},
        {id: 6, name: 'fff'}
      ],
      list3: [
        {id: 7, name: 'ggg'},
        {id: 8, name: 'hhh'},
        {id: 9, name: 'iii'}
      ]
    }
  },
  methods: {
    handleAdd(e) {
      console.log(this.list1, this.list2, this.list3);
    }
  }
}
</script>

<style scoped>
.content {
  display: flex;
}

.content-draggable {
  flex: 1;
  border: 1px solid #ddd;
  height: 300px;
  overflow: auto;
  margin-left: 20px;
}

.dragItem {
  height: 40px;
  line-height: 40px;
  cursor: move;
  position: relative;
  display: block;
  padding: 10px 15px;
  margin-bottom: -1px;
  background-color: #fff;
  border: 1px solid #ddd;
}
</style>
