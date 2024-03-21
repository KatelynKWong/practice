<script>
  import { fly } from "svelte/transition";
  import { crossfade } from 'svelte/transition';
  import { tweened } from "svelte/motion";
  import coffeePlant from './assets/coffee-g5e25637ad_1920.webp';
  import earthquakeClipart from './assets/earthquake_image.jpg';
  import sfEarthquake from './assets/sf_earthquake.png';
  import tsunamiImage from './assets/tsunami.jpg';
  import cloudImage from './assets/clouds.png';
  import japanEarthquake from './assets/japanEarthquake.jpg';
  export let index, width, height;

  // Define the intro block
  const tweenedTitleImageOpacity = tweened(0);
  const tweenedAboutMeOpacity = tweened(0)

  // Intro block animations
  $: {
    // reset positions when we are at top
    if (index === 0) {
      tweenedTitleImageOpacity.set(1);
    }
    if (index === 1) {
      tweenedTitleImageOpacity.set(1);
      tweenedAboutMeOpacity.set(0)
    }
  }

  // Create tweened variables for background story
  const tweenedCloudOpacity = tweened(0)
  const tweenedCloudY = tweened(0)
  const tweenedbackgroundIntroOpacity = tweened(0);
  const tweenedStory1Opacity = tweened(0);
  const tweenedStory1Y = tweened(0);
  tweenedStory1Y.set(height*1.5)
  const introImageOpacity = tweened(0)
  introImageOpacity.set(0)
  const tweenedRectOpacity = tweened(0)
  tweenedRectOpacity.set(0)
  
  const tweenedStory2Opacity = tweened(0);
  const tweenedStory2Y = tweened(0);
  tweenedStory1Y.set(height*1.5)
  const tweenedStory3Opacity = tweened(0);
  const tweenedStory3Y = tweened(0);
  const tweenedStory4Opacity = tweened(0);
  const tweenedStory4Y = tweened(0);
  const tweenedStory5Opacity = tweened(0);
  const tweenedStory5Y = tweened(0);
  const tweenedStory6Opacity = tweened(0);
  const tweenedStory6Y = tweened(0);
  const tweenedStory7Opacity = tweened(0);
  const tweenedStory7Y = tweened(0);
  const tweenedStory8Opacity = tweened(0);
  const tweenedStory8Y = tweened(0);
  const tweenedjapanEarthquakeOpacity = tweened(0)
  const tweenedStory9Opacity = tweened(0);
  const tweenedStory9Y = tweened(0);
  const tweenedStory10Opacity = tweened(0);
  const tweenedStory10Y = tweened(0);
  const tweenedStory11Y = tweened(0);
  const tweenedStory11Opacity = tweened(0);
  const tweenedStory12Y = tweened(0);
  const tweenedStory12Opacity = tweened(0);
  const tweenedStory13Y = tweened(0);
  const tweenedStory13Opacity = tweened(0);

  $: { // background story animations
    if (index === 2) {
      tweenedRectOpacity.set(0)
      tweenedAboutMeOpacity.set(1)
    }
    if (index === 3) {
      tweenedAboutMeOpacity.set(0)
      tweenedRectOpacity.set(.5)
      tweenedCloudOpacity.set(0)
      tweenedCloudY.set(height*1.5)
    }
    if (index === 4) {
      tweenedbackgroundIntroOpacity.set(1)
      tweenedStory1Y.set(height*1.5)
      introImageOpacity.set(0)
      tweenedRectOpacity.set(1)
      tweenedCloudOpacity.set(.3)
      tweenedCloudY.set(-height/3)

     } else {
      tweenedbackgroundIntroOpacity.set(0)
    }
    if (index === 5) {
      tweenedStory1Opacity.set(1)
      tweenedStory1Y.set(height/2)
      tweenedStory2Y.set(height*1.5)
      introImageOpacity.set(1)
      tweenedRectOpacity.set(.5)
      tweenedCloudOpacity.set(0)
      tweenedCloudY.set(-height)

    } else {
      tweenedStory1Opacity.set(0)
    }
    if (index === 6) {
      tweenedStory2Opacity.set(1)
      tweenedStory1Y.set(-20)
      tweenedStory2Y.set(height/2)
      tweenedStory3Y.set(height*1.5)
      introImageOpacity.set(1)
      tweenedRectOpacity.set(.5)
    } else {
      tweenedStory2Opacity.set(0)
    }
    if (index === 7) {
      tweenedStory3Opacity.set(1)
      tweenedStory2Y.set(-20)
      tweenedStory3Y.set(height/2)
      tweenedStory4Y.set(height/2)
      introImageOpacity.set(0)
      tweenedRectOpacity.set(0)
      tweenedjapanEarthquakeOpacity.set(0)
    } else {
      tweenedStory3Opacity.set(0)
    }
    if (index === 8) {
      tweenedStory4Opacity.set(1)
      tweenedStory3Y.set(-20)
      tweenedStory5Y.set(height/2)
      tweenedjapanEarthquakeOpacity.set(.75)

    } else {
      tweenedStory4Opacity.set(0)
    }
    if (index === 9) {
      tweenedStory5Opacity.set(1)
      tweenedStory6Y.set(height/2)
      tweenedjapanEarthquakeOpacity.set(0)
    } else {
      tweenedStory5Opacity.set(0)
    }
    if (index === 10) {
      tweenedStory6Opacity.set(1)
      tweenedStory8Y.set(-20)
    } else {
      tweenedStory6Opacity.set(0)
    }
    if (index === 11) {
      tweenedStory7Opacity.set(1)
      tweenedStory7Y.set(height/2)
    } else {
      tweenedStory7Opacity.set(0)
    }
    if (index === 12) {
      tweenedStory8Opacity.set(1)
      tweenedStory7Y.set(-20)
      tweenedStory8Y.set(height/2)
    } else {
      tweenedStory8Opacity.set(0)
    }
    if (index === 13) {
      tweenedStory9Opacity.set(1)
      tweenedStory8Y.set(-20)
      tweenedStory9Y.set(height/2)
    } else {
      tweenedStory9Opacity.set(0)
    }
    if (index === 14) {
      tweenedStory10Opacity.set(1)
      tweenedStory9Y.set(-20)
      tweenedStory10Y.set(height/2)
    } else {
      tweenedStory10Opacity.set(0)
    }
    if (index === 15) {
      tweenedStory11Opacity.set(1)
      tweenedStory10Y.set(-20)
      tweenedStory11Y.set(height/2)
    } else {
      tweenedStory11Opacity.set(0)
    }
    if (index === 16) {
      tweenedStory12Opacity.set(1)
      tweenedStory11Y.set(-20)
      tweenedStory12Y.set(height/2)
    } else {
      tweenedStory12Opacity.set(0)
    }
    if (index === 17) {
      tweenedStory13Opacity.set(1)
      tweenedStory12Y.set(-20)
      tweenedStory13Y.set(height/2)
    } else {
      tweenedStory13Opacity.set(0)
    }
  }

