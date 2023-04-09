<template>
    <h2>Banks</h2>
    <div  class="flex align item-center justify-between">
        <h2></h2>
<button type="button"  @click="opensidebar()"
class="rounded-full bg-indigo-600 px-4 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">
   + AddProjects</button>
</div>
<Add v-if="open" :open="open" @post-data="postdata" ></Add>
<List  :templatedata="templateData"></List>
<Edit></Edit>
</template>
<script setup>
const open=ref(false)
const templateData=ref([])

//post
const postdata = async (form) => {
    console.log("POSTDATA",form)
  let options = {
    method: "POST",
    headers: {
      "Content-Type": "application/json",
      Accept: "application/json",
      Authorization:
        "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1IjoiYmZlOTY3MDc0YzJhNGVlNDhiODFlYWU1ZmU5ZThhMjkiLCJkIjoiMTY4MDA4MSIsInIiOiJzYSIsInAiOiJmcmVlIiwiYSI6ImZpbmRlci5pbyIsImwiOiJ1czEiLCJleHAiOjE2ODMyNzkyNzB9._HklK6rl9AWu3mp4kRdrOIsxyEP-jNpG7kgF3K-5GlA",
    },
    body:form
  };
 const data= await useAuthLazyFetchPost(
    "https://v7-stark-db-orm.mercury.infinity-api.net/api/question-bank/bulk",
    options
  );
   templateData.value=data.data._rawValue
}

//get
const getData = useAuthLazyFetch(
  "https://v7-stark-db-orm.mercury.infinity-api.net/api/question-bank/?offset=0&limit=100&sort_column=id&sort_direction=desc"
);
templateData.value = getData.data._rawValue;
console.log("get--1222111",templateData)

function opensidebar() {
  open.value = !open.value;
}
</script>