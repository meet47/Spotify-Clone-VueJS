<template>
  <div class="w-full sticky top-0 p-2 flex items-center justify-between h-14">
    <div class="flex items-center mx-3">
      <button class="ml-3 rounded-full bg-black w-8 h-8 text-white">
        <fa
          icon="chevron-left"
          class="mx-1 opacity-75 hover:opacity-100"
          size="2x"
        />
      </button>
      <button class="mx-3 rounded-full bg-black w-8 h-8 text-white">
        <fa
          icon="chevron-right"
          class="mx-2 opacity-75 hover:opacity-100"
          size="2x"
        />
      </button>
    </div>
    <div class="pr-2">
      <Menu as="div" class="relative inline-block text-left">
        <div>
          <MenuButton
            class="inline-flex justify-center w-full rounded-full border-gray-300 shadow-sm px-4 py-2 bg-black text-s font-semibold text-white hover:bg-light focus:outline-none"
          >
            <img src="../assets/user.png" class="rounded-full h-6 w-6 mr-2" />
            Meet
            <ChevronDownIcon
              class="-mr-1 ml-2 h-5 w-5 mt-1"
              aria-hidden="true"
            />
          </MenuButton>
        </div>

        <transition
          enter-active-class="transition ease-out duration-100"
          enter-from-class="transform opacity-0 scale-95"
          enter-to-class="transform opacity-100 scale-100"
          leave-active-class="transition ease-in duration-75"
          leave-from-class="transform opacity-100 scale-100"
          leave-to-class="transform opacity-0 scale-95"
        >
          <MenuItems
            class="origin-top-right absolute right-0 mt-2 w-56 rounded-md shadow-lg bg-light ring-1 ring-black ring-opacity-5 focus:outline-none"
          >
            <div class="py-1">
              <MenuItem v-slot="{ active }">
                <a
                  href="#"
                  :class="[
                    active ? 'bg-dark text-lightest' : 'text-lightest',
                    'block px-4 py-2 text-s font-semibold',
                  ]"
                  >Account</a
                >
              </MenuItem>
              <MenuItem v-slot="{ active }">
                <a
                  href="#"
                  :class="[
                    active ? 'bg-dark text-lightest' : 'text-lightest',
                    'block px-4 py-2 text-s font-semibold',
                  ]"
                  >Profile</a
                >
              </MenuItem>
              <MenuItem v-slot="{ active }">
                <a
                  href="#"
                  :class="[
                    active ? 'bg-dark text-lightest' : 'text-lightest',
                    'block px-4 py-2 text-s font-semibold',
                  ]"
                  >Upgrade to Premium</a
                >
              </MenuItem>
              <form method="POST" action="#">
                <MenuItem v-slot="{ active }">
                  <button
                    type="submit"
                    :class="[
                      active ? 'bg-dark text-lightest' : 'text-lightest',
                      'block w-full text-left px-4 py-2 text-s font-semibold',
                    ]"
                  >
                    Log out
                  </button>
                </MenuItem>
              </form>
            </div>
          </MenuItems>
        </transition>
      </Menu>
    </div>
  </div>
</template>

<script>
import { Menu, MenuButton, MenuItem, MenuItems } from "@headlessui/vue";
import { ChevronDownIcon } from "@heroicons/vue/solid";

export default {
  name: "Header",
  components: {
    Menu,
    MenuButton,
    MenuItem,
    MenuItems,
    ChevronDownIcon,
  },
};
</script>
