<script lang="ts">
  import { writable } from "svelte/store";
  import CartContent from "./CartContent.svelte";

  // Define product type
  interface Product {
    id: number;
    name: string;
    articleNr: string;
    color: string;
    size: string;
    price: number;
    quantity: number;
    image: string;
  }

  // Initial cart items
  const cartItems = writable<Product[]>([
    {
      id: 1,
      name: "Basic T-shirt",
      articleNr: "#643489",
      color: "Grey",
      size: "M",
      price: 49,
      quantity: 1,
      image:
        "https://profilewear.se/image/catalog/shop_information/kategori/pw3/T-shirt.png",
    },
    {
      id: 2,
      name: "Basic T-shirt",
      articleNr: "#643489",
      color: "Grey",
      size: "M",
      price: 49,
      quantity: 1,
      image:
        "https://profilewear.se/image/catalog/shop_information/kategori/pw3/T-shirt.png",
    },
    {
      id: 3,
      name: "Basic T-shirt",
      articleNr: "#643489",
      color: "Grey",
      size: "M",
      price: 49,
      quantity: 1,
      image:
        "https://profilewear.se/image/catalog/shop_information/kategori/pw3/T-shirt.png",
    },
    {
      id: 4,
      name: "Basic T-shirt",
      articleNr: "#643489",
      color: "Grey",
      size: "M",
      price: 49,
      quantity: 1,
      image:
        "https://profilewear.se/image/catalog/shop_information/kategori/pw3/T-shirt.png",
    },
    // ... เพิ่มสินค้าได้ตามต้องการ
  ]);

  // Update quantity of a specific item
  function updateQuantity(id: number, newQuantity: number) {
    cartItems.update((items) =>
      items.map((item) =>
        item.id === id ? { ...item, quantity: Math.max(1, newQuantity) } : item
      )
    );
  }

  // Remove item from cart
  function removeItem(id: number) {
    cartItems.update((items) => items.filter((item) => item.id !== id));
  }

  // Calculate total cart value
  $: total = $cartItems.reduce(
    (sum, item) => sum + item.price * item.quantity,
    0
  );
</script>

<div class="container mx-auto px-4 py-8 ">
  <h1 class="text-3xl font-light mb-6">Cart</h1>

  <CartContent {cartItems} {updateQuantity} {removeItem} />

  <div class="mt-6 bg-gray-100 p-4 rounded-lg text-center">
    <div class="text-gray-600 relative pl-8">
      <span class="absolute left-0 text-2xl top-0">↳</span>
      Add some more articles and get discount!!
    </div>
  </div>

  <div class="mt-6 text-right">
    <div class="font-bold text-xl">Total: {total} SEK</div>
  </div>
</div>
