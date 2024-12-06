<script>
    import ProductCard from '../components/ProductCard.svelte';
  
    let products = [
      {
        title: 'O2 PURE Oxygen',
        description: 'Oxygen canister, 99.5% pure.',
        price: '฿197',
        image: 'https://via.placeholder.com/150',
        link: '/product/1',
        additionalInfo: 'ขายแล้ว 3.7พัน ชิ้น',
        discount: 5,
      },
      {
        title: 'Air Fryer Gen-S Series',
        description: 'Simplus Air Fryer, 1450W, 10 pcs.',
        price: '฿1190',
        image: 'https://via.placeholder.com/150',
        link: '/product/2',
        additionalInfo: 'ขายแล้ว 926 ชิ้น',
      },
      {
        title: 'Air Fryer Gen-S Series',
        description: 'Simplus Air Fryer, 1450W, 10 pcs.',
        price: '฿1190',
        image: 'https://via.placeholder.com/150',
        link: '/product/2',
        additionalInfo: 'ขายแล้ว 926 ชิ้น',
      },
      {
        title: 'Air Fryer Gen-S Series',
        description: 'Simplus Air Fryer, 1450W, 10 pcs.',
        price: '฿1190',
        image: 'https://via.placeholder.com/150',
        link: '/product/2',
        additionalInfo: 'ขายแล้ว 926 ชิ้น',
      },
      {
        title: 'Air Fryer Gen-S Series',
        description: 'Simplus Air Fryer, 1450W, 10 pcs.',
        price: '฿1190',
        image: 'https://via.placeholder.com/150',
        link: '/product/2',
        additionalInfo: 'ขายแล้ว 926 ชิ้น',
      },
      {
        title: 'Air Fryer Gen-S Series',
        description: 'Simplus Air Fryer, 1450W, 10 pcs.',
        price: '฿1190',
        image: 'https://via.placeholder.com/150',
        link: '/product/2',
        additionalInfo: 'ขายแล้ว 926 ชิ้น',
      },
      {
        title: 'Air Fryer Gen-S Series',
        description: 'Simplus Air Fryer, 1450W, 10 pcs.',
        price: '฿1190',
        image: 'https://via.placeholder.com/150',
        link: '/product/2',
        additionalInfo: 'ขายแล้ว 926 ชิ้น',
      },
      {
        title: 'Air Fryer Gen-S Series',
        description: 'Simplus Air Fryer, 1450W, 10 pcs.',
        price: '฿1190',
        image: 'https://via.placeholder.com/150',
        link: '/product/2',
        additionalInfo: 'ขายแล้ว 926 ชิ้น',
      },
      {
        title: 'Air Fryer Gen-S Series',
        description: 'Simplus Air Fryer, 1450W, 10 pcs.',
        price: '฿1190',
        image: 'https://via.placeholder.com/150',
        link: '/product/2',
        additionalInfo: 'ขายแล้ว 926 ชิ้น',
      },
      {
        title: 'Air Fryer Gen-S Series',
        description: 'Simplus Air Fryer, 1450W, 10 pcs.',
        price: '฿1190',
        image: 'https://via.placeholder.com/150',
        link: '/product/2',
        additionalInfo: 'ขายแล้ว 926 ชิ้น',
      }
      // Add more products as needed
    ];
  </script>
  
  <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-5 gap-8 p-6">
    {#each products as product}
      <ProductCard {product} />
    {/each}
  </div>
  