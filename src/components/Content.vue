<template>
  <aside class="lg-side">
    <div class="inbox-head">
      <h3>{{ curentView.title }}</h3>
    </div>

    <keep-alive>
        <component :is="curentView.tag"></component>
      </keep-alive>
  </aside>

</template>

<<script>
  import Inbox from './Inbox'
  import Sent from './Sent'
  import Important from './Important'
  import Trash from './Trash'
  import ViewEmail from './ViewEmail'
  import { eventBus } from '../main'

  export default {
    created () {
      eventBus.$on('changeView', (data) => {
        let temp = [{
          tag: data.tag,
          title: data.title
        }]
        this.history = temp.concat(this.history.splice(0))
      })
    },

    data () {
      return {
        history: [
          {
            tag: 'app-inbox',
            title: 'Inbox'
          }
        ]
      }
    },

    computed: {
      curentView () {
        return this.history[0]
      }
    },
    components: {
      appInbox: Inbox,
      appSent: Sent,
      appImportant: Important,
      appTrash: Trash,
      appViewEmail: ViewEmail
    }
  }
</script>

<style scoped>
.inbox-head {
  background: none repeat scroll 0 0 #41cac0;
  color: #fff;
  height: 90px;
  padding: 20px;
}

.inbox-head h3 {
  display: inline-block;
  font-weight: 300;
  margin: 0;
  padding-top: 12px;
}

</style>


