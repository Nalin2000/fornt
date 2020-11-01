<template>
  <v-container>
    <v-row
      ><v-col v-for="(i, index) in list" :key="index" cols="3">
        <v-card
          class="btn-room nav--text text-center"
          width="100"
          height="100"
          :color="state(index)"
        >
          <br /><b> ROOM {{ i.roomNo }}</b> <br />{{ i.state }}
        </v-card>
      </v-col></v-row
    ></v-container
  >
</template>

<script>
import { db } from '~/plugins/firebaseConfig.js'
export default {
  data() {
    return { list: [] }
  },
  mounted() {
    this.getdata()
  },
  methods: {
    getdata() {
      db.collection('room')
        .orderBy('roomNo', 'asc')
        .onSnapshot((querySnapshot) => {
          const data = []
          querySnapshot.forEach((doc) => {
            data.push(doc.data())
          })
          this.list = data
          console.log(this.list)
        })
    },
    state(index) {
      if (this.list[index].state === 'wait check in') {
        return '#eebd6b'
      } else if (this.list[index].state === 'available') {
        return '#57BDA2'
      } else {
        return '#d5d1ca'
      }
    },
  },
}
</script>
