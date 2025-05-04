<script lang="ts">
    import Cake from './Cake.svelte'
    import Text from "$lib/Components/Text.svelte";
    let isAnimation: boolean = false
    let audioButton: HTMLAudioElement
    let unwrapButton: HTMLButtonElement
    function buttonClicked() {
        isAnimation = !isAnimation
        audioButton.play()
        unwrapButton.style.display = 'none'
    }
</script>

<div class="BirthdayMessage">
  <Text source="/images/text/text1.png" --width="25%" --left="10%" --top="10%" --degree="-90deg"/>
  <Text source="/images/text/text2.png" --width="25%" --left="20%" --top="10%"/>
  <Text source="/images/text/text3.png" --width="25%" --left="50%" --top="10%"/>
  <Text source="/images/text/text4.png" --width="30%" --left="10%" --top="40%"/>
  <Text source="/images/text/text5.png" --width="25%" --left="70%" --top="70%"/>
  <Text source="/images/text/text6.png" --width="25%" --left="0%" --top="60%"/>
  <Text source="/images/text/text7.png" --width="25%" --left="70%" --top="40%"/>
  <Text source="/images/text/text8.png" --width="25%" --left="30%" --top="50%"/>
  <Text source="/images/text/text9.png" --width="25%" --left="75%" --top="20%"/>
    <audio bind:this={audioButton}>
        <source src="/audio/HappyBirthdaySong.mov" />
    </audio>
      <div class="Opener">
          <button
              class="OpenerButton"
              onclick={() => buttonClicked()}
              bind:this={unwrapButton}>
              Unwrap Me
          </button>
          <div
              class="leftOpener"
              class:rightAndLeftOpenerAnimation={isAnimation}>
            <div class="theLines"></div>
            <div class="theLines3"></div>
          </div>
          <div
              class="rightOpener"
              class:rightAndLeftOpenerAnimation={isAnimation}>
            <div class="theLines"></div>
            <div class="theLines2"></div>
          </div>
      </div>
    <h1>
        Happy Birthday <span>Maddy</span>
    </h1>

    <div class="Cake">
        <Cake />
    </div>
</div>

<style>
    .OpenerButton {
        width: 17vw;
        height: 12vh;
        font-size: 3vw;
        background: transparent;
        cursor: pointer;
        border: 0;
        position: absolute;
        top: 42%;
        left: 41.5%;
        z-index: 20;
    }
    .BirthdayMessage {
        position: relative;
        width: 100vw;
        height: 105vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
    }
    .Opener {
        z-index: 1000;
        position: absolute;
        width: 100%;
        height: 100%;
    }
    .leftOpener {
        transform-origin: left;
        position: absolute;
        top: 0;
        left: -1rem;
        width: 60%;
        height: 100%;
        background: lightcoral;
    }
    .rightAndLeftOpenerAnimation {
        perspective: 2000px;
        transform-style: preserve-3d;
        animation: rightOpener 4s forwards;
    }
    .rightOpener {
        transform-origin: right;
        position: absolute;
        top: 0;
        right: -1rem;
        width: 51%;
        height: 100%;
        background: lightcoral;
    }
    .theLines2{
      position: absolute;
      width: 10%;
      height: 100%;
      background: lightblue;
    }
    .theLines3{
      left: 75%;
      position: absolute;
      width: 30%;
      height: 100%;
      background: lightblue;
    }
    @keyframes rightOpener {
        0% {
            transform: rotateY(0deg);
        }
        100% {
            transform: rotateY(90deg);
            display: none;
        }
    }
    .Cake {
        margin-top: 25%;
        margin-left: 40%;
    }
    div {
        height: 80vh;
    }
    h1 {
        margin-left: auto;
        margin-right: auto;
        font-family: Beachday;
        font-size: 5rem;
        color: #add8e6;
        width: 35rem;
        height: 0;
        margin-top: 18rem;
    }
    span {
        margin-left: 10rem;
    }
    @font-face {
        font-family: 'Beachday';
        src: url('/fonts/beachday.otf') format('opentype');
        font-weight: normal;
        font-style: normal;
    }
    .theLines{
      position: absolute;
      top: 41%;
      width: 100%;
      height: 13%;
      background: lightblue;
    }
    .ExtraText{
      position: relative;
    }
</style>
