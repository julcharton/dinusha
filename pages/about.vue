<template>
  <div class="wrapper">
    <div class="profile-pic">
      <img src="../static/2018crop.png" />
    </div>
    <div class="main-title">Biographie</div>
     <div class="description">
        <p>Dinusha is a Film, TVC and Content Producer based in Sydney, Australia. After graduating in 2004 with a BA (Communications) and following up with Producing and Production Management studies at Sydney’s Metroscreen Film School, Dinusha’s first taste of film was as a Producer’s Attachment on ‘Razzle Dazzle: A Journey Into Dance’ (2005) directed by Darren Ashton.
</p> 
<p>Following this, he took up a position at Darren’s Production Company Republic Films as inhouse PA where he stayed for two years. Since leaving Republic, he has freelanced as a Producer and PM for various companies across multiple forms of visual media. His first drama feature ‘The Pretend One’ was completed in 2017 and has since screened at multiple festivals worldwide.</p>
      </div>
  </div>
</template>

<script>
export default {
  mounted() {},
};
</script>

<style scoped>
.profile-pic img{
  height: 164px;
  border-radius: 50%;
  margin: auto;
  display: block
}
.wrapper {
  margin: auto
}
p {
  font-size: 14px;
  font-weight: 400;
  font-family: "Montserrat";
  letter-spacing: 0.9px;
  color: var(--text-primary-200);
  padding: 0 0 24px 0;
}
.description {
  margin: 16px 0;
  text-align: center;
}
.main-title {
  font-size: 24px;
  margin-top: 24px;
  text-align: center;
}
</style>