</script>
<svg class="graph" width="100%" height="100%" y="0">
  <!-- Title image layer with fly transition -->
  <image
    x="0" y="0" width="100%" height="100%"
    xlink:href={coffeePlant}
    opacity={$tweenedTitleImageOpacity}
    in:fly={{ opacity: 1, duration: 1000 }}
    out:fly={{ opacity: 0, duration: 1000 }}
    preserveAspectRatio="xMidYMid slice"
  />

  <!-- Text layers -->
  {#if index > 0}
  <!-- intro text -->
  <rect 
  width="520" 
  height="320" 
  x="20%" 
  y="35%" 
  rx="20" 
  ry="20" 
  fill="white" 
  opacity={$tweenedAboutMeOpacity *3/4}
/>

<text class = "aboutme"
  x="5%"
  y="40%"
  text-anchor="left"
  opacity={$tweenedAboutMeOpacity}
  in:fly={{ y: -300, duration: 1000 }}
  out:fly={{ y: -300, duration: 1000 }}
>
  <tspan x="25%" dy="0%">About the author ...</tspan>
  <tspan x="25%" dy="1.8em">minutes, the aftermath of an earthquake can be felt for</tspan>
  <tspan x="25%" dy="1.8em">weeks to years globally. Earthquakes can displace people from</tspan>
  <tspan x="25%" dy="1.8em">their homes and destroy livelihoods in an instant, ultimately</tspan>
  <tspan x="25%" dy="1.8em">impacting society, the economy, and climate. For example,</tspan>
  <tspan x="25%" dy="1.8em">the Great East Japan Earthquake in 2011 caused an economic</tspan>
  <tspan x="25%" dy="1.8em">loss of $360 billion alone. As such, repairing damages</tspan>
  <tspan x="25%" dy="1.8em">caused by earthquakes can be extremely costly.</tspan>
</text>

    <rect class="grey-rectangle"
    width="100%"  
    height="100%" 
    x="0"
    y="0"
    fill="grey"
    opacity={$tweenedRectOpacity}
    in:crossfade={{ duration: 1000 }}
    out:crossfade={{ duration: 1000 }}
  />

    <image class="clouds"
    x={-width/4} y={-height*5/12} width="150%" height="150%"
    xlink:href={cloudImage}
      opacity={$tweenedCloudOpacity}
      in:crossfade={{ duration: 1000 }}
      out:crossfade={{ duration: 1000 }}
    />


    <!-- background text -->
    <text class="backgroundIntro"
      x="50%"
      y="50%"
      text-anchor="middle"
      opacity={$tweenedbackgroundIntroOpacity}
      in:fly={{ y: -300, duration: 1000 }}
      out:fly={{ y: -300, duration: 1000 }}
    >
      <tspan x="50%" dy="-0.6em">On April 18, 1906</tspan>
      <tspan x="50%" dy="1.8em">at 5:12am in the morning...</tspan>
    </text>

    <image class="introImage"
    x={width * 0.45} y="0" width={width * 0.55} height="100%"
    xlink:href={sfEarthquake}
      opacity={$introImageOpacity}
      in:crossfade={{ duration: 1000 }}
      out:crossfade={{ duration: 1000 }}
    />

    <text class="backgroundStory1"
      x="10%"
      y={$tweenedStory1Y}
      text-anchor="middle"
      opacity={$tweenedStory1Opacity}
      in:fly={{ y: -300, duration: 1000 }}
      out:fly={{ y: -300, duration: 1000 }}
    >
      <tspan x="22%" dy="-4em">an extreme earthquake measuring 7.9 on the</tspan>
      <tspan x="22%" dy="1.8em">moment magnitude scale struck the Northern </tspan>
      <tspan x="22%" dy="1.8em">coast of California. This earthquake devastated </tspan>
      <tspan x="22%" dy="1.8em">areas ranging from San Francisco to Eureka, </tspan>
      <tspan x="22%" dy="1.8em">causing thousands to die and devastating fires</tspan>
      <tspan x="22%" dy="1.8em">in San Francisco.</tspan>
    </text>

    <text class = 'backgroundStory2'
      x="10%"
      y={$tweenedStory2Y}
      text-anchor="middle"
      opacity={$tweenedStory2Opacity}
      in:fly={{ y: -300, duration: 1000 }}
      out:fly={{ y: -300, duration: 1000 }}
    >      
      <tspan x="22%" dy="-4em">In the aftermath of this earthquake, workers</tspan>
      <tspan x="22%" dy="1.8em">found that more than 3,000 died, over 225,000</tspan>
      <tspan x="22%" dy="1.8em">people became homeless, and over $400 million</tspan>
      <tspan x="22%" dy="1.8em">was lost in property damages. With most of</tspan>
      <tspan x="22%" dy="1.8em">San Francicsco and other parts of the bay</tspan>
      <tspan x="22%" dy="1.8em">destroyed, this fateful event is remembered as</tspan>
      <tspan x="22%" dy="1.8em">the deadliest earthquake in US history.</tspan>
    </text>
    
    <image class="tsunamiImage"
    x={-width*5/12} y="0" width="100%" height="100%"
    xlink:href={tsunamiImage}
      opacity={$tweenedStory3Opacity}
      in:crossfade={{ duration: 1000 }}
      out:crossfade={{ duration: 1000 }}
    />
   
    <text class = 'impactStory1'
      x="90%"
      y={$tweenedStory3Y}
      text-anchor="middle"
      opacity={$tweenedStory3Opacity}
      in:fly={{ y: -300, duration: 1000 }}
      out:fly={{ y: -300, duration: 1000 }}
    >
      <tspan x="78%" dy="-4em">Earthquakes are often labeled as one of the most</tspan>
      <tspan x="78%" dy="1.8em">devastating natural disasters. Not only are they </tspan>
      <tspan x="78%" dy="1.8em">difficult to predict and prepare for compared to</tspan>
      <tspan x="78%" dy="1.8em">other types of natural disasters, earthquakes can</tspan>
      <tspan x="78%" dy="1.8em">also trigger other catestrofic events like tsunamis</tspan>
      <tspan x="78%" dy="1.8em">and fires.</tspan>
    </text>

    <image class="japanEarthquake"
    x="{-width*1/12}" y="0" width="115%" height="115%"
    xlink:href={japanEarthquake}
      opacity={$tweenedjapanEarthquakeOpacity}
      in:crossfade={{ duration: 1000 }}
      out:crossfade={{ duration: 1000 }}
    />
   
    

  {/if}
</svg>

<style>
  @import url('https://fonts.google.com/share?query=playfair');
  svg {
    font-family: 'Playfair Display';
    font-size: 20px;
  }

  .title {
    font-size: 40px;
    font-weight: 500;
    position: absolute;
  }

  .subtitle {
    font-size: 20px;
  }

  .backgroundStory1 {
    white-space: pre-wrap;
  }

  .graph {
    width: 100%;
    height: 100%;
    top: 0;
    position: absolute;
  }
</style>
