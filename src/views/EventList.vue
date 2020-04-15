<template>
  <div>
    <h1>Events Listing</h1>
    <EventCard v-for="event in events" :key="event.id" :event="event"></EventCard>
    <BaseIcon></BaseIcon>
  </div>
</template>

<script>
  import EventCard from "../components/EventCard";
  import EventService from '../services/EventService';

  export default {
    components: {
      EventCard
    },
    data() {
      return {
        events: [],
      }
    },
    created() {
      EventService.getEvents()
        .then(response => {
          console.log('RESPONSE', response.data);
          this.events = response.data;
        })
        .catch(error => {
          console.log('ERROR',error);
        })
    }

  }
</script>

