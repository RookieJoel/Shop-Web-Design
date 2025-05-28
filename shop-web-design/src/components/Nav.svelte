<nav>
  <div class="flex justify-between items-center bg-gray-800 p-4">
    <div class="flex items-center space-x-2">
      <div class="drawer md:hidden">
        <input id="my-drawer" type="checkbox" class="drawer-toggle" />
        <div class="drawer-content">
          <label for="my-drawer" class="btn btn-primary drawer-button">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              viewBox="0 0 24 24"
            >
              <path
                fill="currentColor"
                d="M4 18q-.425 0-.712-.288T3 17t.288-.712T4 16h16q.425 0 .713.288T21 17t-.288.713T20 18zm0-5q-.425 0-.712-.288T3 12t.288-.712T4 11h16q.425 0 .713.288T21 12t-.288.713T20 13zm0-5q-.425 0-.712-.288T3 7t.288-.712T4 6h16q.425 0 .713.288T21 7t-.288.713T20 8z"
              />
            </svg>
          </label>
        </div>
        <div class="drawer-side">
          <label
            for="my-drawer"
            aria-label="close sidebar"
            class="drawer-overlay"
          ></label>
          <ul class="menu bg-base-200 text-base-content min-h-full w-80 p-4">
            <li><a>Sidebar Item 1</a></li>
            <li><a>Sidebar Item 2</a></li>
          </ul>
        </div>
      </div>

      <button class="md:hidden text-white focus:outline-none"> </button>

      <div class="text-white text-2xl font-extrabold md:text-center">
        <a href="/">ShopShap</a>
      </div>
    </div>

    <div class="hidden md:flex space-x-4 pl-2">
      <a href="/" class="text-white hover:text-gray-300">Home</a>
      <a href="/products" class="text-white hover:text-gray-300">Products</a>
      <a href="/about" class="text-white hover:text-gray-300">About</a>
      <a href="/contact" class="text-white hover:text-gray-300">Contact</a>
    </div>

    <div class="flex items-center space-x-4">
      <a href="/cart" class="text-white hover:text-gray-300">Cart</a>
      <a href="/login" class="text-white hover:text-gray-300">Login</a>
      <a href="/signup" class="text-white hover:text-gray-300">Sign Up</a>
    </div>
  </div>
</nav>
