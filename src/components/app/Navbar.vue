<template>
  <nav class="navbar orange lighten-1">
    <div class="nav-wrapper">
      <div class="navbar-left">
        <a
          href="#"
          @click.prevent="$emit('click')"
        >
          <i class="material-icons black-text">dehaze</i>
        </a>
        <span class="black-text">12.12.12</span>
      </div>

      <ul class="right hide-on-small-and-down">
        <li>
          <a
            ref="dropdown"
            class="dropdown-trigger black-text"
            href="#"
            data-target="dropdown"
          >
            USER NAME
            <i class="material-icons right">arrow_drop_down</i>
          </a>

          <ul
            id="dropdown"
            class="dropdown-content"
          >
            <li>
              <a
                href="#"
                class="black-text"
              >
                <i class="material-icons">account_circle</i>Профиль
              </a>
            </li>
            <li
              class="divider"
              tabindex="-1"
            />
            <li>
              <a
                href="#"
                class="black-text"
              >
                <i class="material-icons">assignment_return</i>Выйти
              </a>
            </li>
          </ul>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Navbar',
  mounted () {
    M.Dropdown.init(this.$refs.dropdown, {
      constrainWidth: false
    })
  }
}
</script>

<style scoped>

</style>
