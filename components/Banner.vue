<template>
    <div class="banner">
        <img src="../assets/images/bannerImage.jpg" alt="" class="cover">
        <div class="text-wrapper">
            <div class="text">
              <h1>all the  movies</h1>
                <a href="#movie-grid">
                    <b-button type="is-primary">See Them</b-button>
                </a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Banner'
}
</script>

<style lang="scss" scoped>
.banner {
  height: 400px;
  position: relative;

  &::after {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    height: 100%;
    width: 100%;
    background-color: rgba(0, 0, 0, 0.6);
  }
  .cover {
    object-fit: cover;
    height: 100%;
    width: 100%;
  }
  .text-wrapper {
    z-index: 99;
    position: absolute;
    top: 0;
    margin: 0;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;

    .text {
      width: 60%;
      margin: 0 auto;

        h1 {
          font-size: 36px;
        }

        button {
        font-size: 20px;
        align-self: flex-start;
      }
    }

    
  }
}

</style>