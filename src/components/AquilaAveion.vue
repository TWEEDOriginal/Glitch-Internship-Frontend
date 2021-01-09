<template>
  <div class="Aquila-background">
      <div id="center-div"> 
          <div class='header'><p>{{ details.name }}</p> </div>
          <div class='bigPicture'> <img src="../images/bigPicture.png"> </div>
          <div class='bottom' > <span>HOME</span>
          <span>  ABOUT </span><img src="../images/smallImage.png">
          <span> GALLERY </span>
          <span> CONTACT </span> </div>
      </div>
    <aside id="alwaysGuiding"> 
        <ul class="social-icons">
            <li class="media"> <a :href="`https://www.instagram.com/${details.social_media.instagram}`"> <font-awesome-icon :icon="['fab', 'instagram']" /> </a> </li>
            <li class="media"><a :href="`https://twitter.com/${details.social_media.twitter}`">  <font-awesome-icon :icon="['fab', 'twitter-square']" /> </a> </li>
            <li class="media"><a :href="`https://www.snapchat.com/add/${details.social_media.snapchat}`">  <font-awesome-icon :icon="['fab', 'snapchat-square']" /> </a> </li>
            <li class="media"><a :href="`mailto:${details.social_media.email}`">  <font-awesome-icon icon="envelope-square" />  </a> </li>
        </ul>
    </aside>
  </div>
</template>

<script>
export default {
  name: 'AquilaAveion',
 props: ['details']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@100;200;300&display=swap');
   .Aquila-background {
       position: relative;
       background: linear-gradient(90deg, #BD0F4D 50%, #CB2964 50%);
       height: 1024px;
       width: 1440px;
       transform: translate(16px, 16px);
       margin-bottom: 100px;
       font-family: 'Montserrat', sans-serif;
   }

   #center-div{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    height: 100%;
    width: 60%;
   }
   .header {
       text-align: center;
       transform: translateY(50px);
       
   }
   .bigPicture {
       text-align: center;
       transform: translateY(100px);
       
   }
   .bigPicture img {
        box-shadow: -5px 5px 10px 10px rgba(0, 0 , 0, 0.2);
   }
   .header p {
       font-weight: 200;
       font-size: 40px;
       letter-spacing: 10px;
   }
   .bottom {
       transform: translateY(120px);
       display: flex;
       flex-direction: row;
       justify-content: space-around;
       align-items: center;
       height: 100px;
   }
   
   .bottom span {
       font-weight: 300;
       font-size: 20px;
       letter-spacing: 5px;
   }
   .bottom img {
      transform: translateX(40%);
   }

   #alwaysGuiding {
    display: flex;
    flex-direction: column;
    position: absolute;
    transform: translate(-100%, -50%);
    width: 60px;
    top: 50%;
    left: 99%;
    align-items: center;
    justify-content: center;
 } 
 .social-icons {
   list-style: none;
 }
 .social-icons a {
    text-decoration: none;
    color: white;
}

 .media{
    display: flex;
    margin-bottom: 30px;
    height: 40px;
    width: 40px;
    align-items: center; 
    justify-content: center;
    font-size: 40px;
 }
 @media all and (max-width: 1440px) { 
     .Aquila-background {
       height: 70vw;
       width: 95vw;
   }

   .header {
       transform: translateY(3.5vw);
       
   }
   .bigPicture {
       transform: translateY(7vw);
       
   }
   .bigPicture img {
        width: 43.9vw;
        height: 47vw;
        box-shadow: -0.35vw 0.35vw 0.7vw 0.7vw rgba(0, 0 , 0, 0.2);
   }
   .header p {
       font-size: 2.8vw;
       letter-spacing: 0.7vw;
   }
   .bottom {
       transform: translateY(8.3vw);
       height: 7vw;
   }
   
   .bottom span {
       font-size: 1.39vw;
       letter-spacing: 0.35vw;
   }
   .bottom img {
      width: 6.9vw;
        height: 6.9vw;
   }

   #alwaysGuiding {
    width: 4.2vw;
 } 
 

 .media{
    margin-bottom: 2.08vw;
    height: 2.8vw;
    width: 2.8vw;
    font-size: 2.8vw;
 }
 }
 @media all and (max-width: 500px) {
     .Aquila-background {
       width: 100vw;
       transform: translateY(16px);
   }
 }
 

</style>
