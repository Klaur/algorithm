<template>
  <div>
    <h3>{{ data.title }}</h3>
    <div style="display: flex; gap: 20px">
      <div>
        <img width="400" :src="currenVariant?.featured_image?.src" alt="" srcset="" />
      </div>
      <div style="flex: 1">
        <div class="spec-options" v-for="option in skuSpec" :key="option.position">
          <div>
            {{ option.name }}
            <span :class="{ active: option.value === val.name, disabled: val.disabled }" @click="changeSelectedStatus(option, val)" class="spec-item" v-for="val in option.values" :key="val">
              {{ val.name }}
            </span>
          </div>
        </div>
      </div>
    </div>
    <div>当前选中规格: {{ currenSelected }}</div>
  </div>
</template>
<script setup>
import { ref, computed } from 'vue'
const data = ref({
  id: 7195498184902,
  title: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21',
  handle: 'breastfeeding-seamless-wirefree-nursing-bras',
  description: '',
  published_at: '2022-02-11T01:34:43-05:00',
  created_at: '2022-02-09T23:05:53-05:00',
  vendor: 'Momcozy',
  type: 'Nursing Bras',
  tags: ['_wf_cus', 'bras', 'breastfeeding seamless wireless nursing bras', 'Breastfeeding supplies', 'comfort nursing bra'],
  price: 2999,
  price_min: 2999,
  price_max: 5599,
  available: true,
  price_varies: true,
  compare_at_price: 2999,
  compare_at_price_min: 2999,
  compare_at_price_max: 5998,
  compare_at_price_varies: true,
  variants: [
    {
      id: 41834520969414,
      title: 'Brown / S / Single',
      option1: 'Brown',
      option2: 'S',
      option3: 'Single',
      sku: 'MCMYN21-BRSMAC-SJ',
      requires_shipping: true,
      taxable: true,
      featured_image: {
        id: 37011478708422,
        product_id: 7195498184902,
        position: 1,
        created_at: '2024-06-03T00:14:02-04:00',
        updated_at: '2024-08-01T03:45:20-04:00',
        alt: null,
        width: 992,
        height: 1238,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_ae9a5331-7afc-4dde-abc1-5136e356bcbe.jpg?v=1722498320',
        variant_ids: [41573754667206, 41573754699974, 41573754732742, 41573754765510, 41573754798278, 41834520969414]
      },
      available: true,
      name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Brown / S / Single',
      public_title: 'Brown / S / Single',
      options: ['Brown', 'S', 'Single'],
      price: 2999,
      weight: 150,
      compare_at_price: 2999,
      inventory_management: null,
      barcode: '76709775408',
      featured_media: {
        alt: null,
        id: 29870494482630,
        position: 1,
        preview_image: {
          aspect_ratio: 0.801,
          height: 1238,
          width: 992,
          src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_ae9a5331-7afc-4dde-abc1-5136e356bcbe.jpg?v=1722498320'
        }
      },
      quantity_rule: {
        min: 1,
        max: null,
        increment: 1
      },
      quantity_price_breaks: [],
      requires_selling_plan: false,
      selling_plan_allocations: []
    },
    {
      id: 41573754667206,
      title: 'Brown / M / Single',
      option1: 'Brown',
      option2: 'M',
      option3: 'Single',
      sku: 'MCMYN21-BRMEDC-SJ',
      requires_shipping: true,
      taxable: true,
      featured_image: {
        id: 37011478708422,
        product_id: 7195498184902,
        position: 1,
        created_at: '2024-06-03T00:14:02-04:00',
        updated_at: '2024-08-01T03:45:20-04:00',
        alt: null,
        width: 992,
        height: 1238,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_ae9a5331-7afc-4dde-abc1-5136e356bcbe.jpg?v=1722498320',
        variant_ids: [41573754667206, 41573754699974, 41573754732742, 41573754765510, 41573754798278, 41834520969414]
      },
      available: true,
      name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Brown / M / Single',
      public_title: 'Brown / M / Single',
      options: ['Brown', 'M', 'Single'],
      price: 2999,
      weight: 150,
      compare_at_price: 2999,
      inventory_management: null,
      barcode: '96588676521',
      featured_media: {
        alt: null,
        id: 29870494482630,
        position: 1,
        preview_image: {
          aspect_ratio: 0.801,
          height: 1238,
          width: 992,
          src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_ae9a5331-7afc-4dde-abc1-5136e356bcbe.jpg?v=1722498320'
        }
      },
      quantity_rule: {
        min: 1,
        max: null,
        increment: 1
      },
      quantity_price_breaks: [],
      requires_selling_plan: false,
      selling_plan_allocations: []
    },
    {
      id: 41573754699974,
      title: 'Brown / L / Single',
      option1: 'Brown',
      option2: 'L',
      option3: 'Single',
      sku: 'MCMYN21-BRLARC-SJ',
      requires_shipping: true,
      taxable: true,
      featured_image: {
        id: 37011478708422,
        product_id: 7195498184902,
        position: 1,
        created_at: '2024-06-03T00:14:02-04:00',
        updated_at: '2024-08-01T03:45:20-04:00',
        alt: null,
        width: 992,
        height: 1238,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_ae9a5331-7afc-4dde-abc1-5136e356bcbe.jpg?v=1722498320',
        variant_ids: [41573754667206, 41573754699974, 41573754732742, 41573754765510, 41573754798278, 41834520969414]
      },
      available: true,
      name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Brown / L / Single',
      public_title: 'Brown / L / Single',
      options: ['Brown', 'L', 'Single'],
      price: 2999,
      weight: 150,
      compare_at_price: 2999,
      inventory_management: null,
      barcode: '96588676514',
      featured_media: {
        alt: null,
        id: 29870494482630,
        position: 1,
        preview_image: {
          aspect_ratio: 0.801,
          height: 1238,
          width: 992,
          src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_ae9a5331-7afc-4dde-abc1-5136e356bcbe.jpg?v=1722498320'
        }
      },
      quantity_rule: {
        min: 1,
        max: null,
        increment: 1
      },
      quantity_price_breaks: [],
      requires_selling_plan: false,
      selling_plan_allocations: []
    },
    {
      id: 41573754732742,
      title: 'Brown / XL / Single',
      option1: 'Brown',
      option2: 'XL',
      option3: 'Single',
      sku: 'MCMYN21-BR1XLC-SJ',
      requires_shipping: true,
      taxable: true,
      featured_image: {
        id: 37011478708422,
        product_id: 7195498184902,
        position: 1,
        created_at: '2024-06-03T00:14:02-04:00',
        updated_at: '2024-08-01T03:45:20-04:00',
        alt: null,
        width: 992,
        height: 1238,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_ae9a5331-7afc-4dde-abc1-5136e356bcbe.jpg?v=1722498320',
        variant_ids: [41573754667206, 41573754699974, 41573754732742, 41573754765510, 41573754798278, 41834520969414]
      },
      available: true,
      name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Brown / XL / Single',
      public_title: 'Brown / XL / Single',
      options: ['Brown', 'XL', 'Single'],
      price: 2999,
      weight: 150,
      compare_at_price: 2999,
      inventory_management: null,
      barcode: '96588676507',
      featured_media: {
        alt: null,
        id: 29870494482630,
        position: 1,
        preview_image: {
          aspect_ratio: 0.801,
          height: 1238,
          width: 992,
          src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_ae9a5331-7afc-4dde-abc1-5136e356bcbe.jpg?v=1722498320'
        }
      },
      quantity_rule: {
        min: 1,
        max: null,
        increment: 1
      },
      quantity_price_breaks: [],
      requires_selling_plan: false,
      selling_plan_allocations: []
    },
    {
      id: 41573754765510,
      title: 'Brown / 2XL / Single',
      option1: 'Brown',
      option2: '2XL',
      option3: 'Single',
      sku: 'MCMYN21-BR2XLC-SJ',
      requires_shipping: true,
      taxable: true,
      featured_image: {
        id: 37011478708422,
        product_id: 7195498184902,
        position: 1,
        created_at: '2024-06-03T00:14:02-04:00',
        updated_at: '2024-08-01T03:45:20-04:00',
        alt: null,
        width: 992,
        height: 1238,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_ae9a5331-7afc-4dde-abc1-5136e356bcbe.jpg?v=1722498320',
        variant_ids: [41573754667206, 41573754699974, 41573754732742, 41573754765510, 41573754798278, 41834520969414]
      },
      available: true,
      name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Brown / 2XL / Single',
      public_title: 'Brown / 2XL / Single',
      options: ['Brown', '2XL', 'Single'],
      price: 2999,
      weight: 150,
      compare_at_price: 2999,
      inventory_management: null,
      barcode: '96588676500',
      featured_media: {
        alt: null,
        id: 29870494482630,
        position: 1,
        preview_image: {
          aspect_ratio: 0.801,
          height: 1238,
          width: 992,
          src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_ae9a5331-7afc-4dde-abc1-5136e356bcbe.jpg?v=1722498320'
        }
      },
      quantity_rule: {
        min: 1,
        max: null,
        increment: 1
      },
      quantity_price_breaks: [],
      requires_selling_plan: false,
      selling_plan_allocations: []
    },
    {
      id: 41573754798278,
      title: 'Brown / 3XL / Single',
      option1: 'Brown',
      option2: '3XL',
      option3: 'Single',
      sku: 'MCMYN21-BR3XLC-SJ',
      requires_shipping: true,
      taxable: true,
      featured_image: {
        id: 37011478708422,
        product_id: 7195498184902,
        position: 1,
        created_at: '2024-06-03T00:14:02-04:00',
        updated_at: '2024-08-01T03:45:20-04:00',
        alt: null,
        width: 992,
        height: 1238,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_ae9a5331-7afc-4dde-abc1-5136e356bcbe.jpg?v=1722498320',
        variant_ids: [41573754667206, 41573754699974, 41573754732742, 41573754765510, 41573754798278, 41834520969414]
      },
      available: true,
      name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Brown / 3XL / Single',
      public_title: 'Brown / 3XL / Single',
      options: ['Brown', '3XL', 'Single'],
      price: 2999,
      weight: 150,
      compare_at_price: 2999,
      inventory_management: null,
      barcode: '96588676493',
      featured_media: {
        alt: null,
        id: 29870494482630,
        position: 1,
        preview_image: {
          aspect_ratio: 0.801,
          height: 1238,
          width: 992,
          src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_ae9a5331-7afc-4dde-abc1-5136e356bcbe.jpg?v=1722498320'
        }
      },
      quantity_rule: {
        min: 1,
        max: null,
        increment: 1
      },
      quantity_price_breaks: [],
      requires_selling_plan: false,
      selling_plan_allocations: []
    },
    {
      id: 42717458497734,
      title: 'Brown+Brown / S / Double',
      option1: 'Brown+Brown',
      option2: 'S',
      option3: 'Double',
      sku: 'MCMYN21-LGS-2P',
      requires_shipping: true,
      taxable: true,
      featured_image: {
        id: 35609031770310,
        product_id: 7195498184902,
        position: 47,
        created_at: '2023-06-15T02:25:24-04:00',
        updated_at: '2024-08-01T03:45:20-04:00',
        alt: null,
        width: 992,
        height: 1238,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/YN21_YN21_9d21daf9-d861-40b3-85e1-e840bc62dfd0.jpg?v=1722498320',
        variant_ids: [42717458497734, 42717458563270, 42717458628806, 42717458694342, 42717458759878, 42717458825414]
      },
      available: true,
      name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Brown+Brown / S / Double',
      public_title: 'Brown+Brown / S / Double',
      options: ['Brown+Brown', 'S', 'Double'],
      price: 5398,
      weight: 150,
      compare_at_price: 5998,
      inventory_management: null,
      barcode: '05087157715',
      featured_media: {
        alt: null,
        id: 28252290580678,
        position: 47,
        preview_image: {
          aspect_ratio: 0.801,
          height: 1238,
          width: 992,
          src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/YN21_YN21_9d21daf9-d861-40b3-85e1-e840bc62dfd0.jpg?v=1722498320'
        }
      },
      quantity_rule: {
        min: 1,
        max: null,
        increment: 1
      },
      quantity_price_breaks: [],
      requires_selling_plan: false,
      selling_plan_allocations: []
    },
    // {
    //   id: 42717458563270,
    //   title: 'Brown+Brown / M / Double',
    //   option1: 'Brown+Brown',
    //   option2: 'M',
    //   option3: 'Double',
    //   sku: 'MCMYN21-LGM-2P',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 35609031770310,
    //     product_id: 7195498184902,
    //     position: 47,
    //     created_at: '2023-06-15T02:25:24-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/YN21_YN21_9d21daf9-d861-40b3-85e1-e840bc62dfd0.jpg?v=1722498320',
    //     variant_ids: [42717458497734, 42717458563270, 42717458628806, 42717458694342, 42717458759878, 42717458825414]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Brown+Brown / M / Double',
    //   public_title: 'Brown+Brown / M / Double',
    //   options: ['Brown+Brown', 'M', 'Double'],
    //   price: 5398,
    //   weight: 150,
    //   compare_at_price: 5998,
    //   inventory_management: null,
    //   barcode: '05087157708',
    //   featured_media: {
    //     alt: null,
    //     id: 28252290580678,
    //     position: 47,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/YN21_YN21_9d21daf9-d861-40b3-85e1-e840bc62dfd0.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42717458628806,
    //   title: 'Brown+Brown / L / Double',
    //   option1: 'Brown+Brown',
    //   option2: 'L',
    //   option3: 'Double',
    //   sku: 'MCMYN21-LGL-2P',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 35609031770310,
    //     product_id: 7195498184902,
    //     position: 47,
    //     created_at: '2023-06-15T02:25:24-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/YN21_YN21_9d21daf9-d861-40b3-85e1-e840bc62dfd0.jpg?v=1722498320',
    //     variant_ids: [42717458497734, 42717458563270, 42717458628806, 42717458694342, 42717458759878, 42717458825414]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Brown+Brown / L / Double',
    //   public_title: 'Brown+Brown / L / Double',
    //   options: ['Brown+Brown', 'L', 'Double'],
    //   price: 5398,
    //   weight: 150,
    //   compare_at_price: 5998,
    //   inventory_management: null,
    //   barcode: '05087157701',
    //   featured_media: {
    //     alt: null,
    //     id: 28252290580678,
    //     position: 47,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/YN21_YN21_9d21daf9-d861-40b3-85e1-e840bc62dfd0.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42717458694342,
    //   title: 'Brown+Brown / XL / Double',
    //   option1: 'Brown+Brown',
    //   option2: 'XL',
    //   option3: 'Double',
    //   sku: 'MCMYN21-LG1XL-2P',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 35609031770310,
    //     product_id: 7195498184902,
    //     position: 47,
    //     created_at: '2023-06-15T02:25:24-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/YN21_YN21_9d21daf9-d861-40b3-85e1-e840bc62dfd0.jpg?v=1722498320',
    //     variant_ids: [42717458497734, 42717458563270, 42717458628806, 42717458694342, 42717458759878, 42717458825414]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Brown+Brown / XL / Double',
    //   public_title: 'Brown+Brown / XL / Double',
    //   options: ['Brown+Brown', 'XL', 'Double'],
    //   price: 5398,
    //   weight: 150,
    //   compare_at_price: 5998,
    //   inventory_management: null,
    //   barcode: '05087157694',
    //   featured_media: {
    //     alt: null,
    //     id: 28252290580678,
    //     position: 47,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/YN21_YN21_9d21daf9-d861-40b3-85e1-e840bc62dfd0.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42717458759878,
    //   title: 'Brown+Brown / 2XL / Double',
    //   option1: 'Brown+Brown',
    //   option2: '2XL',
    //   option3: 'Double',
    //   sku: 'MCMYN21-LG2XL-2P',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 35609031770310,
    //     product_id: 7195498184902,
    //     position: 47,
    //     created_at: '2023-06-15T02:25:24-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/YN21_YN21_9d21daf9-d861-40b3-85e1-e840bc62dfd0.jpg?v=1722498320',
    //     variant_ids: [42717458497734, 42717458563270, 42717458628806, 42717458694342, 42717458759878, 42717458825414]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Brown+Brown / 2XL / Double',
    //   public_title: 'Brown+Brown / 2XL / Double',
    //   options: ['Brown+Brown', '2XL', 'Double'],
    //   price: 5398,
    //   weight: 150,
    //   compare_at_price: 5998,
    //   inventory_management: null,
    //   barcode: '05087157687',
    //   featured_media: {
    //     alt: null,
    //     id: 28252290580678,
    //     position: 47,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/YN21_YN21_9d21daf9-d861-40b3-85e1-e840bc62dfd0.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42717458825414,
    //   title: 'Brown+Brown / 3XL / Double',
    //   option1: 'Brown+Brown',
    //   option2: '3XL',
    //   option3: 'Double',
    //   sku: 'MCMYN21-LG3XL-2P',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 35609031770310,
    //     product_id: 7195498184902,
    //     position: 47,
    //     created_at: '2023-06-15T02:25:24-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/YN21_YN21_9d21daf9-d861-40b3-85e1-e840bc62dfd0.jpg?v=1722498320',
    //     variant_ids: [42717458497734, 42717458563270, 42717458628806, 42717458694342, 42717458759878, 42717458825414]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Brown+Brown / 3XL / Double',
    //   public_title: 'Brown+Brown / 3XL / Double',
    //   options: ['Brown+Brown', '3XL', 'Double'],
    //   price: 5398,
    //   weight: 150,
    //   compare_at_price: 5998,
    //   inventory_management: null,
    //   barcode: '25114198896',
    //   featured_media: {
    //     alt: null,
    //     id: 28252290580678,
    //     position: 47,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/YN21_YN21_9d21daf9-d861-40b3-85e1-e840bc62dfd0.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 41834521002182,
    //   title: 'Beige / S / Single',
    //   option1: 'Beige',
    //   option2: 'S',
    //   option3: 'Single',
    //   sku: 'MCMYN21-BGSMAC-SJ',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 37241789579462,
    //     product_id: 7195498184902,
    //     position: 10,
    //     created_at: '2024-07-05T05:38:18-04:00',
    //     updated_at: '2024-07-05T05:38:19-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_b6475688-aada-4566-afb9-0940cd9da26b.png?v=1720172299',
    //     variant_ids: [41573754831046, 41573754863814, 41573754896582, 41573754929350, 41573754962118, 41834521002182]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Beige / S / Single',
    //   public_title: 'Beige / S / Single',
    //   options: ['Beige', 'S', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '76709775450',
    //   featured_media: {
    //     alt: null,
    //     id: 30126020362438,
    //     position: 10,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_b6475688-aada-4566-afb9-0940cd9da26b.png?v=1720172299'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 41573754831046,
    //   title: 'Beige / M / Single',
    //   option1: 'Beige',
    //   option2: 'M',
    //   option3: 'Single',
    //   sku: 'MCMYN21-BGMEDC-SJ',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 37241789579462,
    //     product_id: 7195498184902,
    //     position: 10,
    //     created_at: '2024-07-05T05:38:18-04:00',
    //     updated_at: '2024-07-05T05:38:19-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_b6475688-aada-4566-afb9-0940cd9da26b.png?v=1720172299',
    //     variant_ids: [41573754831046, 41573754863814, 41573754896582, 41573754929350, 41573754962118, 41834521002182]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Beige / M / Single',
    //   public_title: 'Beige / M / Single',
    //   options: ['Beige', 'M', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '76709775443',
    //   featured_media: {
    //     alt: null,
    //     id: 30126020362438,
    //     position: 10,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_b6475688-aada-4566-afb9-0940cd9da26b.png?v=1720172299'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 41573754863814,
    //   title: 'Beige / L / Single',
    //   option1: 'Beige',
    //   option2: 'L',
    //   option3: 'Single',
    //   sku: 'MCMYN21-BGLARC-SJ',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 37241789579462,
    //     product_id: 7195498184902,
    //     position: 10,
    //     created_at: '2024-07-05T05:38:18-04:00',
    //     updated_at: '2024-07-05T05:38:19-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_b6475688-aada-4566-afb9-0940cd9da26b.png?v=1720172299',
    //     variant_ids: [41573754831046, 41573754863814, 41573754896582, 41573754929350, 41573754962118, 41834521002182]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Beige / L / Single',
    //   public_title: 'Beige / L / Single',
    //   options: ['Beige', 'L', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '76709775436',
    //   featured_media: {
    //     alt: null,
    //     id: 30126020362438,
    //     position: 10,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_b6475688-aada-4566-afb9-0940cd9da26b.png?v=1720172299'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 41573754896582,
    //   title: 'Beige / XL / Single',
    //   option1: 'Beige',
    //   option2: 'XL',
    //   option3: 'Single',
    //   sku: 'MCMYN21-BG1XLC-SJ',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 37241789579462,
    //     product_id: 7195498184902,
    //     position: 10,
    //     created_at: '2024-07-05T05:38:18-04:00',
    //     updated_at: '2024-07-05T05:38:19-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_b6475688-aada-4566-afb9-0940cd9da26b.png?v=1720172299',
    //     variant_ids: [41573754831046, 41573754863814, 41573754896582, 41573754929350, 41573754962118, 41834521002182]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Beige / XL / Single',
    //   public_title: 'Beige / XL / Single',
    //   options: ['Beige', 'XL', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '76709775429',
    //   featured_media: {
    //     alt: null,
    //     id: 30126020362438,
    //     position: 10,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_b6475688-aada-4566-afb9-0940cd9da26b.png?v=1720172299'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 41573754929350,
    //   title: 'Beige / 2XL / Single',
    //   option1: 'Beige',
    //   option2: '2XL',
    //   option3: 'Single',
    //   sku: 'MCMYN21-BG2XLC-SJ',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 37241789579462,
    //     product_id: 7195498184902,
    //     position: 10,
    //     created_at: '2024-07-05T05:38:18-04:00',
    //     updated_at: '2024-07-05T05:38:19-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_b6475688-aada-4566-afb9-0940cd9da26b.png?v=1720172299',
    //     variant_ids: [41573754831046, 41573754863814, 41573754896582, 41573754929350, 41573754962118, 41834521002182]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Beige / 2XL / Single',
    //   public_title: 'Beige / 2XL / Single',
    //   options: ['Beige', '2XL', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '76709775422',
    //   featured_media: {
    //     alt: null,
    //     id: 30126020362438,
    //     position: 10,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_b6475688-aada-4566-afb9-0940cd9da26b.png?v=1720172299'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 41573754962118,
    //   title: 'Beige / 3XL / Single',
    //   option1: 'Beige',
    //   option2: '3XL',
    //   option3: 'Single',
    //   sku: 'MCMYN21-BG3XLC-SJ',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 37241789579462,
    //     product_id: 7195498184902,
    //     position: 10,
    //     created_at: '2024-07-05T05:38:18-04:00',
    //     updated_at: '2024-07-05T05:38:19-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_b6475688-aada-4566-afb9-0940cd9da26b.png?v=1720172299',
    //     variant_ids: [41573754831046, 41573754863814, 41573754896582, 41573754929350, 41573754962118, 41834521002182]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Beige / 3XL / Single',
    //   public_title: 'Beige / 3XL / Single',
    //   options: ['Beige', '3XL', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '76709775415',
    //   featured_media: {
    //     alt: null,
    //     id: 30126020362438,
    //     position: 10,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_b6475688-aada-4566-afb9-0940cd9da26b.png?v=1720172299'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42489555353798,
    //   title: 'Black / S / Single',
    //   option1: 'Black',
    //   option2: 'S',
    //   option3: 'Single',
    //   sku: 'MCCFB21-BLSMAC-SJ',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 33334141288646,
    //     product_id: 7195498184902,
    //     position: 20,
    //     created_at: '2022-05-19T07:45:29-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: 'Seamless Nursing Bras',
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/SeamlessNursingBras_8cdf7116-ffe8-4624-96f1-1b17ad5b561e.jpg?v=1722498320',
    //     variant_ids: [42489555353798, 42489555386566, 42489555419334, 42489555452102, 42489555484870, 42489555517638]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Black / S / Single',
    //   public_title: 'Black / S / Single',
    //   options: ['Black', 'S', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '96588676486',
    //   featured_media: {
    //     alt: 'Seamless Nursing Bras',
    //     id: 25707902173382,
    //     position: 20,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/SeamlessNursingBras_8cdf7116-ffe8-4624-96f1-1b17ad5b561e.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42489555386566,
    //   title: 'Black / M / Single',
    //   option1: 'Black',
    //   option2: 'M',
    //   option3: 'Single',
    //   sku: 'MCMYN21-BLMEDC-SJ',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 33334141288646,
    //     product_id: 7195498184902,
    //     position: 20,
    //     created_at: '2022-05-19T07:45:29-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: 'Seamless Nursing Bras',
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/SeamlessNursingBras_8cdf7116-ffe8-4624-96f1-1b17ad5b561e.jpg?v=1722498320',
    //     variant_ids: [42489555353798, 42489555386566, 42489555419334, 42489555452102, 42489555484870, 42489555517638]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Black / M / Single',
    //   public_title: 'Black / M / Single',
    //   options: ['Black', 'M', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '96588676479',
    //   featured_media: {
    //     alt: 'Seamless Nursing Bras',
    //     id: 25707902173382,
    //     position: 20,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/SeamlessNursingBras_8cdf7116-ffe8-4624-96f1-1b17ad5b561e.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42489555419334,
    //   title: 'Black / L / Single',
    //   option1: 'Black',
    //   option2: 'L',
    //   option3: 'Single',
    //   sku: 'MCMYN21-BLLARC-SJ',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 33334141288646,
    //     product_id: 7195498184902,
    //     position: 20,
    //     created_at: '2022-05-19T07:45:29-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: 'Seamless Nursing Bras',
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/SeamlessNursingBras_8cdf7116-ffe8-4624-96f1-1b17ad5b561e.jpg?v=1722498320',
    //     variant_ids: [42489555353798, 42489555386566, 42489555419334, 42489555452102, 42489555484870, 42489555517638]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Black / L / Single',
    //   public_title: 'Black / L / Single',
    //   options: ['Black', 'L', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '96588676472',
    //   featured_media: {
    //     alt: 'Seamless Nursing Bras',
    //     id: 25707902173382,
    //     position: 20,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/SeamlessNursingBras_8cdf7116-ffe8-4624-96f1-1b17ad5b561e.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42489555452102,
    //   title: 'Black / XL / Single',
    //   option1: 'Black',
    //   option2: 'XL',
    //   option3: 'Single',
    //   sku: 'MCMYN21-BL1XLC-SJ',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 33334141288646,
    //     product_id: 7195498184902,
    //     position: 20,
    //     created_at: '2022-05-19T07:45:29-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: 'Seamless Nursing Bras',
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/SeamlessNursingBras_8cdf7116-ffe8-4624-96f1-1b17ad5b561e.jpg?v=1722498320',
    //     variant_ids: [42489555353798, 42489555386566, 42489555419334, 42489555452102, 42489555484870, 42489555517638]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Black / XL / Single',
    //   public_title: 'Black / XL / Single',
    //   options: ['Black', 'XL', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '96588676465',
    //   featured_media: {
    //     alt: 'Seamless Nursing Bras',
    //     id: 25707902173382,
    //     position: 20,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/SeamlessNursingBras_8cdf7116-ffe8-4624-96f1-1b17ad5b561e.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42489555484870,
    //   title: 'Black / 2XL / Single',
    //   option1: 'Black',
    //   option2: '2XL',
    //   option3: 'Single',
    //   sku: 'MCMYN21-BL2XLC-SJ',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 33334141288646,
    //     product_id: 7195498184902,
    //     position: 20,
    //     created_at: '2022-05-19T07:45:29-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: 'Seamless Nursing Bras',
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/SeamlessNursingBras_8cdf7116-ffe8-4624-96f1-1b17ad5b561e.jpg?v=1722498320',
    //     variant_ids: [42489555353798, 42489555386566, 42489555419334, 42489555452102, 42489555484870, 42489555517638]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Black / 2XL / Single',
    //   public_title: 'Black / 2XL / Single',
    //   options: ['Black', '2XL', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '96588676458',
    //   featured_media: {
    //     alt: 'Seamless Nursing Bras',
    //     id: 25707902173382,
    //     position: 20,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/SeamlessNursingBras_8cdf7116-ffe8-4624-96f1-1b17ad5b561e.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42489555517638,
    //   title: 'Black / 3XL / Single',
    //   option1: 'Black',
    //   option2: '3XL',
    //   option3: 'Single',
    //   sku: 'MCMYN21-BL3XLC-SJ',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 33334141288646,
    //     product_id: 7195498184902,
    //     position: 20,
    //     created_at: '2022-05-19T07:45:29-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: 'Seamless Nursing Bras',
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/SeamlessNursingBras_8cdf7116-ffe8-4624-96f1-1b17ad5b561e.jpg?v=1722498320',
    //     variant_ids: [42489555353798, 42489555386566, 42489555419334, 42489555452102, 42489555484870, 42489555517638]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Black / 3XL / Single',
    //   public_title: 'Black / 3XL / Single',
    //   options: ['Black', '3XL', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '41912483390',
    //   featured_media: {
    //     alt: 'Seamless Nursing Bras',
    //     id: 25707902173382,
    //     position: 20,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/SeamlessNursingBras_8cdf7116-ffe8-4624-96f1-1b17ad5b561e.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42939471855814,
    //   title: 'Shallow Brown / S / Single',
    //   option1: 'Shallow Brown',
    //   option2: 'S',
    //   option3: 'Single',
    //   sku: 'FB021-LO100S-A',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 36033205764294,
    //     product_id: 7195498184902,
    //     position: 30,
    //     created_at: '2023-11-21T20:37:06-05:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_5ebca54b-3cfc-4445-8830-da38f93d3ddd.jpg?v=1722498320',
    //     variant_ids: [42939471855814, 42939471921350, 42939471986886, 42939472052422, 42939472117958, 42939472183494]
    //   },
    //   available: false,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Shallow Brown / S / Single',
    //   public_title: 'Shallow Brown / S / Single',
    //   options: ['Shallow Brown', 'S', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: 'shopify',
    //   barcode: '82878400295',
    //   featured_media: {
    //     alt: null,
    //     id: 28752281403590,
    //     position: 30,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_5ebca54b-3cfc-4445-8830-da38f93d3ddd.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42939471921350,
    //   title: 'Shallow Brown / M / Single',
    //   option1: 'Shallow Brown',
    //   option2: 'M',
    //   option3: 'Single',
    //   sku: 'FB021-LO200M-A',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 36033205764294,
    //     product_id: 7195498184902,
    //     position: 30,
    //     created_at: '2023-11-21T20:37:06-05:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_5ebca54b-3cfc-4445-8830-da38f93d3ddd.jpg?v=1722498320',
    //     variant_ids: [42939471855814, 42939471921350, 42939471986886, 42939472052422, 42939472117958, 42939472183494]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Shallow Brown / M / Single',
    //   public_title: 'Shallow Brown / M / Single',
    //   options: ['Shallow Brown', 'M', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '05087157750',
    //   featured_media: {
    //     alt: null,
    //     id: 28752281403590,
    //     position: 30,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_5ebca54b-3cfc-4445-8830-da38f93d3ddd.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42939471986886,
    //   title: 'Shallow Brown / L / Single',
    //   option1: 'Shallow Brown',
    //   option2: 'L',
    //   option3: 'Single',
    //   sku: 'FB021-LO200L-A',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 36033205764294,
    //     product_id: 7195498184902,
    //     position: 30,
    //     created_at: '2023-11-21T20:37:06-05:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_5ebca54b-3cfc-4445-8830-da38f93d3ddd.jpg?v=1722498320',
    //     variant_ids: [42939471855814, 42939471921350, 42939471986886, 42939472052422, 42939472117958, 42939472183494]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Shallow Brown / L / Single',
    //   public_title: 'Shallow Brown / L / Single',
    //   options: ['Shallow Brown', 'L', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '05087157743',
    //   featured_media: {
    //     alt: null,
    //     id: 28752281403590,
    //     position: 30,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_5ebca54b-3cfc-4445-8830-da38f93d3ddd.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42939472052422,
    //   title: 'Shallow Brown / XL / Single',
    //   option1: 'Shallow Brown',
    //   option2: 'XL',
    //   option3: 'Single',
    //   sku: 'FB021-LO21XL-A',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 36033205764294,
    //     product_id: 7195498184902,
    //     position: 30,
    //     created_at: '2023-11-21T20:37:06-05:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_5ebca54b-3cfc-4445-8830-da38f93d3ddd.jpg?v=1722498320',
    //     variant_ids: [42939471855814, 42939471921350, 42939471986886, 42939472052422, 42939472117958, 42939472183494]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Shallow Brown / XL / Single',
    //   public_title: 'Shallow Brown / XL / Single',
    //   options: ['Shallow Brown', 'XL', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '05087157736',
    //   featured_media: {
    //     alt: null,
    //     id: 28752281403590,
    //     position: 30,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_5ebca54b-3cfc-4445-8830-da38f93d3ddd.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42939472117958,
    //   title: 'Shallow Brown / 2XL / Single',
    //   option1: 'Shallow Brown',
    //   option2: '2XL',
    //   option3: 'Single',
    //   sku: 'FB021-LO22XL-A',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 36033205764294,
    //     product_id: 7195498184902,
    //     position: 30,
    //     created_at: '2023-11-21T20:37:06-05:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_5ebca54b-3cfc-4445-8830-da38f93d3ddd.jpg?v=1722498320',
    //     variant_ids: [42939471855814, 42939471921350, 42939471986886, 42939472052422, 42939472117958, 42939472183494]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Shallow Brown / 2XL / Single',
    //   public_title: 'Shallow Brown / 2XL / Single',
    //   options: ['Shallow Brown', '2XL', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '05087157729',
    //   featured_media: {
    //     alt: null,
    //     id: 28752281403590,
    //     position: 30,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_5ebca54b-3cfc-4445-8830-da38f93d3ddd.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42939472183494,
    //   title: 'Shallow Brown / 3XL / Single',
    //   option1: 'Shallow Brown',
    //   option2: '3XL',
    //   option3: 'Single',
    //   sku: 'FB021-LO23XL-A',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 36033205764294,
    //     product_id: 7195498184902,
    //     position: 30,
    //     created_at: '2023-11-21T20:37:06-05:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_5ebca54b-3cfc-4445-8830-da38f93d3ddd.jpg?v=1722498320',
    //     variant_ids: [42939471855814, 42939471921350, 42939471986886, 42939472052422, 42939472117958, 42939472183494]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Shallow Brown / 3XL / Single',
    //   public_title: 'Shallow Brown / 3XL / Single',
    //   options: ['Shallow Brown', '3XL', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '05087157722',
    //   featured_media: {
    //     alt: null,
    //     id: 28752281403590,
    //     position: 30,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_5ebca54b-3cfc-4445-8830-da38f93d3ddd.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42939471462598,
    //   title: 'Light Grey / S / Single',
    //   option1: 'Light Grey',
    //   option2: 'S',
    //   option3: 'Single',
    //   sku: 'FB021-LG100S-A',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 36033206780102,
    //     product_id: 7195498184902,
    //     position: 36,
    //     created_at: '2023-11-21T20:37:36-05:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_1825383e-3852-4d82-8ba7-52cefe41612e.jpg?v=1722498320',
    //     variant_ids: [42939471462598, 42939471528134, 42939471593670, 42939471659206, 42939471724742, 42939471790278]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Light Grey / S / Single',
    //   public_title: 'Light Grey / S / Single',
    //   options: ['Light Grey', 'S', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '41912483383',
    //   featured_media: {
    //     alt: null,
    //     id: 28752283107526,
    //     position: 36,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_1825383e-3852-4d82-8ba7-52cefe41612e.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42939471528134,
    //   title: 'Light Grey / M / Single',
    //   option1: 'Light Grey',
    //   option2: 'M',
    //   option3: 'Single',
    //   sku: 'FB021-LG100M-A',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 36033206780102,
    //     product_id: 7195498184902,
    //     position: 36,
    //     created_at: '2023-11-21T20:37:36-05:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_1825383e-3852-4d82-8ba7-52cefe41612e.jpg?v=1722498320',
    //     variant_ids: [42939471462598, 42939471528134, 42939471593670, 42939471659206, 42939471724742, 42939471790278]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Light Grey / M / Single',
    //   public_title: 'Light Grey / M / Single',
    //   options: ['Light Grey', 'M', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '41912483376',
    //   featured_media: {
    //     alt: null,
    //     id: 28752283107526,
    //     position: 36,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_1825383e-3852-4d82-8ba7-52cefe41612e.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42939471593670,
    //   title: 'Light Grey / L / Single',
    //   option1: 'Light Grey',
    //   option2: 'L',
    //   option3: 'Single',
    //   sku: 'FB021-LG100L-A',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 36033206780102,
    //     product_id: 7195498184902,
    //     position: 36,
    //     created_at: '2023-11-21T20:37:36-05:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_1825383e-3852-4d82-8ba7-52cefe41612e.jpg?v=1722498320',
    //     variant_ids: [42939471462598, 42939471528134, 42939471593670, 42939471659206, 42939471724742, 42939471790278]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Light Grey / L / Single',
    //   public_title: 'Light Grey / L / Single',
    //   options: ['Light Grey', 'L', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '41912483369',
    //   featured_media: {
    //     alt: null,
    //     id: 28752283107526,
    //     position: 36,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_1825383e-3852-4d82-8ba7-52cefe41612e.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42939471659206,
    //   title: 'Light Grey / XL / Single',
    //   option1: 'Light Grey',
    //   option2: 'XL',
    //   option3: 'Single',
    //   sku: 'FB021-LG11XL-A',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 36033206780102,
    //     product_id: 7195498184902,
    //     position: 36,
    //     created_at: '2023-11-21T20:37:36-05:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_1825383e-3852-4d82-8ba7-52cefe41612e.jpg?v=1722498320',
    //     variant_ids: [42939471462598, 42939471528134, 42939471593670, 42939471659206, 42939471724742, 42939471790278]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Light Grey / XL / Single',
    //   public_title: 'Light Grey / XL / Single',
    //   options: ['Light Grey', 'XL', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '41912483362',
    //   featured_media: {
    //     alt: null,
    //     id: 28752283107526,
    //     position: 36,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_1825383e-3852-4d82-8ba7-52cefe41612e.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42939471724742,
    //   title: 'Light Grey / 2XL / Single',
    //   option1: 'Light Grey',
    //   option2: '2XL',
    //   option3: 'Single',
    //   sku: 'FB021-LG12XL-A',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 36033206780102,
    //     product_id: 7195498184902,
    //     position: 36,
    //     created_at: '2023-11-21T20:37:36-05:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_1825383e-3852-4d82-8ba7-52cefe41612e.jpg?v=1722498320',
    //     variant_ids: [42939471462598, 42939471528134, 42939471593670, 42939471659206, 42939471724742, 42939471790278]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Light Grey / 2XL / Single',
    //   public_title: 'Light Grey / 2XL / Single',
    //   options: ['Light Grey', '2XL', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '41912483355',
    //   featured_media: {
    //     alt: null,
    //     id: 28752283107526,
    //     position: 36,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_1825383e-3852-4d82-8ba7-52cefe41612e.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42939471790278,
    //   title: 'Light Grey / 3XL / Single',
    //   option1: 'Light Grey',
    //   option2: '3XL',
    //   option3: 'Single',
    //   sku: 'FB021-LG13XL-A',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 36033206780102,
    //     product_id: 7195498184902,
    //     position: 36,
    //     created_at: '2023-11-21T20:37:36-05:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_1825383e-3852-4d82-8ba7-52cefe41612e.jpg?v=1722498320',
    //     variant_ids: [42939471462598, 42939471528134, 42939471593670, 42939471659206, 42939471724742, 42939471790278]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Light Grey / 3XL / Single',
    //   public_title: 'Light Grey / 3XL / Single',
    //   options: ['Light Grey', '3XL', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '41912483348',
    //   featured_media: {
    //     alt: null,
    //     id: 28752283107526,
    //     position: 36,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_1825383e-3852-4d82-8ba7-52cefe41612e.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42253849166022,
    //   title: 'Cream / S / Single',
    //   option1: 'Cream',
    //   option2: 'S',
    //   option3: 'Single',
    //   sku: 'MCMYN21-CRSMAC-SJ',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 33889886798022,
    //     product_id: 7195498184902,
    //     position: 23,
    //     created_at: '2022-07-06T22:41:13-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_1.jpg?v=1722498320',
    //     variant_ids: [42253849166022, 42253849198790, 42253849231558, 42253849264326, 42253849297094, 42253849329862]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Cream / S / Single',
    //   public_title: 'Cream / S / Single',
    //   options: ['Cream', 'S', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '41912483341',
    //   featured_media: {
    //     alt: null,
    //     id: 26332494037190,
    //     position: 23,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_1.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42253849198790,
    //   title: 'Cream / M / Single',
    //   option1: 'Cream',
    //   option2: 'M',
    //   option3: 'Single',
    //   sku: 'MCMYN21-CRMEDC-SJ',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 33889886798022,
    //     product_id: 7195498184902,
    //     position: 23,
    //     created_at: '2022-07-06T22:41:13-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_1.jpg?v=1722498320',
    //     variant_ids: [42253849166022, 42253849198790, 42253849231558, 42253849264326, 42253849297094, 42253849329862]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Cream / M / Single',
    //   public_title: 'Cream / M / Single',
    //   options: ['Cream', 'M', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '41912483334',
    //   featured_media: {
    //     alt: null,
    //     id: 26332494037190,
    //     position: 23,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_1.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42253849231558,
    //   title: 'Cream / L / Single',
    //   option1: 'Cream',
    //   option2: 'L',
    //   option3: 'Single',
    //   sku: 'MCMYN21-CRLARC-SJ',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 33889886798022,
    //     product_id: 7195498184902,
    //     position: 23,
    //     created_at: '2022-07-06T22:41:13-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_1.jpg?v=1722498320',
    //     variant_ids: [42253849166022, 42253849198790, 42253849231558, 42253849264326, 42253849297094, 42253849329862]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Cream / L / Single',
    //   public_title: 'Cream / L / Single',
    //   options: ['Cream', 'L', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '41912483327',
    //   featured_media: {
    //     alt: null,
    //     id: 26332494037190,
    //     position: 23,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_1.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42253849264326,
    //   title: 'Cream / XL / Single',
    //   option1: 'Cream',
    //   option2: 'XL',
    //   option3: 'Single',
    //   sku: 'MCMYN21-CR1XLC-SJ',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 33889886798022,
    //     product_id: 7195498184902,
    //     position: 23,
    //     created_at: '2022-07-06T22:41:13-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_1.jpg?v=1722498320',
    //     variant_ids: [42253849166022, 42253849198790, 42253849231558, 42253849264326, 42253849297094, 42253849329862]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Cream / XL / Single',
    //   public_title: 'Cream / XL / Single',
    //   options: ['Cream', 'XL', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '82878400358',
    //   featured_media: {
    //     alt: null,
    //     id: 26332494037190,
    //     position: 23,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_1.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42253849297094,
    //   title: 'Cream / 2XL / Single',
    //   option1: 'Cream',
    //   option2: '2XL',
    //   option3: 'Single',
    //   sku: 'MCMYN21-CR2XLC-SJ',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 33889886798022,
    //     product_id: 7195498184902,
    //     position: 23,
    //     created_at: '2022-07-06T22:41:13-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_1.jpg?v=1722498320',
    //     variant_ids: [42253849166022, 42253849198790, 42253849231558, 42253849264326, 42253849297094, 42253849329862]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Cream / 2XL / Single',
    //   public_title: 'Cream / 2XL / Single',
    //   options: ['Cream', '2XL', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '82878400351',
    //   featured_media: {
    //     alt: null,
    //     id: 26332494037190,
    //     position: 23,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_1.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42253849329862,
    //   title: 'Cream / 3XL / Single',
    //   option1: 'Cream',
    //   option2: '3XL',
    //   option3: 'Single',
    //   sku: 'MCMYN21-CR3XLC-SJ',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 33889886798022,
    //     product_id: 7195498184902,
    //     position: 23,
    //     created_at: '2022-07-06T22:41:13-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_1.jpg?v=1722498320',
    //     variant_ids: [42253849166022, 42253849198790, 42253849231558, 42253849264326, 42253849297094, 42253849329862]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Cream / 3XL / Single',
    //   public_title: 'Cream / 3XL / Single',
    //   options: ['Cream', '3XL', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '82878400344',
    //   featured_media: {
    //     alt: null,
    //     id: 26332494037190,
    //     position: 23,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_1.jpg?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 44001224491206,
    //   title: 'Maple Sugar / S / Single',
    //   option1: 'Maple Sugar',
    //   option2: 'S',
    //   option3: 'Single',
    //   sku: 'FB021-MS100S-B',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 37493762785478,
    //     product_id: 7195498184902,
    //     position: 51,
    //     created_at: '2024-08-04T23:32:13-04:00',
    //     updated_at: '2024-08-04T23:32:15-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/IMG_202408057027_992x1238_8a9eff32-c493-49f1-a505-1e28ba1d4152.jpg?v=1722828735',
    //     variant_ids: [44001224491206, 44001224556742, 44001224622278, 44001224687814, 44001224753350, 44001224818886]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Maple Sugar / S / Single',
    //   public_title: 'Maple Sugar / S / Single',
    //   options: ['Maple Sugar', 'S', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '82878400337',
    //   featured_media: {
    //     alt: null,
    //     id: 30299886682310,
    //     position: 51,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/IMG_202408057027_992x1238_8a9eff32-c493-49f1-a505-1e28ba1d4152.jpg?v=1722828735'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 44001224556742,
    //   title: 'Maple Sugar / M / Single',
    //   option1: 'Maple Sugar',
    //   option2: 'M',
    //   option3: 'Single',
    //   sku: 'FB021-MS100M-B',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 37493762785478,
    //     product_id: 7195498184902,
    //     position: 51,
    //     created_at: '2024-08-04T23:32:13-04:00',
    //     updated_at: '2024-08-04T23:32:15-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/IMG_202408057027_992x1238_8a9eff32-c493-49f1-a505-1e28ba1d4152.jpg?v=1722828735',
    //     variant_ids: [44001224491206, 44001224556742, 44001224622278, 44001224687814, 44001224753350, 44001224818886]
    //   },
    //   available: false,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Maple Sugar / M / Single',
    //   public_title: 'Maple Sugar / M / Single',
    //   options: ['Maple Sugar', 'M', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: 'shopify',
    //   barcode: '82878400330',
    //   featured_media: {
    //     alt: null,
    //     id: 30299886682310,
    //     position: 51,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/IMG_202408057027_992x1238_8a9eff32-c493-49f1-a505-1e28ba1d4152.jpg?v=1722828735'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 44001224622278,
    //   title: 'Maple Sugar / L / Single',
    //   option1: 'Maple Sugar',
    //   option2: 'L',
    //   option3: 'Single',
    //   sku: 'FB021-MS100L-B',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 37493762785478,
    //     product_id: 7195498184902,
    //     position: 51,
    //     created_at: '2024-08-04T23:32:13-04:00',
    //     updated_at: '2024-08-04T23:32:15-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/IMG_202408057027_992x1238_8a9eff32-c493-49f1-a505-1e28ba1d4152.jpg?v=1722828735',
    //     variant_ids: [44001224491206, 44001224556742, 44001224622278, 44001224687814, 44001224753350, 44001224818886]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Maple Sugar / L / Single',
    //   public_title: 'Maple Sugar / L / Single',
    //   options: ['Maple Sugar', 'L', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '82878400323',
    //   featured_media: {
    //     alt: null,
    //     id: 30299886682310,
    //     position: 51,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/IMG_202408057027_992x1238_8a9eff32-c493-49f1-a505-1e28ba1d4152.jpg?v=1722828735'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 44001224687814,
    //   title: 'Maple Sugar / XL / Single',
    //   option1: 'Maple Sugar',
    //   option2: 'XL',
    //   option3: 'Single',
    //   sku: 'FB021-MS11XL-B',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 37493762785478,
    //     product_id: 7195498184902,
    //     position: 51,
    //     created_at: '2024-08-04T23:32:13-04:00',
    //     updated_at: '2024-08-04T23:32:15-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/IMG_202408057027_992x1238_8a9eff32-c493-49f1-a505-1e28ba1d4152.jpg?v=1722828735',
    //     variant_ids: [44001224491206, 44001224556742, 44001224622278, 44001224687814, 44001224753350, 44001224818886]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Maple Sugar / XL / Single',
    //   public_title: 'Maple Sugar / XL / Single',
    //   options: ['Maple Sugar', 'XL', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '82878400316',
    //   featured_media: {
    //     alt: null,
    //     id: 30299886682310,
    //     position: 51,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/IMG_202408057027_992x1238_8a9eff32-c493-49f1-a505-1e28ba1d4152.jpg?v=1722828735'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 44001224753350,
    //   title: 'Maple Sugar / 2XL / Single',
    //   option1: 'Maple Sugar',
    //   option2: '2XL',
    //   option3: 'Single',
    //   sku: 'FB021-MS12XL-B',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 37493762785478,
    //     product_id: 7195498184902,
    //     position: 51,
    //     created_at: '2024-08-04T23:32:13-04:00',
    //     updated_at: '2024-08-04T23:32:15-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/IMG_202408057027_992x1238_8a9eff32-c493-49f1-a505-1e28ba1d4152.jpg?v=1722828735',
    //     variant_ids: [44001224491206, 44001224556742, 44001224622278, 44001224687814, 44001224753350, 44001224818886]
    //   },
    //   available: false,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Maple Sugar / 2XL / Single',
    //   public_title: 'Maple Sugar / 2XL / Single',
    //   options: ['Maple Sugar', '2XL', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: 'shopify',
    //   barcode: '82878400309',
    //   featured_media: {
    //     alt: null,
    //     id: 30299886682310,
    //     position: 51,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/IMG_202408057027_992x1238_8a9eff32-c493-49f1-a505-1e28ba1d4152.jpg?v=1722828735'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 44001224818886,
    //   title: 'Maple Sugar / 3XL / Single',
    //   option1: 'Maple Sugar',
    //   option2: '3XL',
    //   option3: 'Single',
    //   sku: 'FB021-MS13XL-B',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 37493762785478,
    //     product_id: 7195498184902,
    //     position: 51,
    //     created_at: '2024-08-04T23:32:13-04:00',
    //     updated_at: '2024-08-04T23:32:15-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/IMG_202408057027_992x1238_8a9eff32-c493-49f1-a505-1e28ba1d4152.jpg?v=1722828735',
    //     variant_ids: [44001224491206, 44001224556742, 44001224622278, 44001224687814, 44001224753350, 44001224818886]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Maple Sugar / 3XL / Single',
    //   public_title: 'Maple Sugar / 3XL / Single',
    //   options: ['Maple Sugar', '3XL', 'Single'],
    //   price: 2999,
    //   weight: 150,
    //   compare_at_price: 2999,
    //   inventory_management: null,
    //   barcode: '82878400302',
    //   featured_media: {
    //     alt: null,
    //     id: 30299886682310,
    //     position: 51,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/IMG_202408057027_992x1238_8a9eff32-c493-49f1-a505-1e28ba1d4152.jpg?v=1722828735'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42717459284166,
    //   title: 'Brown+Black / S / Double',
    //   option1: 'Brown+Black',
    //   option2: 'S',
    //   option3: 'Double',
    //   sku: 'MCMFB21-BRSBL-2P',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 35609034719430,
    //     product_id: 7195498184902,
    //     position: 49,
    //     created_at: '2023-06-15T02:25:51-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_3_8656d32e-3a42-4463-ae1d-8f2258406f54.png?v=1722498320',
    //     variant_ids: [42717459284166, 42717459349702, 42717459415238, 42717459480774, 42717459546310, 42717459611846]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Brown+Black / S / Double',
    //   public_title: 'Brown+Black / S / Double',
    //   options: ['Brown+Black', 'S', 'Double'],
    //   price: 5599,
    //   weight: 150,
    //   compare_at_price: 5998,
    //   inventory_management: null,
    //   barcode: '25114198889',
    //   featured_media: {
    //     alt: null,
    //     id: 28252293497030,
    //     position: 49,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_3_8656d32e-3a42-4463-ae1d-8f2258406f54.png?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42717459349702,
    //   title: 'Brown+Black / M / Double',
    //   option1: 'Brown+Black',
    //   option2: 'M',
    //   option3: 'Double',
    //   sku: 'MCMFB21-BRMBL-2P',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 35609034719430,
    //     product_id: 7195498184902,
    //     position: 49,
    //     created_at: '2023-06-15T02:25:51-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_3_8656d32e-3a42-4463-ae1d-8f2258406f54.png?v=1722498320',
    //     variant_ids: [42717459284166, 42717459349702, 42717459415238, 42717459480774, 42717459546310, 42717459611846]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Brown+Black / M / Double',
    //   public_title: 'Brown+Black / M / Double',
    //   options: ['Brown+Black', 'M', 'Double'],
    //   price: 5599,
    //   weight: 150,
    //   compare_at_price: 5998,
    //   inventory_management: null,
    //   barcode: '25114198882',
    //   featured_media: {
    //     alt: null,
    //     id: 28252293497030,
    //     position: 49,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_3_8656d32e-3a42-4463-ae1d-8f2258406f54.png?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42717459415238,
    //   title: 'Brown+Black / L / Double',
    //   option1: 'Brown+Black',
    //   option2: 'L',
    //   option3: 'Double',
    //   sku: 'MCMFB21-BRLBL-2P',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 35609034719430,
    //     product_id: 7195498184902,
    //     position: 49,
    //     created_at: '2023-06-15T02:25:51-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_3_8656d32e-3a42-4463-ae1d-8f2258406f54.png?v=1722498320',
    //     variant_ids: [42717459284166, 42717459349702, 42717459415238, 42717459480774, 42717459546310, 42717459611846]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Brown+Black / L / Double',
    //   public_title: 'Brown+Black / L / Double',
    //   options: ['Brown+Black', 'L', 'Double'],
    //   price: 5599,
    //   weight: 150,
    //   compare_at_price: 5998,
    //   inventory_management: null,
    //   barcode: '25114198875',
    //   featured_media: {
    //     alt: null,
    //     id: 28252293497030,
    //     position: 49,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_3_8656d32e-3a42-4463-ae1d-8f2258406f54.png?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42717459480774,
    //   title: 'Brown+Black / XL / Double',
    //   option1: 'Brown+Black',
    //   option2: 'XL',
    //   option3: 'Double',
    //   sku: 'MCMFB21-BRXLBL-2P',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 35609034719430,
    //     product_id: 7195498184902,
    //     position: 49,
    //     created_at: '2023-06-15T02:25:51-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_3_8656d32e-3a42-4463-ae1d-8f2258406f54.png?v=1722498320',
    //     variant_ids: [42717459284166, 42717459349702, 42717459415238, 42717459480774, 42717459546310, 42717459611846]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Brown+Black / XL / Double',
    //   public_title: 'Brown+Black / XL / Double',
    //   options: ['Brown+Black', 'XL', 'Double'],
    //   price: 5599,
    //   weight: 150,
    //   compare_at_price: 5998,
    //   inventory_management: null,
    //   barcode: '25114198868',
    //   featured_media: {
    //     alt: null,
    //     id: 28252293497030,
    //     position: 49,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_3_8656d32e-3a42-4463-ae1d-8f2258406f54.png?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42717459546310,
    //   title: 'Brown+Black / 2XL / Double',
    //   option1: 'Brown+Black',
    //   option2: '2XL',
    //   option3: 'Double',
    //   sku: 'MCMFB21-BR2XLBL-2P',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 35609034719430,
    //     product_id: 7195498184902,
    //     position: 49,
    //     created_at: '2023-06-15T02:25:51-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_3_8656d32e-3a42-4463-ae1d-8f2258406f54.png?v=1722498320',
    //     variant_ids: [42717459284166, 42717459349702, 42717459415238, 42717459480774, 42717459546310, 42717459611846]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Brown+Black / 2XL / Double',
    //   public_title: 'Brown+Black / 2XL / Double',
    //   options: ['Brown+Black', '2XL', 'Double'],
    //   price: 5599,
    //   weight: 150,
    //   compare_at_price: 5998,
    //   inventory_management: null,
    //   barcode: '25114198861',
    //   featured_media: {
    //     alt: null,
    //     id: 28252293497030,
    //     position: 49,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_3_8656d32e-3a42-4463-ae1d-8f2258406f54.png?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42717459611846,
    //   title: 'Brown+Black / 3XL / Double',
    //   option1: 'Brown+Black',
    //   option2: '3XL',
    //   option3: 'Double',
    //   sku: 'MCMFB21-BR3XLBL-2P',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 35609034719430,
    //     product_id: 7195498184902,
    //     position: 49,
    //     created_at: '2023-06-15T02:25:51-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_3_8656d32e-3a42-4463-ae1d-8f2258406f54.png?v=1722498320',
    //     variant_ids: [42717459284166, 42717459349702, 42717459415238, 42717459480774, 42717459546310, 42717459611846]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Brown+Black / 3XL / Double',
    //   public_title: 'Brown+Black / 3XL / Double',
    //   options: ['Brown+Black', '3XL', 'Double'],
    //   price: 5599,
    //   weight: 150,
    //   compare_at_price: 5998,
    //   inventory_management: null,
    //   barcode: '25114198854',
    //   featured_media: {
    //     alt: null,
    //     id: 28252293497030,
    //     position: 49,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_3_8656d32e-3a42-4463-ae1d-8f2258406f54.png?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42717458890950,
    //   title: 'Beige+Black / S / Double',
    //   option1: 'Beige+Black',
    //   option2: 'S',
    //   option3: 'Double',
    //   sku: 'MCMYN41-MUSMAC-SJ',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 35609033146566,
    //     product_id: 7195498184902,
    //     position: 50,
    //     created_at: '2023-06-15T02:25:37-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_1_9d140918-ff64-4315-a722-caf80adc4eaa.png?v=1722498320',
    //     variant_ids: [42717458890950, 42717458956486, 42717459022022, 42717459087558, 42717459153094, 42717459218630]
    //   },
    //   available: false,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Beige+Black / S / Double',
    //   public_title: 'Beige+Black / S / Double',
    //   options: ['Beige+Black', 'S', 'Double'],
    //   price: 5599,
    //   weight: 150,
    //   compare_at_price: 5998,
    //   inventory_management: 'shopify',
    //   barcode: '25114198847',
    //   featured_media: {
    //     alt: null,
    //     id: 28252292219078,
    //     position: 50,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_1_9d140918-ff64-4315-a722-caf80adc4eaa.png?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42717458956486,
    //   title: 'Beige+Black / M / Double',
    //   option1: 'Beige+Black',
    //   option2: 'M',
    //   option3: 'Double',
    //   sku: 'MCMYN41-MUMEDC-SJ',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 35609033146566,
    //     product_id: 7195498184902,
    //     position: 50,
    //     created_at: '2023-06-15T02:25:37-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_1_9d140918-ff64-4315-a722-caf80adc4eaa.png?v=1722498320',
    //     variant_ids: [42717458890950, 42717458956486, 42717459022022, 42717459087558, 42717459153094, 42717459218630]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Beige+Black / M / Double',
    //   public_title: 'Beige+Black / M / Double',
    //   options: ['Beige+Black', 'M', 'Double'],
    //   price: 5599,
    //   weight: 150,
    //   compare_at_price: 5998,
    //   inventory_management: null,
    //   barcode: '25114198840',
    //   featured_media: {
    //     alt: null,
    //     id: 28252292219078,
    //     position: 50,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_1_9d140918-ff64-4315-a722-caf80adc4eaa.png?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42717459022022,
    //   title: 'Beige+Black / L / Double',
    //   option1: 'Beige+Black',
    //   option2: 'L',
    //   option3: 'Double',
    //   sku: 'MCMYN41-MULARC-SJ',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 35609033146566,
    //     product_id: 7195498184902,
    //     position: 50,
    //     created_at: '2023-06-15T02:25:37-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_1_9d140918-ff64-4315-a722-caf80adc4eaa.png?v=1722498320',
    //     variant_ids: [42717458890950, 42717458956486, 42717459022022, 42717459087558, 42717459153094, 42717459218630]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Beige+Black / L / Double',
    //   public_title: 'Beige+Black / L / Double',
    //   options: ['Beige+Black', 'L', 'Double'],
    //   price: 5599,
    //   weight: 150,
    //   compare_at_price: 5998,
    //   inventory_management: null,
    //   barcode: '25114198833',
    //   featured_media: {
    //     alt: null,
    //     id: 28252292219078,
    //     position: 50,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_1_9d140918-ff64-4315-a722-caf80adc4eaa.png?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42717459087558,
    //   title: 'Beige+Black / XL / Double',
    //   option1: 'Beige+Black',
    //   option2: 'XL',
    //   option3: 'Double',
    //   sku: 'MCMYN41-MU1XLC-SJ',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 35609033146566,
    //     product_id: 7195498184902,
    //     position: 50,
    //     created_at: '2023-06-15T02:25:37-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_1_9d140918-ff64-4315-a722-caf80adc4eaa.png?v=1722498320',
    //     variant_ids: [42717458890950, 42717458956486, 42717459022022, 42717459087558, 42717459153094, 42717459218630]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Beige+Black / XL / Double',
    //   public_title: 'Beige+Black / XL / Double',
    //   options: ['Beige+Black', 'XL', 'Double'],
    //   price: 5599,
    //   weight: 150,
    //   compare_at_price: 5998,
    //   inventory_management: null,
    //   barcode: '35595210630',
    //   featured_media: {
    //     alt: null,
    //     id: 28252292219078,
    //     position: 50,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_1_9d140918-ff64-4315-a722-caf80adc4eaa.png?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    // {
    //   id: 42717459153094,
    //   title: 'Beige+Black / 2XL / Double',
    //   option1: 'Beige+Black',
    //   option2: '2XL',
    //   option3: 'Double',
    //   sku: 'MCMYN41-MU2XLC-SJ',
    //   requires_shipping: true,
    //   taxable: true,
    //   featured_image: {
    //     id: 35609033146566,
    //     product_id: 7195498184902,
    //     position: 50,
    //     created_at: '2023-06-15T02:25:37-04:00',
    //     updated_at: '2024-08-01T03:45:20-04:00',
    //     alt: null,
    //     width: 992,
    //     height: 1238,
    //     src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_1_9d140918-ff64-4315-a722-caf80adc4eaa.png?v=1722498320',
    //     variant_ids: [42717458890950, 42717458956486, 42717459022022, 42717459087558, 42717459153094, 42717459218630]
    //   },
    //   available: true,
    //   name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Beige+Black / 2XL / Double',
    //   public_title: 'Beige+Black / 2XL / Double',
    //   options: ['Beige+Black', '2XL', 'Double'],
    //   price: 5599,
    //   weight: 150,
    //   compare_at_price: 5998,
    //   inventory_management: null,
    //   barcode: '35595210623',
    //   featured_media: {
    //     alt: null,
    //     id: 28252292219078,
    //     position: 50,
    //     preview_image: {
    //       aspect_ratio: 0.801,
    //       height: 1238,
    //       width: 992,
    //       src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_1_9d140918-ff64-4315-a722-caf80adc4eaa.png?v=1722498320'
    //     }
    //   },
    //   quantity_rule: {
    //     min: 1,
    //     max: null,
    //     increment: 1
    //   },
    //   quantity_price_breaks: [],
    //   requires_selling_plan: false,
    //   selling_plan_allocations: []
    // },
    {
      id: 42717459218630,
      title: 'Beige+Black / 3XL / Double',
      option1: 'Beige+Black',
      option2: '3XL',
      option3: 'Double',
      sku: 'MCMYN41-MU3XLC-SJ',
      requires_shipping: true,
      taxable: true,
      featured_image: {
        id: 35609033146566,
        product_id: 7195498184902,
        position: 50,
        created_at: '2023-06-15T02:25:37-04:00',
        updated_at: '2024-08-01T03:45:20-04:00',
        alt: null,
        width: 992,
        height: 1238,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_1_9d140918-ff64-4315-a722-caf80adc4eaa.png?v=1722498320',
        variant_ids: [42717458890950, 42717458956486, 42717459022022, 42717459087558, 42717459153094, 42717459218630]
      },
      available: true,
      name: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra-YN21 - Beige+Black / 3XL / Double',
      public_title: 'Beige+Black / 3XL / Double',
      options: ['Beige+Black', '3XL', 'Double'],
      price: 5599,
      weight: 150,
      compare_at_price: 5998,
      inventory_management: null,
      barcode: '35595210616',
      featured_media: {
        alt: null,
        id: 28252292219078,
        position: 50,
        preview_image: {
          aspect_ratio: 0.801,
          height: 1238,
          width: 992,
          src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_1_9d140918-ff64-4315-a722-caf80adc4eaa.png?v=1722498320'
        }
      },
      quantity_rule: {
        min: 1,
        max: null,
        increment: 1
      },
      quantity_price_breaks: [],
      requires_selling_plan: false,
      selling_plan_allocations: []
    }
  ],
  images: [
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_ae9a5331-7afc-4dde-abc1-5136e356bcbe.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/2_b2bb5218-f90d-4ccb-b742-f4b7475bf149.jpg?v=1727172132',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/1_b9b405f6-cf5d-413a-9df9-ac7f0a55bea5.jpg?v=1727172100',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/3_da62fa38-fc7c-4078-a6e2-018480e11dfc.jpg?v=1727172141',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/4_297a6caf-9551-42c4-8bb4-d2d27e2af454.jpg?v=1727172201',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/5_3978a53c-3782-4682-b99c-7cd382333ed2.jpg?v=1727172205',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/d4719cd55b5e2a2676cfebe92033ddf7_b4501b5c-2715-40c6-a900-f76c08de31eb.jpg?v=1727172367',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/products/SupportNursingBras.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/products/SeamlessBreastfeedingBras.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_b6475688-aada-4566-afb9-0940cd9da26b.png?v=1720172299',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/Beige-02.jpg?v=1722498304',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/2_1_6d6252d2-9831-4592-aaab-4d274ddf483b.jpg?v=1718849049',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/4_1.jpg?v=1718849208',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/3_1.jpg?v=1718849157',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/6_1.jpg?v=1718849235',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/products/ComfortWirelessBra.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/products/SeamlessBreastfeedingBras_773a20ac-7519-4af2-81c0-ecc7848c80dd.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/products/SoftNursingBras.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/products/MomcozySeamlessNusingBras.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/products/SeamlessNursingBras_8cdf7116-ffe8-4624-96f1-1b17ad5b561e.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/products/PregnancySleepingBralette.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/products/ComfortMaternityBras.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_1.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_2_4cfa1116-2467-46cb-93a1-c865e6cc697b.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_3_e6002485-f4ab-4eb7-9ceb-59c978ece64c.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_4_9b7c0335-3548-487d-932c-abe6fced2ae7.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_5.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_6.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_7.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/1_5ebca54b-3cfc-4445-8830-da38f93d3ddd.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/ShallowBrown-02.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/ShallowBrown-01.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/ShallowBrown-03.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/ShallowBrown-04.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/ShallowBrown-05_1.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/1_1825383e-3852-4d82-8ba7-52cefe41612e.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/LightGrey-05.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/LightGrey-02.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/LightGrey-01.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/LightGrey-03.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/LightGrey-04.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/LightGrey-07.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/products/ComfortMaternityBras_53416939-bedf-4f31-976a-5f3673f90541.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/products/WirefreeNursingBras_6e846705-78bd-45e6-b057-de8e8c284fa7.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/products/InvisiblesNursingBras_5860ba05-d1f8-4a5d-8925-9a35584da224.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/products/SeamlessBreastfeedingBras_3fe6d481-da46-4c48-a8ae-ec3fef690d11.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/YN21_YN21_9d21daf9-d861-40b3-85e1-e840bc62dfd0.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/YN21_YN21_644fde83-80fa-4d25-b8a6-96bf8ad86724.jpg?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_3_8656d32e-3a42-4463-ae1d-8f2258406f54.png?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_1_9d140918-ff64-4315-a722-caf80adc4eaa.png?v=1722498320',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/IMG_202408057027_992x1238_8a9eff32-c493-49f1-a505-1e28ba1d4152.jpg?v=1722828735',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/1_b9cf8cf9-5981-4c18-a4ff-2a2554404fa2.jpg?v=1722828278',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/2_1fdb0fab-3658-4897-ba9a-b64b268dcd0b.jpg?v=1722828282',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/7_c2402a75-c27d-4d6a-986d-5637f918096a.jpg?v=1722828195',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/3_89694ed6-25a0-4074-b380-cccb1b56bf79.jpg?v=1722828287',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/4_17154daf-3394-497f-a4fc-08569312cf08.jpg?v=1722828290',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/5_0de76053-d161-4597-9b41-63ae6027e65a.jpg?v=1722828292',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/9_16aa45a0-6beb-40b2-a6e2-3ff1c955f246.jpg?v=1722828197',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/1_5569da7d-35ca-4f21-8a5e-9ef68a763a2d.jpg?v=1728899347',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/2_57e54797-c976-48cd-b56d-8d84f12377c5.jpg?v=1728899348',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/3_c7d67cd6-6814-4332-aa8f-e75ce2f53604.jpg?v=1728899351',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/4_ec833a88-f0f7-418f-a245-ab4cef6204bf.jpg?v=1728899354',
    '//cdn.shopify.com/s/files/1/0559/2321/2486/files/5_5029a463-0c13-440f-af72-ebd4fa8babf3.jpg?v=1728899357'
  ],
  featured_image: '//cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_ae9a5331-7afc-4dde-abc1-5136e356bcbe.jpg?v=1722498320',
  url: '/products/breastfeeding-seamless-wirefree-nursing-bras',
  media: [
    {
      alt: null,
      id: 29870494482630,
      position: 1,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_ae9a5331-7afc-4dde-abc1-5136e356bcbe.jpg?v=1722498320'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_ae9a5331-7afc-4dde-abc1-5136e356bcbe.jpg?v=1722498320',
      width: 992
    },
    {
      alt: null,
      id: 30566073172166,
      position: 2,
      preview_image: {
        aspect_ratio: 0.771,
        height: 1660,
        width: 1280,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/2_b2bb5218-f90d-4ccb-b742-f4b7475bf149.jpg?v=1727172132'
      },
      aspect_ratio: 0.771,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/2_b2bb5218-f90d-4ccb-b742-f4b7475bf149.jpg?v=1727172132',
      width: 1280
    },
    {
      alt: null,
      id: 30566069698758,
      position: 3,
      preview_image: {
        aspect_ratio: 0.771,
        height: 1660,
        width: 1280,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_b9b405f6-cf5d-413a-9df9-ac7f0a55bea5.jpg?v=1727172100'
      },
      aspect_ratio: 0.771,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_b9b405f6-cf5d-413a-9df9-ac7f0a55bea5.jpg?v=1727172100',
      width: 1280
    },
    {
      alt: null,
      id: 30566074515654,
      position: 4,
      preview_image: {
        aspect_ratio: 0.771,
        height: 1660,
        width: 1280,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/3_da62fa38-fc7c-4078-a6e2-018480e11dfc.jpg?v=1727172141'
      },
      aspect_ratio: 0.771,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/3_da62fa38-fc7c-4078-a6e2-018480e11dfc.jpg?v=1727172141',
      width: 1280
    },
    {
      alt: null,
      id: 30566077956294,
      position: 5,
      preview_image: {
        aspect_ratio: 0.771,
        height: 1660,
        width: 1280,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/4_297a6caf-9551-42c4-8bb4-d2d27e2af454.jpg?v=1727172201'
      },
      aspect_ratio: 0.771,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/4_297a6caf-9551-42c4-8bb4-d2d27e2af454.jpg?v=1727172201',
      width: 1280
    },
    {
      alt: null,
      id: 30566078152902,
      position: 6,
      preview_image: {
        aspect_ratio: 0.771,
        height: 1660,
        width: 1280,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/5_3978a53c-3782-4682-b99c-7cd382333ed2.jpg?v=1727172205'
      },
      aspect_ratio: 0.771,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/5_3978a53c-3782-4682-b99c-7cd382333ed2.jpg?v=1727172205',
      width: 1280
    },
    {
      alt: null,
      id: 30566092472518,
      position: 7,
      preview_image: {
        aspect_ratio: 0.8,
        height: 2000,
        width: 1600,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/d4719cd55b5e2a2676cfebe92033ddf7_b4501b5c-2715-40c6-a900-f76c08de31eb.jpg?v=1727172367'
      },
      aspect_ratio: 0.8,
      height: 2000,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/d4719cd55b5e2a2676cfebe92033ddf7_b4501b5c-2715-40c6-a900-f76c08de31eb.jpg?v=1727172367',
      width: 1600
    },
    {
      alt: 'Support Nursing Bras',
      id: 25707896864966,
      position: 8,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/SupportNursingBras.jpg?v=1722498320'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/SupportNursingBras.jpg?v=1722498320',
      width: 992
    },
    {
      alt: 'SMOOTH - Ultra Soft & Omni Maternity Nursing Bra with One-Hand Clips',
      id: 25707896766662,
      position: 9,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/SeamlessBreastfeedingBras.jpg?v=1722498320'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/SeamlessBreastfeedingBras.jpg?v=1722498320',
      width: 992
    },
    {
      alt: null,
      id: 30126020362438,
      position: 10,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_b6475688-aada-4566-afb9-0940cd9da26b.png?v=1720172299'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/yn21_b6475688-aada-4566-afb9-0940cd9da26b.png?v=1720172299',
      width: 992
    },
    {
      alt: null,
      id: 30288037806278,
      position: 11,
      preview_image: {
        aspect_ratio: 0.771,
        height: 1660,
        width: 1280,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/Beige-02.jpg?v=1722498304'
      },
      aspect_ratio: 0.771,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/Beige-02.jpg?v=1722498304',
      width: 1280
    },
    {
      alt: null,
      id: 30003407847622,
      position: 12,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/2_1_6d6252d2-9831-4592-aaab-4d274ddf483b.jpg?v=1718849049'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/2_1_6d6252d2-9831-4592-aaab-4d274ddf483b.jpg?v=1718849049',
      width: 992
    },
    {
      alt: null,
      id: 30003423740102,
      position: 13,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/4_1.jpg?v=1718849208'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/4_1.jpg?v=1718849208',
      width: 992
    },
    {
      alt: null,
      id: 30003418300614,
      position: 14,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/3_1.jpg?v=1718849157'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/3_1.jpg?v=1718849157',
      width: 992
    },
    {
      alt: null,
      id: 30003427049670,
      position: 15,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/6_1.jpg?v=1718849235'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/6_1.jpg?v=1718849235',
      width: 992
    },
    {
      alt: 'Comfort Wireless Bra',
      id: 25707902042310,
      position: 16,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/ComfortWirelessBra.jpg?v=1722498320'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/ComfortWirelessBra.jpg?v=1722498320',
      width: 992
    },
    {
      alt: 'Seamless Breastfeeding Bras',
      id: 25707902140614,
      position: 17,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/SeamlessBreastfeedingBras_773a20ac-7519-4af2-81c0-ecc7848c80dd.jpg?v=1722498320'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/SeamlessBreastfeedingBras_773a20ac-7519-4af2-81c0-ecc7848c80dd.jpg?v=1722498320',
      width: 992
    },
    {
      alt: 'Soft Nursing Bras',
      id: 25707902206150,
      position: 18,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/SoftNursingBras.jpg?v=1722498320'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/SoftNursingBras.jpg?v=1722498320',
      width: 992
    },
    {
      alt: null,
      id: 26820767154374,
      position: 19,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/MomcozySeamlessNusingBras.jpg?v=1722498320'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/MomcozySeamlessNusingBras.jpg?v=1722498320',
      width: 992
    },
    {
      alt: 'Seamless Nursing Bras',
      id: 25707902173382,
      position: 20,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/SeamlessNursingBras_8cdf7116-ffe8-4624-96f1-1b17ad5b561e.jpg?v=1722498320'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/SeamlessNursingBras_8cdf7116-ffe8-4624-96f1-1b17ad5b561e.jpg?v=1722498320',
      width: 992
    },
    {
      alt: null,
      id: 26820767187142,
      position: 21,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/PregnancySleepingBralette.jpg?v=1722498320'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/PregnancySleepingBralette.jpg?v=1722498320',
      width: 992
    },
    {
      alt: 'Comfort Maternity Bras',
      id: 25707902009542,
      position: 22,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/ComfortMaternityBras.jpg?v=1722498320'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/ComfortMaternityBras.jpg?v=1722498320',
      width: 992
    },
    {
      alt: null,
      id: 26332494037190,
      position: 23,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_1.jpg?v=1722498320'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_1.jpg?v=1722498320',
      width: 992
    },
    {
      alt: null,
      id: 26332494069958,
      position: 24,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_2_4cfa1116-2467-46cb-93a1-c865e6cc697b.jpg?v=1722498320'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_2_4cfa1116-2467-46cb-93a1-c865e6cc697b.jpg?v=1722498320',
      width: 992
    },
    {
      alt: null,
      id: 26332494102726,
      position: 25,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_3_e6002485-f4ab-4eb7-9ceb-59c978ece64c.jpg?v=1722498320'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_3_e6002485-f4ab-4eb7-9ceb-59c978ece64c.jpg?v=1722498320',
      width: 992
    },
    {
      alt: null,
      id: 26332494135494,
      position: 26,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_4_9b7c0335-3548-487d-932c-abe6fced2ae7.jpg?v=1722498320'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_4_9b7c0335-3548-487d-932c-abe6fced2ae7.jpg?v=1722498320',
      width: 992
    },
    {
      alt: null,
      id: 26332494201030,
      position: 27,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_5.jpg?v=1722498320'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_5.jpg?v=1722498320',
      width: 992
    },
    {
      alt: null,
      id: 26332494233798,
      position: 28,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_6.jpg?v=1722498320'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_6.jpg?v=1722498320',
      width: 992
    },
    {
      alt: null,
      id: 26332494266566,
      position: 29,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_7.jpg?v=1722498320'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/BreastfeedingSeamlessWirelessNursingBras_7.jpg?v=1722498320',
      width: 992
    },
    {
      alt: null,
      id: 28752281403590,
      position: 30,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_5ebca54b-3cfc-4445-8830-da38f93d3ddd.jpg?v=1722498320'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_5ebca54b-3cfc-4445-8830-da38f93d3ddd.jpg?v=1722498320',
      width: 992
    },
    {
      alt: null,
      id: 28725740044486,
      position: 31,
      preview_image: {
        aspect_ratio: 1,
        height: 1660,
        width: 1660,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/ShallowBrown-02.jpg?v=1722498320'
      },
      aspect_ratio: 1,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/ShallowBrown-02.jpg?v=1722498320',
      width: 1660
    },
    {
      alt: null,
      id: 28725740175558,
      position: 32,
      preview_image: {
        aspect_ratio: 1,
        height: 1660,
        width: 1660,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/ShallowBrown-01.jpg?v=1722498320'
      },
      aspect_ratio: 1,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/ShallowBrown-01.jpg?v=1722498320',
      width: 1660
    },
    {
      alt: null,
      id: 28725740208326,
      position: 33,
      preview_image: {
        aspect_ratio: 1,
        height: 1660,
        width: 1660,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/ShallowBrown-03.jpg?v=1722498320'
      },
      aspect_ratio: 1,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/ShallowBrown-03.jpg?v=1722498320',
      width: 1660
    },
    {
      alt: null,
      id: 28725740241094,
      position: 34,
      preview_image: {
        aspect_ratio: 1,
        height: 1660,
        width: 1660,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/ShallowBrown-04.jpg?v=1722498320'
      },
      aspect_ratio: 1,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/ShallowBrown-04.jpg?v=1722498320',
      width: 1660
    },
    {
      alt: null,
      id: 28733448814790,
      position: 35,
      preview_image: {
        aspect_ratio: 1,
        height: 1660,
        width: 1660,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/ShallowBrown-05_1.jpg?v=1722498320'
      },
      aspect_ratio: 1,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/ShallowBrown-05_1.jpg?v=1722498320',
      width: 1660
    },
    {
      alt: null,
      id: 28752283107526,
      position: 36,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_1825383e-3852-4d82-8ba7-52cefe41612e.jpg?v=1722498320'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_1825383e-3852-4d82-8ba7-52cefe41612e.jpg?v=1722498320',
      width: 992
    },
    {
      alt: null,
      id: 28725739913414,
      position: 37,
      preview_image: {
        aspect_ratio: 1,
        height: 1660,
        width: 1660,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/LightGrey-05.jpg?v=1722498320'
      },
      aspect_ratio: 1,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/LightGrey-05.jpg?v=1722498320',
      width: 1660
    },
    {
      alt: null,
      id: 28725738995910,
      position: 38,
      preview_image: {
        aspect_ratio: 1,
        height: 1660,
        width: 1660,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/LightGrey-02.jpg?v=1722498320'
      },
      aspect_ratio: 1,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/LightGrey-02.jpg?v=1722498320',
      width: 1660
    },
    {
      alt: null,
      id: 28725739585734,
      position: 39,
      preview_image: {
        aspect_ratio: 1,
        height: 1660,
        width: 1660,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/LightGrey-01.jpg?v=1722498320'
      },
      aspect_ratio: 1,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/LightGrey-01.jpg?v=1722498320',
      width: 1660
    },
    {
      alt: null,
      id: 28725739782342,
      position: 40,
      preview_image: {
        aspect_ratio: 1,
        height: 1660,
        width: 1660,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/LightGrey-03.jpg?v=1722498320'
      },
      aspect_ratio: 1,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/LightGrey-03.jpg?v=1722498320',
      width: 1660
    },
    {
      alt: null,
      id: 28725739847878,
      position: 41,
      preview_image: {
        aspect_ratio: 1,
        height: 1660,
        width: 1660,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/LightGrey-04.jpg?v=1722498320'
      },
      aspect_ratio: 1,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/LightGrey-04.jpg?v=1722498320',
      width: 1660
    },
    {
      alt: null,
      id: 28725739946182,
      position: 42,
      preview_image: {
        aspect_ratio: 1,
        height: 1660,
        width: 1660,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/LightGrey-07.jpg?v=1722498320'
      },
      aspect_ratio: 1,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/LightGrey-07.jpg?v=1722498320',
      width: 1660
    },
    {
      alt: 'Comfort Maternity Bras',
      id: 25707906662598,
      position: 43,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/ComfortMaternityBras_53416939-bedf-4f31-976a-5f3673f90541.jpg?v=1722498320'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/ComfortMaternityBras_53416939-bedf-4f31-976a-5f3673f90541.jpg?v=1722498320',
      width: 992
    },
    {
      alt: 'Wirefree Nursing Bras',
      id: 25707906859206,
      position: 44,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/WirefreeNursingBras_6e846705-78bd-45e6-b057-de8e8c284fa7.jpg?v=1722498320'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/WirefreeNursingBras_6e846705-78bd-45e6-b057-de8e8c284fa7.jpg?v=1722498320',
      width: 992
    },
    {
      alt: 'Invisibles Nursing Bras',
      id: 25707906728134,
      position: 45,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/InvisiblesNursingBras_5860ba05-d1f8-4a5d-8925-9a35584da224.jpg?v=1722498320'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/InvisiblesNursingBras_5860ba05-d1f8-4a5d-8925-9a35584da224.jpg?v=1722498320',
      width: 992
    },
    {
      alt: 'Seamless Breastfeeding Bras',
      id: 25707906760902,
      position: 46,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/SeamlessBreastfeedingBras_3fe6d481-da46-4c48-a8ae-ec3fef690d11.jpg?v=1722498320'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/products/SeamlessBreastfeedingBras_3fe6d481-da46-4c48-a8ae-ec3fef690d11.jpg?v=1722498320',
      width: 992
    },
    {
      alt: null,
      id: 28252290580678,
      position: 47,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/YN21_YN21_9d21daf9-d861-40b3-85e1-e840bc62dfd0.jpg?v=1722498320'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/YN21_YN21_9d21daf9-d861-40b3-85e1-e840bc62dfd0.jpg?v=1722498320',
      width: 992
    },
    {
      alt: null,
      id: 28252289073350,
      position: 48,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/YN21_YN21_644fde83-80fa-4d25-b8a6-96bf8ad86724.jpg?v=1722498320'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/YN21_YN21_644fde83-80fa-4d25-b8a6-96bf8ad86724.jpg?v=1722498320',
      width: 992
    },
    {
      alt: null,
      id: 28252293497030,
      position: 49,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_3_8656d32e-3a42-4463-ae1d-8f2258406f54.png?v=1722498320'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_3_8656d32e-3a42-4463-ae1d-8f2258406f54.png?v=1722498320',
      width: 992
    },
    {
      alt: null,
      id: 28252292219078,
      position: 50,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_1_9d140918-ff64-4315-a722-caf80adc4eaa.png?v=1722498320'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/BreastfeedingSeamlessWirelessNursingBras2Pack_1_9d140918-ff64-4315-a722-caf80adc4eaa.png?v=1722498320',
      width: 992
    },
    {
      alt: null,
      id: 30299886682310,
      position: 51,
      preview_image: {
        aspect_ratio: 0.801,
        height: 1238,
        width: 992,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/IMG_202408057027_992x1238_8a9eff32-c493-49f1-a505-1e28ba1d4152.jpg?v=1722828735'
      },
      aspect_ratio: 0.801,
      height: 1238,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/IMG_202408057027_992x1238_8a9eff32-c493-49f1-a505-1e28ba1d4152.jpg?v=1722828735',
      width: 992
    },
    {
      alt: null,
      id: 30299879342278,
      position: 52,
      preview_image: {
        aspect_ratio: 0.771,
        height: 1660,
        width: 1280,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_b9cf8cf9-5981-4c18-a4ff-2a2554404fa2.jpg?v=1722828278'
      },
      aspect_ratio: 0.771,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_b9cf8cf9-5981-4c18-a4ff-2a2554404fa2.jpg?v=1722828278',
      width: 1280
    },
    {
      alt: null,
      id: 30299879407814,
      position: 53,
      preview_image: {
        aspect_ratio: 0.771,
        height: 1660,
        width: 1280,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/2_1fdb0fab-3658-4897-ba9a-b64b268dcd0b.jpg?v=1722828282'
      },
      aspect_ratio: 0.771,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/2_1fdb0fab-3658-4897-ba9a-b64b268dcd0b.jpg?v=1722828282',
      width: 1280
    },
    {
      alt: null,
      id: 30299877736646,
      position: 54,
      preview_image: {
        aspect_ratio: 1,
        height: 1660,
        width: 1660,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/7_c2402a75-c27d-4d6a-986d-5637f918096a.jpg?v=1722828195'
      },
      aspect_ratio: 1,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/7_c2402a75-c27d-4d6a-986d-5637f918096a.jpg?v=1722828195',
      width: 1660
    },
    {
      alt: null,
      id: 30299879604422,
      position: 55,
      preview_image: {
        aspect_ratio: 0.771,
        height: 1660,
        width: 1280,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/3_89694ed6-25a0-4074-b380-cccb1b56bf79.jpg?v=1722828287'
      },
      aspect_ratio: 0.771,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/3_89694ed6-25a0-4074-b380-cccb1b56bf79.jpg?v=1722828287',
      width: 1280
    },
    {
      alt: null,
      id: 30299879637190,
      position: 56,
      preview_image: {
        aspect_ratio: 0.771,
        height: 1660,
        width: 1280,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/4_17154daf-3394-497f-a4fc-08569312cf08.jpg?v=1722828290'
      },
      aspect_ratio: 0.771,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/4_17154daf-3394-497f-a4fc-08569312cf08.jpg?v=1722828290',
      width: 1280
    },
    {
      alt: null,
      id: 30299879669958,
      position: 57,
      preview_image: {
        aspect_ratio: 0.771,
        height: 1660,
        width: 1280,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/5_0de76053-d161-4597-9b41-63ae6027e65a.jpg?v=1722828292'
      },
      aspect_ratio: 0.771,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/5_0de76053-d161-4597-9b41-63ae6027e65a.jpg?v=1722828292',
      width: 1280
    },
    {
      alt: null,
      id: 30299877769414,
      position: 58,
      preview_image: {
        aspect_ratio: 1,
        height: 1660,
        width: 1660,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/9_16aa45a0-6beb-40b2-a6e2-3ff1c955f246.jpg?v=1722828197'
      },
      aspect_ratio: 1,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/9_16aa45a0-6beb-40b2-a6e2-3ff1c955f246.jpg?v=1722828197',
      width: 1660
    },
    {
      alt: null,
      id: 30695524270278,
      position: 59,
      preview_image: {
        aspect_ratio: 0.771,
        height: 1660,
        width: 1280,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_5569da7d-35ca-4f21-8a5e-9ef68a763a2d.jpg?v=1728899347'
      },
      aspect_ratio: 0.771,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/1_5569da7d-35ca-4f21-8a5e-9ef68a763a2d.jpg?v=1728899347',
      width: 1280
    },
    {
      alt: null,
      id: 30695524565190,
      position: 60,
      preview_image: {
        aspect_ratio: 0.771,
        height: 1660,
        width: 1280,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/2_57e54797-c976-48cd-b56d-8d84f12377c5.jpg?v=1728899348'
      },
      aspect_ratio: 0.771,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/2_57e54797-c976-48cd-b56d-8d84f12377c5.jpg?v=1728899348',
      width: 1280
    },
    {
      alt: null,
      id: 30695524696262,
      position: 61,
      preview_image: {
        aspect_ratio: 0.771,
        height: 1660,
        width: 1280,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/3_c7d67cd6-6814-4332-aa8f-e75ce2f53604.jpg?v=1728899351'
      },
      aspect_ratio: 0.771,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/3_c7d67cd6-6814-4332-aa8f-e75ce2f53604.jpg?v=1728899351',
      width: 1280
    },
    {
      alt: null,
      id: 30695524794566,
      position: 62,
      preview_image: {
        aspect_ratio: 0.771,
        height: 1660,
        width: 1280,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/4_ec833a88-f0f7-418f-a245-ab4cef6204bf.jpg?v=1728899354'
      },
      aspect_ratio: 0.771,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/4_ec833a88-f0f7-418f-a245-ab4cef6204bf.jpg?v=1728899354',
      width: 1280
    },
    {
      alt: null,
      id: 30695525253318,
      position: 63,
      preview_image: {
        aspect_ratio: 0.771,
        height: 1660,
        width: 1280,
        src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/5_5029a463-0c13-440f-af72-ebd4fa8babf3.jpg?v=1728899357'
      },
      aspect_ratio: 0.771,
      height: 1660,
      media_type: 'image',
      src: 'https://cdn.shopify.com/s/files/1/0559/2321/2486/files/5_5029a463-0c13-440f-af72-ebd4fa8babf3.jpg?v=1728899357',
      width: 1280
    }
  ],
  requires_selling_plan: false,
  selling_plan_groups: []
})

