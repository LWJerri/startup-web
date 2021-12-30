<script>
  import { onMount } from "svelte";
  import { themeChange } from "theme-change";

  // NOTE: the element that is using one of the theme attributes must be in the DOM on mount
  onMount(() => {
    themeChange(false);
    // 👆 false parameter is required for svelte
  });
</script>

<div>
  <div class="navbar mb-2 shadow-lg bg-neutral text-neutral-content rounded-box">
    <div class="px-2 mx-2 navbar-start">
      <span class="text-lg font-bold">Example</span>
    </div>
    <div class="hidden px-2 mx-2 navbar-center lg:flex">
      <div class="flex items-stretch">
        <a class="btn btn-ghost btn-sm rounded-btn" href="/example/1236">Example page</a>
        <a class="btn btn-ghost btn-sm rounded-btn" href="/components/modal#my-modal">Click!</a>
      </div>
    </div>
  </div>

  <div id="my-modal" class="modal">
    <div class="modal-box">
      <p>Yay! Works!</p>
      <div class="modal-action">
        <a href="/components/modal#" class="btn btn-primary">Accept</a>
        <a href="/components/modal#" class="btn">Close</a>
      </div>
    </div>
  </div>

  <select data-choose-theme>
    <option value="light">Light</option>
    <option value="dark">Dark</option>
    <option value="cupcake">Cupcake</option>
    <option value="bumblebee">Bumblebee</option>
    <option value="emerald">Emerald</option>
    <option value="corporate">Corporate</option>
    <option value="synthwave">Synthwave</option>
    <option value="retro">Retro</option>
    <option value="cyberpunk">Cyberpunk</option>
    <option value="valentine">Valentine</option>
    <option value="halloween">Halloween</option>
    <option value="garden">Garden</option>
    <option value="forest">Forest</option>
    <option value="aqua">Aqua</option>
    <option value="lofi">Lofi</option>
    <option value="pastel">Pastel</option>
    <option value="fantasy">Fantasy</option>
    <option value="wireframe">Wireframe</option>
    <option value="black">Black</option>
    <option value="luxury">Luxury</option>
    <option value="dracula">Dracula</option>
    <option value="cmyk">CMYK</option>
  </select>
</div>
