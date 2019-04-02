<template lang="jade">
div.sidebar
  div.active.main Войти&nbsp;&nbsp;&nbsp;&#8594;
  div.bar
    div {{ greeting }}
    a Ж/Д Авиабилеты
    a Гостиницы
    a Страхование
    a Трансфер
</template>

<script>
    module.exports = {
        data: function() {
            return {
                greeting: 'Авиабилеты'
            }
        }
    }
</script>

<style lang="sass?indentedSyntax=true">
.sidebar
  font-family: SegoeUI
  font-size: 12px
  min-width: 12%
  min-height: 966px
  border-left: 1px solid #c5c5c5
  align-items: flex-end

@media screen and (max-width: 1280px)
  .sidebar
    font-size: 11px
    min-width: 175px

a
  position: relative
  top: 235px
  left: 11px
  color: #c5c5c5
  display: flex
  flex-direction: column
  padding: 17%

.main
  position: relative
  top: 92px
  left: 45px

.bar div
  position: relative
  top: 231px
  left: 15px
  color: #c5c5c5
  display: flex
  flex-direction: column
  padding: 14%

.bar a:before
  position: absolute
  top: 0
  width: 5%
  border-top: 1px solid #c5c5c5
  content: ""

.active
  color: #00aeef
  padding-bottom: 14px
  text-decoration: none
  cursor: pointer
</style>
