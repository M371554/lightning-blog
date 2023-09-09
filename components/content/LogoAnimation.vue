<template>
	<div class="bolt" ref="boltElement">
	  <svg viewBox="0 0 170 57" class="white left">
		  <path d="M36.2701759,17.9733192 C-0.981139498,45.4810755 -7.86361824,57.6618438 15.6227397,54.5156241 C50.8522766,49.7962945 201.109341,31.1461782 161.361488,2"></path>
	  </svg>
	  <svg viewBox="0 0 170 57" class="white right">
		  <path d="M36.2701759,17.9733192 C-0.981139498,45.4810755 -7.86361824,57.6618438 15.6227397,54.5156241 C50.8522766,49.7962945 201.109341,31.1461782 161.361488,2"></path>
	  </svg>
	  <div ref="divElement">
		  <span></span>
	  </div>
	  <svg viewBox="0 0 112 44" class="circle">
		  <path d="M96.9355003,2 C109.46067,13.4022454 131.614152,42 56.9906735,42 C-17.6328048,42 1.51790702,13.5493875 13.0513641,2"></path>
	  </svg>
	  <svg viewBox="0 0 70 3" class="line left">
		  <path transform="translate(-2.000000, 0.000000)" d="M2,1.5 L70,1.5"></path>
	  </svg>
	  <svg viewBox="0 0 70 3" class="line right">
		  <path transform="translate(-2.000000, 0.000000)" d="M2,1.5 L70,1.5"></path>
	  </svg>
	</div>
  </template>
  
  <script>
  import { TimelineMax, Back } from 'gsap';
  
  export default {
	mounted() {
	  this.$nextTick(() => {
		this.initAnimation();
	  });
	},
	methods: {
	  initAnimation() {
		const bolt = this.$refs.boltElement;
		const div = this.$refs.divElement;
  
		bolt.classList.add("animate");
  
		const tween = new TimelineMax({
		  onComplete: () => {
			bolt.classList.remove("animate");
			this.repeatAnimation(bolt, tween);
		  }
		})
		.set(div, { rotation: 360 })
		.to(div, 0.7, { y: 80, rotation: 370 })
		.to(div, 0.6, { y: -140, rotation: 20 })
		.to(div, 0.1, { rotation: -24, y: 80 })
		.to(div, 0.8, { ease: Back.easeOut.config(1.6), rotation: 0, y: 0 });
	  },
	  repeatAnimation(bolt, tween) {
		setTimeout(() => {
		  bolt.classList.add("animate");
		  tween.restart();
		}, 400);
	  }
	}
  };
  </script>


<style >
.bolt {
  --bolt: rgb(242, 222, 16);
  width: 126px;
  height: 186px;
  position: relative;
  top: 150px ;
  margin: auto;

}
.bolt svg {
  position: absolute;
  display: block;
  stroke-width: 4;
  fill: none;
  stroke-linecap: round;
  stroke: var(--bolt);
}
.bolt svg.circle {
  left: 7px;
  top: 100%;
  width: 112px;
  height: 44px;
  stroke-dashoffset: 179px;
  stroke-dasharray: 0px 178px;
}
.bolt svg.line {
  --r: 0deg;
  top: 95%;
  width: 70px;
  height: 3px;
  stroke-dashoffset: 71px;
  stroke-dasharray: 0px 70px;
  transform: rotate(var(--r));
}
.bolt svg.line.left {
  --r: 130deg;
  left: -24px;
}
.bolt svg.line.right {
  --r: 40deg;
  right: -24px;
}
.bolt svg.white {
  --r: 0deg;
  --s: 1;
  top: 30%;
  z-index: 1;
  stroke: #fff;
  stroke-dashoffset: 241px;
  stroke-dasharray: 0px 240px;
  transform: rotate(var(--r)) scaleX(var(--s));
}
.bolt svg.white.left {
  --r: -20deg;
  left: 0;
}
.bolt svg.white.right {
  --r: 20deg;
  --s: -1;
  right: 0;
}
.bolt div {
  display: block;
  position: relative;
}
.bolt div:before, .bolt div:after {
  content: "";
  position: absolute;
  left: 50%;
  top: 44%;
}
.bolt div:before {
  width: 112px;
  height: 112px;
  margin: -56px 0 0 -56px;
  background: #CDD9ED;
  filter: blur(124px);
}
.bolt div:after {
  width: 64px;
  height: 64px;
  margin: -32px 0 0 -32px;
  background: #FFF9BC;
  z-index: 1;
  filter: blur(60px);
}
.bolt div span {
  display: block;
  width: 106px;
  height: 186px;
  background: var(--bolt);
  -webkit-clip-path: polygon(80% 0%, 80% 0, 60% 45%, 90% 45%, 20% 100%, 40% 57%, 10% 57%);
          clip-path: polygon(80% 0%, 80% 0, 60% 45%, 90% 45%, 20% 100%, 40% 57%, 10% 57%);
}
.bolt.animate div:before, .bolt.animate div:after {
  -webkit-animation: shine 2s ease;
          animation: shine 2s ease;
}
.bolt.animate div span {
  -webkit-animation: morph 2s ease;
          animation: morph 2s ease;
}
.bolt.animate svg.circle {
  -webkit-animation: circle 0.45s cubic-bezier(0.77, 0, 0.175, 1) forwards 1.3s;
          animation: circle 0.45s cubic-bezier(0.77, 0, 0.175, 1) forwards 1.3s;
}
.bolt.animate svg.line {
  -webkit-animation: line 0.45s cubic-bezier(0.77, 0, 0.175, 1) forwards 1.3s;
          animation: line 0.45s cubic-bezier(0.77, 0, 0.175, 1) forwards 1.3s;
}
.bolt.animate svg.white {
  -webkit-animation: white 0.45s cubic-bezier(0.77, 0, 0.175, 1) forwards 1.45s;
          animation: white 0.45s cubic-bezier(0.77, 0, 0.175, 1) forwards 1.45s;
}
.bolt.animate svg.white.right {
  -webkit-animation-delay: 1.6s;
          animation-delay: 1.6s;
}

