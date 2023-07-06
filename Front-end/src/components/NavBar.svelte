<script>
  import { Navbar, NavBrand, NavLi, NavUl, NavHamburger, Avatar, Dropdown, DropdownItem, DropdownHeader, DropdownDivider } from 'flowbite-svelte'
</script>

<nav>
  <Navbar let:hidden let:toggle>
    <NavBrand href="/">
          <span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white custom-title p-10">DevAccess</span>
    </NavBrand>
    <div class="flex items-center md:order-2 px-10">
      <Avatar id="avatar-menu" src="avatar.jpg" class="w-20 h-20" />
      <NavHamburger on:click={toggle} class1="w-full md:flex md:w-auto md:order-1" menuClass="h-20 w-20 shrink-0"/>
    </div>
    <Dropdown placement="bottom" triggeredBy="#avatar-menu">
      <DropdownHeader>
      <span class="block text-sm"> Bonnie Green </span>
      <span class="block truncate text-sm font-medium"> name@flowbite.com </span>
      </DropdownHeader>
      <DropdownItem>Dashboard</DropdownItem>
      <DropdownItem>Settings</DropdownItem>
      <DropdownItem>Earnings</DropdownItem>
      <DropdownDivider />
      <DropdownItem>Sign out</DropdownItem>
    </Dropdown>
    <NavUl {hidden}>
      <NavLi href="/" active={true}>Home</NavLi>
      <NavLi href="/about">About</NavLi>
      <NavLi href="/services">Services</NavLi>
      <NavLi href="/pricing">Pricing</NavLi>
      <NavLi href="/contact">Contact</NavLi>
    </NavUl>
  </Navbar>
</nav>
<style lang="scss">
  @import "../styles/extends";
  @import "../styles/mixins";
  @import "../styles/variables";

  .custom-title{
    font-size: 2.4rem !important;
    font-family: $quote-font;
  }

nav{
  position: fixed;
    width: 100%;
    z-index: 1;
}
</style>
