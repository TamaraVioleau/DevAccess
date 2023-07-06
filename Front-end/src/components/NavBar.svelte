<script>
  import {
    Navbar,
    NavBrand,
    NavLi,
    NavUl,
    NavHamburger,
    Avatar,
    Dropdown,
    DropdownItem,
    DropdownHeader,
    DropdownDivider,
  } from "flowbite-svelte";
</script>

<nav>
  <Navbar let:hidden let:toggle>
    <NavBrand href="/">
      <span
        class="self-center whitespace-nowrap text-xl font-semibold dark:text-white custom-title p-10"
        >DevAccess</span
      >
    </NavBrand>
    <div class="flex items-center md:order-2 px-10">
      <Avatar id="avatar-menu" src="avatar.jpg" class="w-20 h-20" />
      <NavHamburger
        on:click={toggle}
        class1="w-full md:flex md:w-auto md:order-1"
        menuClass="h-20 w-20 shrink-0"
      />
    </div>
    <Dropdown placement="bottom" triggeredBy="#avatar-menu">
      <DropdownHeader>
        <span class="block text-sm"> Bonnie Green </span>
        <span class="block truncate text-sm font-medium">
          name@flowbite.com
        </span>
      </DropdownHeader>
      <DropdownItem>Dashboard</DropdownItem>
      <DropdownItem>Settings</DropdownItem>
      <DropdownItem>Earnings</DropdownItem>
      <DropdownDivider />
      <DropdownItem>Sign out</DropdownItem>
    </Dropdown>
    <NavUl {hidden}>
      <NavLi class="text-4xl" href="/" active={true}><span class="custom-categories">Home</span></NavLi>
      <NavLi class="text-4xl" href="/about"><span class="custom-categories">About</span></NavLi>
      <NavLi class="text-4xl" href="/services"><span class="custom-categories">Services</span></NavLi>
      <NavLi class="text-4xl" href="/pricing"><span class="custom-categories">Pricing</span></NavLi>
      <NavLi class="text-4xl" href="/contact"><span class="custom-categories">Contact</span></NavLi>
    </NavUl>
  </Navbar>
</nav>

<style lang="scss">
  @import "../styles/extends";
  @import "../styles/mixins";
  @import "../styles/variables";

  .custom-title {
    font-size: 2.4rem !important;
    font-family: $quote-font;
  }

  .custom-categories {
    font-size: 2.4rem !important;
    font-family: $text-font;
    font-weight: 600;
  }

  nav {
    position: fixed;
    width: 100%;
    z-index: 1;
  }


</style>
