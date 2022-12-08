<template>
  <div id="snow">

  </div>
</template>
<script>
export default {
  name: "MerryChristmas",
  data() {
    return {
      snowflakes_count: 200
    }
  },
  methods: {
    toggle_snow() {
      let check_box = document.getElementById("toggle_snow");
      if (check_box.checked == true) {
        document.getElementById('snow').style.display = "block";
      }
      else {
        document.getElementById('snow').style.display = "none";
      }
    },

    // Creating snowflakes
    spawn_snow(snow_density = 200) {
      snow_density -= 1;

      for (let x = 0; x < snow_density; x++) {
        let board = document.createElement('div');
        board.className = "snowflake";

        document.getElementById('snow').appendChild(board);
      }
    },

    // Append style for each snowflake to the head
    add_css(rule) {
      let css = document.createElement('style');
      css.type = 'text/css';
      css.appendChild(document.createTextNode(rule)); // Support for the rest
      document.getElementsByTagName("head")[0].appendChild(css);
    },
    
    // Math
    random_int(value = 100) {
      return Math.floor(Math.random() * value) + 1;
    },

    random_range(min, max) {
      min = Math.ceil(min);
      max = Math.floor(max);
      return Math.floor(Math.random() * (max - min + 1)) + min;
    },


    // Create style for snowflake
    spawnSnowCSS(snow_density = 200) {
      let snowflake_name = "snowflake";
      let rule = ``;
      if (typeof base_css !== 'undefined') {
        rule = base_css;
      }

      for (let i = 1; i < snow_density; i++) {
        let random_x = Math.random() * 100; // vw
        let random_offset = this.random_range(-100000, 100000) * 0.0001; // vw;
        let random_x_end = random_x + random_offset;
        let random_x_end_yoyo = random_x + (random_offset / 2);
        let random_yoyo_time = this.random_range(30000, 80000) / 100000;
        let random_yoyo_y = random_yoyo_time * 100; // vh
        let random_scale = Math.random();
        let fall_duration = this.random_range(10, 30) * 1; // s
        let fall_delay = this.random_int(30) * -1; // s
        let opacity_ = Math.random();

        rule += `
        .${snowflake_name}:nth-child(${i}) {
            opacity: ${opacity_};
            transform: translate(${random_x}vw, -10px) scale(${random_scale});
            animation: fall-${i} ${fall_duration}s ${fall_delay}s linear infinite;
        }

        @keyframes fall-${i} {
            ${random_yoyo_time * 100}% {
                transform: translate(${random_x_end}vw, ${random_yoyo_y}vh) scale(${random_scale});
            }

            to {
                transform: translate(${random_x_end_yoyo}vw, ${document.body.clientHeight}px) scale(${random_scale});
            }
            
        }
        `
      }

      this.add_css(rule);
    }
  },
  mounted () {
    this.spawnSnowCSS(this.snowflakes_count);
    this.spawn_snow(this.snowflakes_count);
  }

}


</script>
<style>
.snowflake {
  position: absolute;
  width: 10px;
  height: 10px;
  background: linear-gradient(white, white);
  /* Workaround for Chromium's selective color inversion */
  border-radius: 50%;
  filter: drop-shadow(0 0 10px white);
}
</style>
