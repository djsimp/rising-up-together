<template>
  <div id="board-trustees">
    <MemberProfile v-for="member in members" :key="member.name" :name="member.name" :title="member.title" :img="member.img" />
  </div>
</template>

<script>
import MemberProfile from './MemberProfile.vue'

export default {
  name: 'BoardTrustees',
  data: function() {
    return {
      members: [
        {
          name: "Shelly A. Jordan",
          title: "Founder of Rising Up Together & Chief of Board of Trustees",
          img: "../../assets/board-members/Shelly-Jordan.jpg",
          /*bio: "Becoming the founder of Rising Up Together was not ever in
            Shelly Jordan&#39;s plans. In fact, it took a lot of prayers and
            persuasion before she finally submitted herself to the daunting,
            yet inspiring and incredibly fulfilling task!\n\n
            It was Shelly&#39;s personal experience with depression after her
            mother died; as well as helping her teenage daughter who suffered
            with anxiety, that led Shelly to this great opportunity.\n\n
            Shelly always had a strong desire to help and lift the youth.
            She finds purpose in bringing people together, as well as she lifts
            and serves so many around her. Her genuine love for others is felt
            by all who know her.\n\n
            As a director at Especially for Youth, Shelly has greatly shaped for
            good many youth throughout the nation and continues to inspire many
            with her love and enthusiasm for life!\n\n
            She has served in many different capacities in her community, family,
            neighbors, and church callings. Her personal experience as a volunteer
            has helped her witness healing that comes as we lift
            and serve each other.\n\n
            Shelly Jordan currently lives in Layton, Utah with her loving husband
            Rick Jordan and their five enjoyable children. She is grateful to have
            the powerful ability to empathize with those in her family and others
            because of her experiences. She is excited to inspire others to do
            the same as we all come together to bring hope to these wonderful
            youth to a safer and brighter future!"*/
        }, {
          name: "Elise Cole",
          title: "Secretary of Rising Up Together",
          img: "../../assets/board-members/Elise-Cole.JPG",
          /*bio: "Elise’s interest in this cause is a personal one. She struggled
            off and on with clinical depression in High School. More recently, she
            has battled postpartum depression after each of her daughters was born.\n\n
            She is currently employed as a radiology technologist at
            Davis Hospital and Medical Center. She has been serving members of
            her community with compassion and empathy in this capacity for over 15 years.\n\n
            Elise has been married for 14 years to her husband Michael,
            who teaches religion classes at Morgan High School. She is also the
            mother of five little girls. She enjoys the outdoors - especially if
            it includes spending time with a book in the hammock in her backyard.
            She also enjoys creative work - dabbling in painting, decorating,
            knitting and crocheting. Elise is also an accomplished pianist and
            vocal soloist. She has served in many other capacities, in both
            positions helping the youth and women in her community.\n\n
            Elise has chosen to make it her mission to use her experiences to help
            others find help and healing in their own struggles with mental illness."*/
        }, {
          name: "Jill Laurence",
          title: "Treasurer of Rising Up Together",
          img: "../../assets/board-members/Jill-Laurence.JPG",
          /*bio: "The reason Jill is a part of this organization is she has eleven
            nieces and nephews she cares deeply about. They all attend, or have
            attended, school in Davis County and she desires a wonderful
            environment for them to thrive and learn.\n\n
            Jill wants this organization to reach out to all, especially those
            individuals who feel like they “don’t fit the mold” and give them a voice.
            Children are bombarded at a young age with all kinds of difficult,
            diverse situations to handle. There are lots of children who may not
            have a supportive aunt, parent, or anyone they can confide in that
            could find shelter in the programs administered by this organization
            in tackling mental issues or crippling despair.\n\n
            Jill has over 16 years of diverse experience in the financial industry
            and is currently the Chief Financial Officer for FloorTex, a concrete
            floor polishing company located in West Haven, Utah.\n\n
            Jill was born and raised in Layton, Utah where she currently lives as
            a full-time aunt extraordinaire to eleven of the best nieces and
            nephews who she spoils shamelessly. She loves to collect vinyl records,
            shoes, and experiences as she travels. Writing her story as she goes,
            she’s a lover of words and music. Jill plays the piano, flute, violin,
            ukulele and she loves to sing (mostly in the car and shower for the
            sake of anyone who can hear).\n\n
            One of her bucket list items is to visit all seven continents,
            and she only has one more to go! Jill loves to play games (card,
            board, and video) with family and friends.\n\n
            She delights in working with the youth in her community as well as
            those within her family."*/
        }, {
          name: "Ashley Garbe Smith",
          title: "Board Member",
          img: "../../assets/board-members/Ashley-Garbe-Smith.jpg",
          /*bio: "Ashley Garbe Smith is an attorney, professional musician,
            and speaker. While working in several different industries with high
            rates of depression and anxiety, Ashley has witnessed many close
            friends and colleagues battle mental illness. After Ashley’s first
            husband died in a helicopter crash, Ashley learned to manage her own
            depression and anxiety through therapy, counseling, meditation,
            music, and physical exercise.\n\n
            Ashley works for the law firm of Kesler &amp; Rust in Salt Lake City
            practicing business law, estate planning, real estate and construction
            law, and litigation. As a musician, Ashley has toured nationally with
            several bands as a keyboardist and singer. She wrote and produced her
            own album in 2012 and continues to write and perform. Ashley loves
            going to concerts and spending time outdoors with her husband of
            13 years and two energetic boys.\n\n
            Ashley is passionate about challenging and overcoming stigmas
            associated with mental illness as well as helping others discover
            tools to manage and cope with their own depression and anxiety."*/
        }, {
          name: "Brady Griffin",
          title: "Board Member",
          img: "../../assets/board-members/Brady-Griffin.jpg",
          /*bio: "I am married and am the father of three boys. I am a
            Weber State University graduate. I have a master’s degree in
            Business Administration, and a bachelor’s degree in Quantitative
            Economics with a minor in Accounting and a minor in Mathematics.
            I am a self published author, and have given away hundreds of
            books in order to help promote a better society and happier
            individuals. I have teaching experience with teenagers, and have
            spent years volunteering in youth groups. I love working with people,
            I’m good with numbers, and I want to make a difference.\n\n
            I am very passionate about helping people in need, and with my
            analytical background, I am always looking for ways to do more good
            with limited recources. I also went through foster care training,
            which helped me better understand trauma, and how to help people
            who struggle with various emotional conditions."*/
        }, {
          name: "Kali Hoenes",
          title: "Board Member",
          img: "",
          /*bio: "Kali Hoenes is pleased to be a member of the Rising Up Together
            organization. She is a firm believer that sharing thoughts, feelings
            and trials with others is crucial to surviving life. She feels
            strongly that sharing her own story has helped her connect with others
            as well as helped in her own healing process after her 2-year-old son
            fell 14 feet from her 2nd story window. Although he survived, the road
            ahead was a long and hard one to walk.\n\n
            Since the accident, Kali and each of her family members have faced
            the hardships that can come from trauma. Anxiety, shame, depression,
            isolation and guilt to name a few. In sharing her story, Kali has
            learned that you don’t have to go through the same trial to relate
            to one another. Loss, in one way or another, loss of what you thought
            your life would look like, has been a key factor in relating to others
            dealing with difficult hardships of their own.\n\n
            Kali has a passion for the outdoors and graduated from Utah State
            University in the field of Parks and Recreation. She has enjoyed
            working on the recreation side of things for various cities in Utah
            running their summer programs, Boys and Girls Club, being an Elementary
            school P.E. teacher, a church youth leader for girls ages 12-18 off
            and on for the pas 11+ years and serving on the Parks and Recreation
            Commission for a small town in Arizona where she resided with her
            husband and children for 9 years until their recent relocation
            back to Utah."*/
        }, {
          name: "Lorene Lillywhite",
          title: "Board Member",
          img: "../../assets/board-members/Lorene-Lillywhite.jpg",
          /*bio: "Lorene Lillywhite is excited to be a part of the Rising Up
            Together effort. Personally, she has experienced the struggle that
            anxiety and depression can have on families. Her mother struggled
            with depression throughout her life. Lorene has also had her own
            personal struggles with anxiety. Some of her children have experienced
            struggles with depression and anxiety, and other mental health issues.
            She also has friends that have experienced the devastating affects of
            suicide.\n\n  
            Lorene has been married for almost 33 years. She is the mother of five
            children and grandmother to 3. She has a Bachelor’s degree in
            elementary education and a Master’s degree in education. She taught
            first grade for a short time before starting her family and has been
            employed as a substitute teacher for over 30 years. She and her family
            have lived in Layton, Utah since 1994.\n\n
            Lorene enjoys being involved in community efforts; especially
            interacting with her neighbors and friends. She enjoys being physically
            active. She enjoys biking, rollerblading, playing pickle ball,
            wake boarding, and jogging. She has enjoyed learning how to play the
            organ. Her greatest fun is being with her family.\n\n
            Lorene is very active in her faith and enjoys serving in different
            capacities in her church. She loves being with people and has the
            philosophy that, “we are all in this together” (meaning our life
            experience). Her goal is to help others along their path as much as
            possible. Rising Up Together is a great way to make this happen!"*/
        }, {
          name: "Laurn Miner Zufelt",
          title: "Board Member",
          img: "../../assets/board-members/Lauren-Miner-Zufelt.jpg",
          /*bio: "When describing Lauren Zufelt, people would identify her as a
            protector of children and individuals. Throughout her career and life,
            Lauren has worked to protect the well being and safety of children.
            Lauren is an elementary school teacher and works with students ages
            5-12, has participated in multiple youth camps/ activities and is a
            “natural mother” at heart.\n\n
            Lauren has seen the importance of promoting well-being from an early
            age. Her involvement in this organization is to help youth and
            children have the tools and strategies they need to be safe, healthy
            and be their best selves. Lauren’s involvement in this organization
            reaches a personal level as she has personally struggled with
            depression and anxiety and has recognized the essential need for support.\n\n
            She is currently employed as a fifth grade teacher in the Alpine School
            District with the Gifted Program. She recognizes everyday students
            who are heavily dealing with emotional/mental struggles. She is
            passionate about educating children and providing the necessary
            tools for them to succeed.\n\n
            Lauren has been married for one year to her husband, Jacob who is a
            construction management major. She enjoys singing, dancing, being
            outdoors, reading, serving, planning/ organizing, learning, creating
            tech creations and speaking. She is a professional singer.\n\n
            Lauren has dedicated her life to making this world a safer and
            better place for individuals to live in. She knows that that begins
            with an individual."*/
        }, {
          name: "Kristianne Rushton",
          title: "Board Member",
          img: "../../assets/board-members/Kristianne-Rushton.jpg",
          bio: ""
        }
      ]
    }
  },
  components: {
    MemberProfile
  }
}
</script>

<style scoped>
  #board-trustees {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
  }
</style>
