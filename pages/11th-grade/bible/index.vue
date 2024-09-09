<template>
    <div>
      <h3>11th Grade Bible {{ week }} of {{ items.length }}</h3>
      <h1>{{ item.passage }}</h1>
      <h3>Learning:</h3>
      <ul>
        <li><a :href="getBibleGatewayUrl(item.passage)" target="_blank">Bible Gateway</a></li>
        <li><a :href="getYoutubeUrl(item.passage)" target="_blank">Videos</a></li>
        <li><a :href="getGoogleSearchUrl(item.passage)" target="_blank">Web Search</a></li>
      </ul>
      <h3>Assignment:</h3>
      <p>
        Each week, you'll have a new passage from the Bible to study.
        <ul>
            <li>Copy/paste the steps to the attached document to answer.</li>
            <li>Read the passage a couple times and look up any words you don't understand to get a good idea.</li>
            <li>Research the passage to find out what people say about it.</li>
            <li>Rewrite a the passage in IN YOUR OWN WORDS (paraphrase), not leaving out any details.</li>
            <li>Write about the passage using the “Discovery Bible Study” questions:
                <ul>
                    <li>1 Paragraph: What does this passage reveal about God?</li>
                    <li>1 Paragraph: What does this passage reveal about people?</li>
                    <li>1 Paragraph: If this passage is true, what would/should you change about your ways of thinking, behaviors or choices?</li>
                    <li>1 Paragraph: Who else in your life needs to learn these same lessons? Why?</li>
                </ul>
            </li>
            <li>Memorize your favorite verse or verses from this passage and demonstrate to an adult.</li>
            <li>This should result in a well-written and thoughtful document about the passage.</li>
        </ul>
      </p>
    </div>
  </template>
  
  <script lang="ts" setup>
  import { useRoute } from "vue-router";
  const router = useRoute();
  
  const items = [
  { passage: "Mark 2:1-17" },
    { passage: "Mark 4:1-20" },
    { passage: "Mark 5:1-20" },
    { passage: "Luke 7:37-50" },
    { passage: "Luke 15:11-32" },
    { passage: "Luke 17:11-19" },
    { passage: "Luke 18:9-14" },
    { passage: "Luke 19:1-10" },
    { passage: "Luke 4:14-22" },
    { passage: "Luke 5:1-11" },
    { passage: "John 15:1-11" },
    { passage: "Mark 8:27-37" },
    { passage: "Mark 9:17-32" },
    { passage: "Luke 23:32-49" },
    { passage: "John 20:1-18" },
    { passage: "Matthew 28:5-20" },
    { passage: "Psalm 33 & John 1" },
    { passage: "Genesis 3:1-21" },
    { passage: "Genesis 12, Genesis 15, & Galatians 3" },
    { passage: "Ezekiel 34 & John 10" },
    { passage: "Isaiah 61 & Luke 4" },
    { passage: "Isaiah 53" },
    { passage: "Luke 23:26-49" },
    { passage: "John 20:1-18" },
    { passage: "Mark 1:4-20" },
    { passage: "Mark 1:21-39" },
    { passage: "Mark 2:1-12" },
    { passage: "Mark 2:13-28" },
    { passage: "Mark 4:21-34" },
    { passage: "Mark 5:22-43" },
    { passage: "Mark 6:1-13" },
    { passage: "Mark 8:22-37" },
    { passage: "Mark 9:1-13" },
    { passage: "Mark 9:17-32" },
    { passage: "Mark 10:32-45" },
    { passage: "Mark 11:1-19" },
    { passage: "Mark 11:27-12:12" },
    { passage: "Mark 14:53-65" },
    { passage: "Mark 15:21-39" },
    { passage: "Mark 15:42-16:8" },
  ];

  function getYoutubeUrl(passage: string){
    return `https://www.youtube.com/results?search_query=${encodeURI(passage)}`;
  }

  function getGoogleSearchUrl(passage: string){
    return `https://www.google.com/search?q=${encodeURI(passage)}`;
  }

  function getBibleGatewayUrl(passage: string){
    return `https://www.biblegateway.com/passage/?search=${encodeURI(passage)}`;
  }

  const week = router.query.week || 1;
  const item = computed(() => items[week - 1]);
  </script>
  
  <style>
  .table {
    width: 100%;
    border-collapse: collapse;
  }
  
  .table tr td {
    border-bottom: solid 2px #000;
    height: 100px;
  }
  </style>
  