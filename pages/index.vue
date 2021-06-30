<template>
  <div>
    <section class="wrapperForVideo">
      <div>
        <pre>
       Extreme 
                  Sport</pre
        >
      </div>

      <video muted autoplay loop src="../assets/media/Motocross.mp4"></video>
    </section>
    <section class="kindsOfSport">
      <div class="heading">We offer ...</div>

      <div class="defaultKindBlock" v-for="kind in kinds" :key="kind.id">
        <img :src="require('@/assets/images/' + kind.img)" />
        <div class="wrapperForInfo">
          <div>
            <span class="specialSymbol">&#9883;</span>
            <span class="headerSpan">{{ kind.title }}</span
            ><br />
            <span class="contentSpan">{{ kind.text }}</span>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      kinds: [
        {
          id: 1,
          text:
            "Some might not consider scuba diving to be an extreme sport. But think about it, you’re 100+ feet underwater and the only thing keeping you alive is that tank of oxygen strapped to your back. Not to mention all of the creatures lurking below… pretty intense.",
          title: "SCUBA DIVING",
          img: "scuba.png"
        },
        {
          id: 2,
          text:
            "Also known as dirtboarding and offroad boarding, mountain boards take on all types of terrain, and are sometimes used to do tricks or even downhill races. Kind of a cross between skateboarding and snowboarding.",
          title: " MOUNTAIN BOARDING",
          img: "mountain.png"
        },
        {
          id: 3,
          text:
            "Wakeboarding and water skiing are very popular water sports, typically done at the recreational level. But, some take these sports to a whole new level, throwing fancy maneuvers and jumping the boat’s wake to do tricks in the air.",
          title: "WAKEBOARDING / WATER SKIING",
          img: "water.png"
        },
        {
          id: 4,
          text:
            "Also known as kitesurfing and kiteboarding. All you need is wind, a board and a big kite to harness into. On water, on sand, or on snow… it’s is a rush. Just hope a giant gust of wind doesn’t take you away.",
          title: "KITING",
          img: "kitting.png"
        },
        {
          id: 5,
          text:
            "Many probably think parasailing is just a relaxing tourist activity at the beach. But, when you’re being pulled by a piece of rope hundreds of feet above the water, the adrenaline rush definitely kicks in.",
          title: "PARASAILING",
          img: "paras.png"
        },
        {
          id: 6,
          text:
            "There are varying degrees of skateboarding, but here’s the bottom line. Every skateboarder works to improve their skills, adding more difficult tricks every time. Crashing onto the pavement is to be expected, and getting back up to try it again is part of the process.",
          title: "SKATEBOADING",
          img: "skate.png"
        }
      ]
    };
  }
};
</script>
<style lang="scss">
img {
  pointer-events: none;
}
.mainWrapper {
  height: 100%;
  width: 100%;

  .heading {
    text-align: center;
    font-family: "AlFresco";
    font-size: 60px;
  }
}
.wrapperForVideo {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0px 0px 0px 100px;
  border-bottom: solid 1px #c3c8cb;
  div {
    padding-right: 30px;
    pre {
      font-family: "AlFresco";
      font-size: 100px;
      color: rgb(68, 67, 67);
    }
  }

  video {
    width: 50%;
    position: relative;
    object-fit: cover;
  }
}
.kindsOfSport {
  padding: 50px 10px;
  width: 100%;

  .heading {
    text-align: center;
    font-family: "AlFresco";
    font-size: 60px;
  }

  .defaultKindBlock {
    position: relative;
    display: inline-flex;
    padding-top: 20px;
    width: 50%;
    flex-wrap: nowrap;
    img {
      width: 25%;
      border-radius: 5%;
      opacity: 0.65;
    }

    .wrapperForInfo {
      display: flex;
      align-items: center;
      padding-left: 10px;
      .specialSymbol {
        position: relative;
      }
      .headerSpan {
        text-transform: none;
        position: relative;
        margin-left: 6px;
      }
      .contentSpan {
        display: block;
        padding-top: 7px;
        width: 80%;
        line-height: 180%;
      }
      span {
        opacity: 0.7;
        position: relative;
        margin: auto;
        font-family: "EB Garamond", serif;
      }
    }
  }
}
</style>
