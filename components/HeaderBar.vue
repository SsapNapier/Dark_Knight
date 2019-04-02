<template lang="jade">
div.header-bar#menu
  nuxt-link.header-bar.link.active {{ greeting }}
  nuxt-link.header-bar.link О компании
  nuxt-link.header-bar.link Стать субагентом
  nuxt-link.header-bar.link Услуги
  nuxt-link.header-bar.link Контакты
</template>

<script>
    module.exports = {
        data: function() {
            return {
                greeting: 'Главная'
            }
        }
    }
</script>

<style lang="sass?indentedSyntax=true">
body
  box-sizing: border-box
  padding: 0
  margin: 0 auto
  background: #1a1a1a

.container
  display: flex

#menu
  position: relative
  top: 89px
  flex-basis: 100%

  &:before
    content: ""
    display: inline-block
    vertical-align: middle
    box-sizing: border-box
    width: 42%
    height: 1px
    background: #c5c5c5

@media screen and (max-width: 1280px)
  #menu:before
    width: 44%
    margin-right: 14px

nuxt-link
  font-family: SegoeUI
  font-size: 12px
  color: #c5c5c5
  cursor: pointer
  margin-left: 50px

  &:hover
    color: #00aeef
    border-bottom: 1px solid #00aeef
    padding-bottom: 14px
    text-decoration: none

  &.active
    color: #00aeef
    border-bottom: 1px solid #00aeef
    padding-bottom: 14px
    text-decoration: none
@media screen and (max-width: 1280px)
  nuxt-link
    margin-left: 40px
    font-size: 64%
</style>
