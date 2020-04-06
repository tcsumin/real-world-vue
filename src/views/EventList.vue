<template>
  <div>
    <h1>Event Listing</h1>
    <EventCard v-for="event in events" :key="event.id" :event="event" />
    <!-- <p>
      <router-link :to="{ name: 'event-show', params: { id: '1' } }">
        First Event
      </router-link>
    </p> -->
  </div>
</template>

<script>
import EventCard from '@/components/EventCard.vue'
// import axios from 'axios' // brings in the axios library
import EventService from '@/services/EventService.js'

export default {
  components: {
    EventCard,
  },
  created() {
    // axios
    //   .get('http://localhost:3000/events') // does a get request
    //   .then((res) => {
    //     // console.log(res.data) // for now, log the response
    //     this.events = res.data // set the events when returned
    //     // console.log(this.events)
    //   })
    //   .catch((err) => {
    //     console.log('There was an error', err.message) // log the error
    //   })
    EventService.getEvents(this.id)
      .then((res) => {
        this.events = res.data
      })
      .catch((err) => {
        console.log('There was an error', err.message)
      })
  },
  data() {
    return {
      events: [],
    }
  },
}
</script>
