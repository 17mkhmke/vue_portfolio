<template>
  <ResumeComponent/>
</template>
<script>
import ResumeComponent from '@/components/ResumeComponent.vue'
export default {
  components: {
    ResumeComponent
  }
}

</script>
<style>
#Education{
  background: lightyellow;
}
.row2{
  border:double gold;
}
/* ===================================================Skills====================================================== */
.skills {
    display:flex;
    justify-content: center;
    align-items: center;
    min-height:100vh;
    background: lightgoldenrodyellow;

}
.cont {
    position: relative;
    display:flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    gap: 40px;

}
.container1{
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-column-gap: 1em;
  margin-left: -2%;
  margin-right: -2%;
}
.cont .skillCard {
    position: relative;
    width: 220px;
    height: 250px;
    background: #303030;
    display:flex;
    justify-content: center;
    align-items: center;
}
.cont .skillCard .percent {
    position: relative;
    width: 150px;
    height: 150px;

}
.cont .skillCard .percent svg{
    position: relative;
    width: 150px;
    height: 150px;
    transform:rotate(270deg)
}
.cont .skillCard .percent svg circle {
    width: 100%;
    height: 100%;
    fill: transparent;
    stroke-width: 2;
    stroke: #191919;
    transform: translate(5px,5px);
}
.cont .skillCard .percent svg circle:nth-child(2) {
    stroke:var(--clr);
    stroke-dasharray: 440;
    stroke-dashoffset: calc(440 - (440 * var(--num)) / 100);
    opacity: 0;
    animation: fadeIn 1s linear forwards;
    animation-delay: 2.5s;

}
.dot {
    position: absolute;
    inset: 5px;
    z-index: 10;
    transform: rotate(calc(3.6deg * var(--num)));
    animation: animateDot 2s linear forwards;
}
@keyframes animeDot {
    0% {
        transform: rotate(0deg);
    }
    100% {
        transform: rotate(calc(33.6deg * var(--num)));
    }
}
.dot ::before{
    content: '';
    position:absolute;
    top: -5px;
    left: 50%;
    transform:translate(-50%);
    width: 10px;
    height: 10px;
    border-radius: 50%;
    background: var(--clr);
    box-shadow: 0 0 10px var(--clr), 0 0 30px var(--clr);
}
.number {
    position: absolute;
    inset: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    opacity: 0;
    animation: fadeIn 1s linear forwards;
    animation-delay: 2.5s;
}
@keyframes fadeIn {
    0%{
        opacity: 0;
    }
    100%{
        opacity: 1;
    }
}
.number h2{
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
    font-weight: 700;
    font-size: 2.5em;

}
.number h2 span {
    font-weight: 300;
    color: white;
    font-size: 0.5em;
}
.number p {
    font-weight :300;
    font-size: 0.75em;
    line-height: 2px;
    margin-top: 5px;
    text-transform: uppercase;
    color:lightblue;
}
.picture{
  width: 25rem;
  height: 25rem;
}
</style>