@-webkit-keyframes circle {
  100% {
    stroke-dasharray: 178px 178px;
  }
}

@keyframes circle {
  100% {
    stroke-dasharray: 178px 178px;
  }
}
@-webkit-keyframes white {
  100% {
    stroke-dasharray: 240px 240px;
  }
}
@keyframes white {
  100% {
    stroke-dasharray: 240px 240px;
  }
}
@-webkit-keyframes line {
  100% {
    stroke-dasharray: 70px 70px;
  }
}
@keyframes line {
  100% {
    stroke-dasharray: 70px 70px;
  }
}
@-webkit-keyframes shine {
  30%, 70% {
    opacity: 0;
  }
}
@keyframes shine {
  30%, 70% {
    opacity: 0;
  }
}
@-webkit-keyframes morph {
  12% {
    -webkit-clip-path: polygon(24% 50%, 100% 0, 65% 40%, 65% 40%, 8% 100%, 24% 50%, 24% 50%);
            clip-path: polygon(24% 50%, 100% 0, 65% 40%, 65% 40%, 8% 100%, 24% 50%, 24% 50%);
  }
  24%, 72% {
    -webkit-clip-path: polygon(36% 40%, 82% 40%, 82% 40%, 82% 40%, 36% 71%, 36% 40%, 36% 40%);
            clip-path: polygon(36% 40%, 82% 40%, 82% 40%, 82% 40%, 36% 71%, 36% 40%, 36% 40%);
  }
  84% {
    -webkit-clip-path: polygon(24% 50%, 100% 0, 65% 40%, 65% 40%, 8% 100%, 24% 50%, 24% 50%);
            clip-path: polygon(24% 50%, 100% 0, 65% 40%, 65% 40%, 8% 100%, 24% 50%, 24% 50%);
  }
}
@keyframes morph {
  12% {
    -webkit-clip-path: polygon(24% 50%, 100% 0, 65% 40%, 65% 40%, 8% 100%, 24% 50%, 24% 50%);
            clip-path: polygon(24% 50%, 100% 0, 65% 40%, 65% 40%, 8% 100%, 24% 50%, 24% 50%);
  }
  24%, 72% {
    -webkit-clip-path: polygon(36% 40%, 82% 40%, 82% 40%, 82% 40%, 36% 71%, 36% 40%, 36% 40%);
            clip-path: polygon(36% 40%, 82% 40%, 82% 40%, 82% 40%, 36% 71%, 36% 40%, 36% 40%);
  }
  84% {
    -webkit-clip-path: polygon(24% 50%, 100% 0, 65% 40%, 65% 40%, 8% 100%, 24% 50%, 24% 50%);
            clip-path: polygon(24% 50%, 100% 0, 65% 40%, 65% 40%, 8% 100%, 24% 50%, 24% 50%);
  }
}


</style>