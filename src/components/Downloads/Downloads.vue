<template>
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

      <div class="button-wrapper-desktop">
        <button class="downloads-button">Download all (desktop)</button>
      </div>
    </div>
    <div class="downloads-col-2">
      <picture>
        <source
          srcset="@/assets/images/downloads_desktop.png"
          media="(min-width: 700px)"
        />
        <img
          class="downloads-image"
          src="@/assets/images/downloads_mobile.png"
        />
      </picture>
    </div>
  </div>
  <div class="button-wrapper-mobile">
    <button class="downloads-button">Download all (mobile)</button>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.has-left-border {
  display: flex;
  align-items: center;
  height: 48px;
  // NB: Primary/Red
  border-left: 2px solid #FF1F27;
}

.downloads-title {
  margin-left: 24px;
}

.downloads-description {
  margin-top: 16px;
}

.downloads-col-2 {
  margin-top: 24px;
}

.downloads-image {
  width: 100%;
}

.button-wrapper-mobile, .button-wrapper-desktop {
  @extend .text-container;
}

.button-wrapper-mobile {
  margin-top: 168px;
}

.button-wrapper-desktop {
  display: none;
}

.downloads-button {
  margin-left: 16px;
  background-color: transparent;
  border: 0;
  cursor: pointer;

}

@media (min-width: 700px) {
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
