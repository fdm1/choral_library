<script context="module" lang="ts">
  import { writable } from "svelte/store";
  import { setContext } from "svelte";

  export let data;

  interface User {
    email: string | null;
    name: string | null;
  }

  const UserStore = writable<User>({ email: null, name: null });

  export const userLogout = () => {
    UserStore.set({ email: null, name: null });
    setContext("user", UserStore);
    UserStore.subscribe(value => console.log("Logged out: ", value));
  };

  export const userLogin = (email: string | null, name: string | null) => {
    UserStore.set({ email, name });
    setContext("user", UserStore);
    UserStore.subscribe(value => console.log("Logged in: ", value));
  };
</script>
