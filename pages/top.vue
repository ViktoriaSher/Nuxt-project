<template>
  <div class="mainWrapp">
    <h1>Our top</h1>
    <ol>
      <li v-for="item in topList" :key="item.title">
        <span class="itemTitle">{{ item.title }}</span
        ><br />
        <div class="footerInfoTop">
          <img :src="require('@/assets/images/' + item.img)" />
          <div>{{ item.text }}</div>
        </div>
      </li>
    </ol>
  </div>
</template>
<script>
export default {
  data() {
    return {
      topList: [
        {
          title: "Highlining – for the classic daredevil",
          text:
            "Highlining is an extreme sport that includes a daredevil tightrope walking a thin line between two mountains, buildings or fixed points. Only one-inch in width, the tightrope is usually suspended around 1,000 foot (304 metres) above safe ground. ",
          img: "highlining.png"
        },
        {
          title: "Wing Walking",
          text:
            "Wing walking is yet another extreme sport that takes something already hair-raising and takes it up a notch.This activity earns its way onto our list of extreme sports due to the sheer insanity of it. Wing walking involves someone standing on top of a fast-moving small plane (300 km/200 mph to be specific), as it performs turns and tricks ",
          img: "wind.png"
        },
        {
          title: " Base Jumping – the successor of parachuting",
          text:
            "For those of you who tried parachuting and decided it was simply too boring, there’s always this unusual sport which may just do the trick. Base jumping involves jumping off tall structures, such as bridges, cliffs or buildings. Taking into consideration all of the unforeseen variables, such as wind change, base jumping has a huge mortality rate that is 43% higher than its predecessor: parachuting",
          img: "jump.png"
        },
        {
          title: "Limbo Skating – for only the most flexible",
          text:
            "Hugely popular in India, this is one of the entries on our list of extreme sports that if you haven’t checked out before, now is the time.This sport involves roller skating in a splits position and passing underneath cars or low bars. The longest limbo-skating stint achieved under bars was 603.67 feet (184 metres) by G. Devisri Prasad in India in 2017.",
          img: "limbo.png"
        },
        {
          title:
            "Crocodile Bungee Jumping – the jump to crocodile-infested waters",
          text:
            "Bungee jumping made its debut onto the extreme sports scene in 1979 and has been attracting adrenaline junkies since its inception. As if it weren’t hair raising enough, how about jumping over crocodile-infested waters? This unusual sport is popular in Australia and Africa and has had its share of tragedies to date.",
          img: "croc.png"
        }
      ]
    };
  }
};
</script>
<style lang="scss" scoped>
.mainWrapp {
  display: flex;
  align-items: center;
  flex-direction: column;
  padding: 50px 10px;
  h1 {
    font-family: "AlFresco";
    font-size: 80px;
    font-weight: normal;
  }

  ol {
    width: 80%;
    li {
      &::marker {
        font-size: 26px;
        opacity: 0.8;
        font-weight: 550;
      }
      .itemTitle {
        display: block;
        padding: 50px 0px 20px 0px;
        font-size: 26px;
        opacity: 0.8;
        font-weight: 550;
      }
      .footerInfoTop {
        display: flex;
        align-items: center;
        img {
          width: 25%;

          border-radius: 5%;
          opacity: 0.65;
        }
        div {
          line-height: 180%;
          opacity: 0.7;
          font-size: 22px;
          padding-left: 30px;
        }
      }
    }
  }
}
</style>
