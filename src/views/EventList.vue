<template>
  <div>
    <h1>Events Listing</h1>
    <EventCard></EventCard>
    <BaseIcon></BaseIcon>
  </div>
</template>

<script>
  import EventCard from "../components/EventCard";

  export default {
    components: {
      EventCard
    }

  }
</script>