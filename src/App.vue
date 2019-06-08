<template>
  <div id="app">
    <Home />
    <Navigation />
    <Features />
    <SampleWorks />
    <PurchaseBlock />
    <TeamMember />
    <Offer />
  </div>
</template>

<script>
import Home from '@/components/Home/Home';
import Navigation from '@/components/Navigation/Navigation';
import Features from '@/components/Features/Features';
import SampleWorks from '@/components/SampleWorks/SampleWorks';
import PurchaseBlock from '@/components/Purchase/PurchaseBlock';
import TeamMember from '@/components/TeamMember/TeamMember';
import Offer from '@/components/Offer/Offer';

export default {
  name: 'app',
  components: {
    Home ,
    Navigation,
    Features,
    SampleWorks,
    PurchaseBlock,
    TeamMember,
    Offer,
  }
}
</script>

<style>
html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
  padding: 0;
}

:root {
  --main-color: #00A99D;
}

#app {
  font-family: "Raleway", "Arial";
}

</style>
