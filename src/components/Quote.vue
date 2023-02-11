<template>
  <div class="quote">
      <div class="quote-content">
          {{ content }}
          <div class="quote-info">
          <div class="quote-anime">
             - {{ category }}
          </div>
          <figure class="quote-author">
              <img :src="avtar_img" alt="Image">
          </figure>
      </div>
      </div>
  </div>
</template>

<script>

export default {
    name: 'quote',
    props: ["content", "category", "author", "avtar_img"]
}
</script>

<style lang="scss" scoped>
.quote {
        position: relative;
        margin: 0 auto;
        padding: 32px;
        max-width: 720px;


        &-content {
            position: relative;
            padding: 80px 35px;
            background-color: white;
            color: var(--dark);
            font-size: 24px;
            text-align: center;
            border-radius: 7px;
            box-shadow: 0 2px 4px rgb(0, 0, 0, 10%);

            &::before {
                content: '"';
                font-size: 24pt;
                color: var(--grey);
                margin: 0 10px;
            }
        }
        &-info {
            .quote-author,
            .quote-anime {
                position: absolute;
                font-size: 18px;
                font-weight: 100;
            }
            .quote-author {
                right: 50%;
                top: -50px;
                width: 85px;

                img {
                position: absolute;
                width: 85px;
                max-width: 100%;
                object-fit: cover;
                aspect-ratio: 1/1;
                border-radius: 50%;
                border: 10px solid var(--dark);
            }
            }
            .quote-anime {
                bottom: 30px;
                color: var(--dark);
            }
        }    
    }
</style>