<template>
<TransitionRoot as="template" :show="open">
    <Dialog as="div" class="relative z-10" @close="open = false">
      <TransitionChild as="template" enter="ease-out duration-300" enter-from="opacity-0" enter-to="opacity-100" leave="ease-in duration-200" leave-from="opacity-100" leave-to="opacity-0">
        <div class="fixed inset-0 bg-gray-500 bg-opacity-75 transition-opacity" />
      </TransitionChild>

      <div class="fixed inset-0 z-10 overflow-y-auto">
        <div class="flex min-h-full items-end justify-center p-4 text-center sm:items-center sm:p-0">
          <TransitionChild as="template" enter="ease-out duration-300" enter-from="opacity-0 translate-y-4 sm:translate-y-0 sm:scale-95" enter-to="opacity-100 translate-y-0 sm:scale-100" leave="ease-in duration-200" leave-from="opacity-100 translate-y-0 sm:scale-100" leave-to="opacity-0 translate-y-4 sm:translate-y-0 sm:scale-95">
            <DialogPanel class="relative transform overflow-hidden rounded-lg bg-white px-4 pb-4 pt-5 text-left shadow-xl transition-all sm:my-8 sm:w-full sm:max-w-lg sm:p-6">
              <div>
               
                <div class="mt-3 text-center sm:mt-5">
                    <div>
                      <label
                        for="text"
                        class="block text-sm font-medium leading-6 text-gray-900"
                        >category</label
                      >
                      <input
                        type="text"
                        name="text"
                        id="text"
                        v-model="category"
                        class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
                      />
                    </div>
                    <div>
                      <label
                        for="text"
                        class="block text-sm font-medium leading-6 text-gray-900"
                        >skill</label
                      >
                      <input
                        type="text"
                        name="text"
                        id="text"
                        v-model="skill"
                        class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
                      />
                    </div>
                    <div>
                      <label
                        for="text"
                        class="block text-sm font-medium leading-6 text-gray-900"
                        >question</label
                      >
                      <input
                        type="text"
                        name="text"
                        id="text"
                        v-model="question"
                        class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
                      />
                    </div>
                    <div>
                      <label
                        for="text"
                        class="block text-sm font-medium leading-6 text-gray-900"
                        >answer</label
                      >
                      <input
                        type="text"
                        name="text"
                        id="text"
                        v-model="answer"
                        class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
                      />
                    </div>
                    <div>
                      <label
                        for="text"
                        class="block text-sm font-medium leading-6 text-gray-900"
                        >sub_skill</label
                      >
                      <input
                        type="text"
                        name="text"
                        id="text"
                        v-model="sub_skill"
                        class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
                      />
                    </div>
                    <div>
                      <label
                        for="text"
                        class="block text-sm font-medium leading-6 text-gray-900"
                        >question_url</label
                      >
                      <input
                        type="text"
                        name="text"
                        id="text"
                        v-model="question_url"
                        class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
                      />
                    </div>
                    <div>
                      <label
                        for="text"
                        class="block text-sm font-medium leading-6 text-gray-900"
                        >answer_hint</label
                      >
                      <input
                        type="text"
                        name="text"
                        id="text"
                        v-model="answer_hint"
                        class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
                      />
                    </div>
                    <div>
                      <label
                        for="text"
                        class="block text-sm font-medium leading-6 text-gray-900"
                        >explanation</label
                      >
                      <input
                        type="text"
                        name="text"
                        id="text"
                        v-model="explanation"
                        class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
                      />
                    </div>
                  
                </div>
              </div>
              <div class="mt-5 sm:mt-6 sm:grid sm:grid-flow-row-dense sm:grid-cols-2 sm:gap-3">
                <div @click="open = false">
                <button type="button"
                class="inline-flex w-full justify-center rounded-md bg-indigo-600 px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600 sm:col-start-2"
                @click="postData1()">Save</button></div>
                <div>
                <button type="button" 
                class="mt-3 inline-flex w-full justify-center rounded-md bg-white px-3 py-2 text-sm font-semibold text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 hover:bg-gray-50 sm:col-start-1 sm:mt-0"
                 @click="open = false" ref="cancelButtonRef">Cancel</button></div>
              </div>
            </DialogPanel>
          </TransitionChild>
        </div>
      </div>
    </Dialog>
  </TransitionRoot>
</template>
<script setup>
import { ref } from 'vue'
import { Dialog, DialogPanel, DialogTitle, TransitionChild, TransitionRoot } from '@headlessui/vue'
import { CheckIcon } from '@heroicons/vue/24/outline'
const emits = defineEmits(["post-data"]);
const props=defineProps({
    open: { type: Boolean, default: false },
   
})
const category=ref("")
const skill=ref("")
const question=ref("")
const answer=ref("")
 const  sub_skill=ref("")
const  question_url=ref("")
const answer_hint=ref("")
const  explanation=ref("")

const postData1 = async () => {
  open.value = false;
  let form = {
    category: category.value,
    skill:skill.value,
    question_type:  "text",
    question: question.value,
    answer_type: "short",
    answer: answer.value,
    answer_rules: {},
    question_url: question_url.value,
    answer_hint: answer_hint.value,
    explanation: explanation.value,
    difficulty_level: "easy",
    marks: 0,
    question_rules: {},
    mark_rules: {},
    id:0,
    sub_skill:sub_skill.value
  };
  emits("post-data", form);
};

</script>