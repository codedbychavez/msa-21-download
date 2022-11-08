<template>
  <div>
    <section>
      <div class="container">
        <div class="flex-row">
          <div class="downloads-col-1">
            <div class="has-left-border">
              <div class="text-container">
                <h1 class="downloads-title">Downloads</h1>
              </div>
            </div>
            <div class="text-container">
              <p class="downloads-description">
                Lorem ipsum dolor sit amet, consectetur.
              </p>
            </div>

            <div class="button-wrapper button-wrapper-desktop">
              <button class="downloads-button">Download all (desktop)</button>
            </div>
          </div>
          <div class="downloads-col-2">
            <picture>
              <source srcset="@/assets/images/downloads_desktop.png" media="(min-width: 700px)">
              <img class="downloads-image" src="@/assets/images/downloads_mobile.png">
            </picture>
          </div>
        </div>
        <div class="button-wrapper button-wrapper-mobile">
          <button class="downloads-button">Download all (mobile)</button>
        </div>
      </div>
    </section>
  </div>
</template>

<script>

export default {
  
}

</script>

<style lang="scss">


// Specific styles

.container {
  padding: 24px;
}

.has-left-border {
  display: flex;
  align-items: center;
  height: 48px;
  border-left: 2px solid red;
}

.downloads-title {
  margin-left: 24px;
}

.downloads-description {
  margin-top: 20px;
}

.downloads-col-2 {
  margin-top: 24px;
}

.downloads-image {
  width: 100%;
}

.button-wrapper {
  @extend .text-container;
}

.button-wrapper-mobile {
  margin-top: 168px;
}

.button-wrapper-desktop {
  display: none;
}

.downloads-button {
  background-color: transparent;
  border: 0;
  cursor: pointer;
}

@media (min-width: 700px) {
  .container {
    padding: 64px;
  }

  .flex-row {
    display: flex;
    gap: 24px;
  }

  .downloads-col-1,
  .downloads-col-2 {
    margin: 0;
    width: 100%;
  }

  .downloads-col-1 {
    @extend .flex-row;
    gap: 0;
    flex-direction: column;
  }

  .text-container {
    margin-left: 128px;
  }

  .has-left-border {
    height: 72px;
  }

  .downloads-title {
    margin-left: 0;
    font-size: 52px;
    font-weight: 300;
  }

  .downloads-description {
    font-size: 20px;
    line-height: 24px;
  }

  .button-wrapper-mobile {
    display: none;
  }

  .button-wrapper-desktop {
    display: block;
    margin-top: auto;
  }
}

</style>