const currenSelected = computed(() => {
  return skuSpec.value.map(item => item.value)
})
const currenVariant = computed(() => {
  const result = data.value.variants.find(item => {
    // console.log([item.option1, item.option2, item.option3].join('-') === currenSelected.value.join('-'))
    return [item.option1, item.option2, item.option3].join('-') === currenSelected.value.join('-')
  })

  return result
})
const skuSpec = ref([
  {
    name: 'Color',
    position: 1,
    values: ['Brown', 'Brown+Brown', 'Beige', 'Black', 'Shallow Brown', 'Light Grey', 'Cream', 'Maple Sugar', 'Brown+Black', 'Beige+Black'].map(item => ({
      name: item,
      disabled: false
    })),
    value: data.value.variants.filter(item => item.available)[0].option1
  },
  {
    name: 'Size',
    position: 2,
    values: ['S', 'M', 'L', 'XL', '2XL', '3XL'].map(item => ({
      name: item,
      disabled: false
    })),
    value: data.value.variants.filter(item => item.available)[0].option2
  },
  {
    name: 'Quantity',
    position: 3,
    values: ['Single', 'Double'].map(item => ({
      name: item,
      disabled: false
    })),
    value: data.value.variants.filter(item => item.available)[0].option3
  }
])
const currenSpec = ref([])
const changeSelectedStatus = (option, val) => {
  if (val.disabled) return
  if (option.value === val.name) {
    option.value = ''
  } else {
    option.value = val.name
  }
  updateDisabledStatus(skuSpec.value, pathMapData)
}
/*  
生成有效路径字段对象
核心原理：当前的规格Sku，或者组合起来的规则Sku，在skus数组中对应项的库存为零时，当前规格会被禁用，生成的字典路径是为了协助和简化这个匹配过程 
1、初始化的时候判断规格是否可以点击
2、选择规格后判断规则是否可点
如：
颜色：蓝色 红色
产品：中国 美国
=》可能的Sku组合
蓝色 - 美国 库存 10
蓝色 - 中国 库存 0
红色 - 美国 库存 10
红色 - 中国 库存 0
=》有效Sku组合
蓝色 - 美国 库存 10 skuid 1001
红色 - 美国 库存 10 skuid 1002
=》得到所有有效sku结合的子集（算法）
[蓝色],[美国],[蓝色,美国]
[红色],[美国],[红色,美国]
=>生成路径集合（对象，方便查找）
{
  '蓝色':[1001],
  '美国':[1001,1002]
  '蓝色-美国': [1001],
  '红色': [1002],
  '红色-美国': [1002],}
*/

