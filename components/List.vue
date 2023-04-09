<template>
     <div class="mt-8 flow-root">
      <div class="-mx-4 -my-2 overflow-x-auto sm:-mx-6 lg:-mx-8">
        <div class="inline-block min-w-full py-2 align-middle sm:px-6 lg:px-8">
  <table class="min-w-full divide-y divide-gray-50">
    <thead>
      <tr class="divide-x divide-gray-20">
        <th
          scope="col"
          class="py-3.5 pl-4 pr-4 text-center text-sm font-semibold text-gray-900 sm:pl-0"
        >
          Category
        </th>
        <th
          scope="col"
          class="px-4 py-3.5 text-center text-sm font-semibold text-gray-900"
        >
          Skill
        </th>
        <!-- <th
          scope="col"
          class="px-4 py-3.5 text-center text-sm font-semibold text-gray-900"
        >
          answer
        </th> -->
        <!-- <th
          scope="col"
          class="px-4 py-3.5 text-center text-sm font-semibold text-gray-900"
        >
          sub_skill
        </th> -->
        <!-- <th
          scope="col"
          class="py-3.5 pl-4 pr-4 text-center text-sm font-semibold text-gray-900 sm:pr-0"
        >
          question_url
        </th> -->
        <!-- <th
          scope="col"
          class="px-4 py-3.5 text-center text-sm font-semibold text-gray-900"
        >
          answer_hint
        </th> -->
        <th
          scope="col"
          class="py-3.5 pl-4 pr-4 text-center text-sm font-semibold text-gray-900 sm:pr-0"
        >
          explanation
        </th>
      </tr>
      <th
        scope="col"
        class="py-3.5 pl-4 pr-4 text-center text-sm font-semibold text-gray-900 sm:pr-0"
      >
        answer_type
      </th>
    </thead>
    <tbody class="divide-y divide-gray-200 bg-white">
      <tr
        v-for="template in templatedata"
        :key="template.category"
        class="divide-x divide-gray-200"
      >
        <td
          class="whitespace-nowrap py-4 text-center pl-4 pr-4 text-sm font-medium text-gray-900 sm:pl-0"
        >
          {{ template.category }}
        </td>
        <td
          class="whitespace-nowrap py-4 text-center pl-4 pr-4 text-sm font-medium text-gray-900 sm:pl-0"
        >
          {{ template.Skill }}
        </td>
        <td
          class="whitespace-nowrap py-4 text-center pl-4 pr-4 text-sm font-medium text-gray-900 sm:pl-0"
        >
          {{ template.answer }}
        </td>
        <td class="whitespace-nowrap text-center p-4 text-sm text-gray-500">
          {{ template.sub_skill }}
        </td>
        <td class="whitespace-nowrap p-4 text-center text-sm text-gray-500">
          {{ template.question_url }}
        </td>
        <td
          class="whitespace-nowrap py-4 pl-4 text-center pr-4 text-sm text-gray-500 sm:pr-0"
        >
          {{ template.answer_hint }}
        </td>
        <td
          class="whitespace-nowrap py-4 pl-4 text-center pr-4 text-sm text-gray-500 sm:pr-0"
        >
          {{ template.explanation }}
        </td>
        <td
          class="whitespace-nowrap py-4 pl-4 text-center pr-4 text-sm text-gray-500 sm:pr-0"
        >
          {{ template.answer_type }}
        </td>
      </tr>
    </tbody>
  </table>
  </div></div></div>
</template>
<script setup>
//define the props
const props = defineProps({
  templatedata: Array,
  default: () => [],
});
</script>
