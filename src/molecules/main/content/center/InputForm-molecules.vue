<template>
  <div class="mainInput">
    <div class="mI-Inner">
      <user-icon></user-icon>
      <div class="mI-formOut">
        <form class="mI-form">
          <div class="mI-input-box">
            <input class="input-input">
            <i class="fas fa-image"></i>
          </div>
          <div class="mI-icon-box">
            <div class="icon-image">
              <i class="fas fa-image"></i>
            </div>
            <div class="icon-plus">
              <i class="far fa-plus-square"></i>
            </div>
            <div class="icon-booth">
              <i class="fas fa-person-booth"></i>
            </div>
            <div class="icon-marker">
              <i class="fas fa-map-marker-alt"></i>
            </div>
          </div>
          <div class="mI-submit-box">
            <div class="submit-plus">
              <i class="fas fa-plus-circle"></i>
            </div>
            <div class="submit-button">
              <button type="submit"></button>
            </div>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
    import UserIcon from "../../../../atoms/icons/UserIcon";
    export default {
        name: "InputForm-molecules",
      components: {'user-icon':UserIcon}
    }
</script>

<style scoped>
  .mainInput{
    width: 100%;
    background: #E8F4FB;
    border-bottom: 1px solid #e6ecf0;
  }
  .mI-Inner{
    padding: 15px;
  }
  .mI-icon-box{
    display: none;
  }
  .mI-submit-box{
    display: none;
  }
</style>