const getPathMap = goods => {
  const pathMap = {}
  // 1. 根据skus字段生成有效sku数组（有库存的）
  const effectiveSkus = goods.filter(item => item.available)
  // 2. 根据有效SKU使用算法（子集算法） [1,2] => [[1], [2], [1,2]]
  effectiveSkus.forEach(sku => {
    //2.1 获取匹配的option(valueName)组成的数组
    const selectedOptionArr = [sku.option1, sku.option2, sku.option3]
    // 2.2 获取子集
    const valueArrPowerSet = bwPowerSet(selectedOptionArr)
    console.log(valueArrPowerSet)
    // 3. 把得到的子集填充到路径字典中
    valueArrPowerSet.forEach(item => {
      // 初始化key
      const key = item.join('-')
      if (pathMap[key]) {
        pathMap[key].push(sku.id)
      } else {
        pathMap[key] = [sku.id]
      }
    })
  })
  return pathMap
}
const bwPowerSet = originalSet => {
  const subSets = []

  // We will have 2^n possible combinations (where n is a length of original set).
  // It is because for every element of original set we will decide whether to include
  // it or not (2 options for each set element).
  const numberOfCombinations = 2 ** originalSet.length

  // Each number in binary representation in a range from 0 to 2^n does exactly what we need:
  // it shows by its bits (0 or 1) whether to include related element from the set or not.
  // For example, for the set {1, 2, 3} the binary number of 0b010 would mean that we need to
  // include only "2" to the current set.
  for (let combinationIndex = 0; combinationIndex < numberOfCombinations; combinationIndex += 1) {
    const subSet = []

    for (let setElementIndex = 0; setElementIndex < originalSet.length; setElementIndex += 1) {
      // Decide whether we need to include current element into the subset or not.
      if (combinationIndex & (1 << setElementIndex)) {
        subSet.push(originalSet[setElementIndex])
      }
    }

    // Add current subset to the list of all subsets.
    subSets.push(subSet)
  }

  return subSets
}
const pathMapData = getPathMap(data.value.variants)
/* 
 思路（初始化禁用状态）
 1、遍历每一个规格对象，使用name字段作为key去路径字典pathMap中做匹配，匹配不上则禁用
 2、若初始就有选中sku，不用调用初始化，直接调用updateDisabledStatus更新禁用状态
  */
