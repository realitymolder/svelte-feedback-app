<script lang="ts">

import FeedbackList from './components/FeedbackList.svelte'

let feedBack =[
  {
    id: 1,
    rating: 10,
    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. consequuntur vel vitae commodi alias voluptatem est voluptatum ipsa quae.',
  },
  {
    id: 2,
    rating: 9,
    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. consequuntur vel vitae commodi alias voluptatem est voluptatum ipsa quae.',
  },
  {
    id: 3,
    rating: 8,
    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. consequuntur vel vitae commodi alias voluptatem est voluptatum ipsa quae.',
  },
]
const deleteFeedback = (e) => {
  const itemId = e.detail;
  feedBack = feedBack.filter((item) => item.id != itemId);
};
</script>

<main class="container">
<FeedbackList {feedBack} on:delete-feedback={deleteFeedback}/>
</main>
