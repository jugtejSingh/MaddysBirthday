<script lang="ts">
    import {innerWidth} from "svelte/reactivity/window";
    import Masonary from "$lib/Components/Masonary.svelte";

    export const source = [
      { source: "/images/maddyAndPeople/image1.jpeg",
      },
      { source: "/images/maddyAndPeople/image2.jpeg",
        text: "There are wayyy too many stories for us together and its kinda crazy looking back youre actually one of the few people who has been there for a lot of my first experiences, i cant think of a single funny moment, cause all of our moments are the most random experiences, from snooping through the walls in ncl and in grenada lmao, from playing random card games while drunk, singing anirudh songs out loud, dancing together, speaking in the weirdest mix of tamil and malayalam in a crowded room when no one could understand us, somehow always my partner in crime, you havent judged me and i only sort of get freaked out by your weird asf demonic laugh and the coolest person to live with, i was supposed to write about one instance but honestly every serious situation becomes funny whenever we talk about it, and somehow i always feel like home around you, even when youre family came to grenada spending time with all of you really meant a lot in many ways, idk if its the cultural similarities maybe that just made it better, youre one of my best friends and someone i consider a sister, thanks for always looking out for me and asking me if i need milk when you go grocery shopping. Love you always nanbi",
        source2: "/images/maddyAndPeople/image2.jpeg",
        name: "Shradha"
      },
      {source: "/images/maddyAndPeople/image3.jpeg",
      },
      {source: "/images/maddyAndPeople/image4.jpeg",
      },
      {source: "/images/maddyAndPeople/image5.jpeg",
      },
      {source: "/images/maddyAndPeople/image6.jpeg",
      },
      {source: "/images/maddyAndPeople/image7.jpeg",
        text: "My favourite memory w you isn’t something big but every time we sit in one of our flats nd yap (either high or sober) nd we start laughing loudly abt something, I have so much fun and even though it’s a small thing it’s one of my favourite things to do w you + i can only laugh like that w you. Also when we went to Blackpool nd we got lost away from the whole group obv cuz we wanted to smoke nd the joint fell nd we picked it up from the wet floor, smoked it nd then struggled to find the rest of the group and walked around the whole park 😭 i love doing this stuff w you and you don’t know how much I’m gonna miss you and spending time w you <3 happiest birthday madhi i love you so much I hope you have the best day and the best year ahead. I’m so proud of you for everything and I wish you all the luck for everything that’s coming ❤️",
        source2: "/images/maddyAndPeople/image7.jpeg",
        name:"Simone"
      },
      {source: "/images/maddyAndPeople/image8.jpeg",
      },
      {source: "/images/maddyAndPeople/image9.jpeg",
        text: "Helllooo girlyyyy remember this   Picture we took in London when we went with the guys, got fuck drunk and we went to this place with all lights got so amazed by it for some odd reason and these 2 were like our fathers just waiting for us to come out and talking about big boy stuff while we were laughing about each light we saw hahahahhah",
        source2: "/images/maddyAndPeople/image9.jpeg",
        name: "Manasvi"
      },
      {source: "/images/maddyAndPeople/image10.jpeg",
      },
      {source: "/images/maddyAndPeople/image11.jpeg",
      },
      {source: "/images/maddyAndPeople/image12.jpeg",
      },
      {source: "/images/maddyAndPeople/image13.jpeg",
      },
      {source: "/images/maddyAndPeople/image21.jpeg",
        text: "this was like in the first few days of us knowing each other and i like an idiot came outside on the streets w a singular sweater on idk with what confidence bro, and then you being all sweet hugged me cuz i was freezing to death and i just look at this picture a lot cuz it was so put of the blue but so cute, and its one of our first memories together, also not in the pic but remember those rides we went on behind student union that was soo fun and random and crazy😭😭" ,
        source2: "/images/maddyAndPeople/image20.jpeg",
        name: "Asra"
      },
      {source: "/images/maddyAndPeople/image14.jpeg",
      },
      {source: "/images/maddyAndPeople/image15.jpg",
        text: "There was once when we were in imcq n suddenly madhi opens her notes on her phone and goes to every person who owes her n tells them to pay it asap. It doesn’t sound as funny but the way she did it was soo soo funny. N then ppl were like take my share from this one n that one n she goes like no u all will pay me urs i m not taking money from others on ur behalf. Thats when I changed her name to stingy bitch on my phone 😭😂",
        source2: "/images/maddyAndPeople/image15.jpg",
        name: "Aditee"
      },
      {source: "/images/maddyAndPeople/image16.jpg",
      },
      {source: "/images/maddyAndPeople/image17.jpg",
      },
      {source: "/images/maddyAndPeople/image18.jpg",
      },
      {source: "/images/maddyAndPeople/image19.jpeg",
      },
      {source: "/images/maddyAndPeople/image20.jpeg",
        text: "this was deffo one of the most emo days of my life, leaving our amazingg life behind in that wonderful city and literally leaping blindly into whatever we thought grenada would be at that point… but i think celebrating your birthday like this was one of the most perfect endings to that beautiful chapter of our lives, absolutely loveddd this day it was soo cute😍",
        source2: "/images/maddyAndPeople/image20.jpeg",
        name: "Asra"
      },
      ];

    const columnInGrids :string = $derived.by(()=>{
      if(innerWidth.current <= 700 && innerWidth){
        return "1fr 1fr"
      }else if (innerWidth.current >= 2000) {
        return "1fr 1fr 1fr 1fr";
      }
      else{
        return "1fr 1fr 1fr";
      }
    });
</script>

<div class="Container">
    <Masonary sources={source} columnInGrids={columnInGrids} gap={'1rem'} />
</div>

<style>
    .Container {
      width: 100%;
      background: #e6e6fa;
    }
</style>