const initDisabledStatus = (specs, pathMap) => {
  specs.forEach(spec => {
    spec.values.forEach(val => {
      if (pathMap[val.name]) {
        val.disabled = false
      } else {
        val.disabled = true
      }
    })
  })
}
// initDisabledStatus(skuSpec.value, pathMapData)
/* 
  思路（点击时组合更新警用状态）
  1、按顺序得到规则选中项的数组[蓝色, 20cm, '']
  2、遍历每一个规格
    2.1 把name字段的值填充到1对应的位置
    2.2 过滤空项使join方法形成一个有效的key
    2.3 使用key区域pathMap中进行匹配，匹配不上则禁用当前项
*/
const updateDisabledStatus = (specs, pathMap) => {
  specs.forEach((spec, index) => {
    const selectedValues = [...currenSelected.value]
    console.log(selectedValues)
    spec.values.forEach(val => {
      selectedValues[index] = val.name
      const key = selectedValues.filter(item => item).join('-')
      if (pathMap[key]) {
        val.disabled = false
      } else {
        val.disabled = true
      }
    })
  })
}
updateDisabledStatus(skuSpec.value, pathMapData)
function getSubsets(arr) {
  const subsets = []

  function findSubsets(index, currentSubset) {
    if (index === arr.length) {
      subsets.push(currentSubset)
      return
    }

    findSubsets(index + 1, currentSubset.concat(arr[index]))
    findSubsets(index + 1, currentSubset)
  }

  findSubsets(0, [])
  return subsets
}
</script>
<style scoped lang="scss">
.spec-options {
  margin-bottom: 30px;
}
.spec-item {
  padding: 10px 16px;
  border: 1px solid #ccc;
  display: inline-block;
  margin-left: 12px;
  font-size: 14px;
  cursor: pointer;
  &.active {
    border-color: blue;
  }
  &.disabled {
    border-style: dashed;
    opacity: 0.7;
    cursor: not-allowed;
  }
}
</style>
