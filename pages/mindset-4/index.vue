<template>
  <div>
    <h3>4th Grade Mindset {{ week }} of {{ items.length }}</h3>
    <h1>{{ item.title }}</h1>
    <h3>Writing Prompt:</h3>
    <p>{{ item.writing }}</p>
    <h3>Conversation Starter:</h3>
    <p>{{ item.conversation }}</p>
    <h3>Quiz:</h3>
    <p>{{ item.quiz }}</p>
  </div>
</template>

<script lang="ts" setup>
import { useRoute } from "vue-router";
const router = useRoute();

const items = [
  {
    title: "Understanding Growth Mindset vs. Fixed Mindset",
    writing:
      "Think about something you were once bad at but got better with practice. How did you do it?",
    conversation:
      "What’s something you’d like to get better at? How can you practice to improve?",
    quiz: "What does it mean to have a “growth mindset”?",
  },
  {
    title: "The Power of Yet",
    writing: "Write about something you can’t do yet but want to learn.",
    conversation:
      "How can adding “yet” to “I can’t do this” make you feel better about learning?",
    quiz: "What is the power of adding the word “yet” to your thinking?",
  },
  {
    title: "Embracing Mistakes as Learning Opportunities",
    writing:
      "Tell a story about a time you made a mistake. What did you learn from it?",
    conversation: "Why do you think it’s okay to make mistakes?",
    quiz: "True or False: Making mistakes is a bad thing.",
  },
  {
    title: "Overcoming Self-Doubt",
    writing:
      "Write about a time you doubted yourself. What helped you feel better?",
    conversation:
      "What do you say to yourself when you feel like you can’t do something?",
    quiz: "What can you do when you start to doubt yourself?",
  },
  {
    title: "The Importance of Trying Hard",
    writing:
      "Think about a time when you kept trying even though something was hard. What happened?",
    conversation:
      "Why is it important to keep trying, even when things are tough?",
    quiz: "What does it mean to “persevere”?",
  },
  {
    title: "Setting Simple Goals",
    writing: "What’s a small goal you can set for yourself this week?",
    conversation: "How do you feel when you achieve a goal, even a small one?",
    quiz: "What’s one thing that can help you reach a goal?",
  },
  {
    title: "Managing Worry",
    writing:
      "Write about something that worries you. What helps you feel less worried?",
    conversation: "What do you do when you feel worried or stressed?",
    quiz: "What is one way to help yourself feel less worried?",
  },
  {
    title: "Being Kind to Yourself",
    writing: "How can you be kind to yourself when you make a mistake?",
    conversation: "Why is it important to say nice things to yourself?",
    quiz: "True or False: You should be as kind to yourself as you are to your friends.",
  },
  {
    title: "Bouncing Back After a Tough Day",
    writing:
      "Write about a day that didn’t go well. How did you feel better afterward?",
    conversation: "What helps you feel better when you’re having a tough day?",
    quiz: "What does it mean to “bounce back”?",
  },
  {
    title: "Understanding Others’ Feelings",
    writing:
      "Think of a time when you helped a friend who was feeling sad. What did you do?",
    conversation: "How can you tell when someone else is feeling upset?",
    quiz: "What is it called when you try to understand how someone else feels?",
  },
  {
    title: "Listening Well",
    writing:
      "Why is it important to listen carefully when someone is talking to you?",
    conversation:
      "How can you show someone that you’re really listening to them?",
    quiz: "What’s one thing you can do to be a good listener?",
  },
  {
    title: "Understanding Your Own Feelings",
    writing:
      "Write about a time when you felt a strong emotion, like being really happy or really mad. What did you do?",
    conversation: "Why is it important to know what you’re feeling?",
    quiz: "True or False: Understanding your feelings can help you make better choices.",
  },
  {
    title: "Staying Calm",
    writing:
      "Write about a time when you felt upset. What helped you calm down?",
    conversation: "What do you do to stay calm when you feel angry or upset?",
    quiz: "What is one way to help yourself stay calm?",
  },
  {
    title: "Dealing with Peer Pressure",
    writing:
      "Write about a time when someone tried to get you to do something you didn’t want to do. What did you do?",
    conversation:
      "What can you do if a friend wants you to do something you know is wrong?",
    quiz: "What does it mean to stand up for yourself?",
  },
  {
    title: "Being Grateful",
    writing: "What are three things you are thankful for today?",
    conversation:
      "How does thinking about things you’re thankful for make you feel?",
    quiz: "What is one thing you’re grateful for right now?",
  },
  {
    title: "Using Positive Words",
    writing: "Write down three nice things you can say to yourself each day.",
    conversation:
      "How do you feel when someone says something nice to you? How can you say nice things to yourself?",
    quiz: "Why is it important to use positive words when talking to yourself?",
  },
  {
    title: "Making Good Friends",
    writing:
      "What makes someone a good friend? How can you be a good friend to others?",
    conversation:
      "What do you look for in a friend? How do you show kindness to your friends?",
    quiz: "What’s one thing you can do to be a good friend?",
  },
  {
    title: "Finishing Tasks",
    writing:
      "Think of a time when you didn’t finish something. What stopped you? How can you make sure to finish next time?",
    conversation:
      "What do you do to help yourself finish your work, even when it’s hard?",
    quiz: "What’s one way to help yourself finish a task?",
  },
  {
    title: "Listening to Feedback",
    writing:
      "Write about a time when someone gave you advice. Did you follow it? Why or why not?",
    conversation: "Why is it helpful to listen to advice from others?",
    quiz: "True or False: Listening to feedback can help you get better at things.",
  },
  {
    title: "Knowing Yourself",
    writing:
      "What’s one thing you’re really good at, and one thing you want to get better at?",
    conversation:
      "Why is it important to know what you’re good at and what you need to work on?",
    quiz: "What’s one way to learn more about yourself?",
  },
  {
    title: "Being Flexible",
    writing: "Write about a time when plans changed. How did you handle it?",
    conversation:
      "Why is it important to be able to go with the flow when things don’t go as planned?",
    quiz: "What does it mean to be flexible?",
  },
  {
    title: "Looking on the Bright Side",
    writing:
      "Write about a time when something didn’t go your way. How did you find something good in it?",
    conversation: "How can you stay positive even when things are tough?",
    quiz: "What’s one way to find the good in a bad situation?",
  },
  {
    title: "Setting Boundaries",
    writing:
      "Write about a time when you needed to say “no” to someone. How did it feel?",
    conversation: "Why is it important to know when to say “no”?",
    quiz: "What does it mean to set a boundary?",
  },
  {
    title: "Thinking About Your Day",
    writing:
      "What was the best part of your day today? What was the hardest part?",
    conversation:
      "Why is it good to think about what went well and what didn’t each day?",
    quiz: "What’s one good thing that happened to you today?",
  },
  {
    title: "Using Your Time Wisely",
    writing:
      "Write about how you spent your time today. What could you do differently tomorrow?",
    conversation:
      "How do you decide what to do first when you have lots of things to do?",
    quiz: "What’s one way to manage your time better?",
  },
  {
    title: "Solving Problems Peacefully",
    writing:
      "Think of a time when you had a disagreement with a friend. How did you solve it?",
    conversation:
      "What can you do to solve problems without getting into a fight?",
    quiz: "What’s one way to solve a problem with a friend?",
  },
  {
    title: "Being Patient",
    writing:
      "Write about a time when you had to wait for something. How did you stay patient?",
    conversation:
      "Why is it important to be patient, even when you don’t want to be?",
    quiz: "What does it mean to be patient?",
  },
  {
    title: "Having a Positive Attitude",
    writing:
      "How can a positive attitude help you when you’re trying something new?",
    conversation:
      "What can you do to stay positive, even when things are hard?",
    quiz: "True or False: A positive attitude can help you do better in school.",
  },
  {
    title: "Handling Big Feelings",
    writing:
      "Write about a time when you felt really strong emotions. What did you do to handle them?",
    conversation: "What do you do when you feel really mad or really sad?",
    quiz: "What’s one thing you can do when you feel a strong emotion?",
  },
  {
    title: "Asking for Help",
    writing:
      "Write about a time when you needed help. Who did you ask, and how did they help you?",
    conversation: "Why is it okay to ask for help when you need it?",
    quiz: "What’s one good reason to ask for help?",
  },
  {
    title: "Being Optimistic",
    writing:
      "Think about something you’re looking forward to. How does it make you feel?",
    conversation: "Why is it good to be hopeful about the future?",
    quiz: "What’s one thing that makes you feel excited about the future?",
  },
  {
    title: "Dealing with Negative Thoughts",
    writing:
      "Write about a negative thought you’ve had and how you can change it into a positive one.",
    conversation:
      "What do you do when you have a thought that makes you feel bad?",
    quiz: "What’s one way to change a negative thought into a positive one?",
  },
  {
    title: "Finding Support",
    writing:
      "Who do you turn to when you need support, and why do you choose them?",
    conversation:
      "Why is it important to have people in your life who support you?",
    quiz: "Who is someone you can count on for support?",
  },
  {
    title: "Body Language and Communication",
    writing:
      "How does your body show how you’re feeling, even when you’re not talking?",
    conversation:
      "How can you tell how someone is feeling just by looking at them?",
    quiz: "What is body language, and why is it important?",
  },
  {
    title: "Recognizing When You Need a Break",
    writing:
      "Write about a time when you felt really tired or overwhelmed. What did you do to feel better?",
    conversation: "How do you know when you need to take a break?",
    quiz: "What’s one sign that you might need a break?",
  },
  {
    title: "Taking Responsibility",
    writing:
      "Write about a time when you had to take responsibility for something you did. How did it feel?",
    conversation:
      "Why is it important to take responsibility for your actions?",
    quiz: "True or False: Taking responsibility means admitting when you’ve made a mistake.",
  },
];

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
