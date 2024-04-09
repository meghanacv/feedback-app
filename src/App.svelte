<script>
  import FeedbackList from "./components/FeedbackList.svelte";

  let feedback = [
    {
      id: "1",
      rating: 10,
      text: "Lorem ipsum dolor sit. amet consectetur, adipisicing elit Architecto",
    },
    {
      id: "2",
      rating: 8,
      text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Omnis in fuga veritatis aliquam sunt velit"
    },
    {
      id: "3",
      rating: 7,
      text: "Lorem ipsum dolor sit amet consectetur, adipisicing elit.",
    }
  ];

  const deleteFeedback = (e) => {
	const itemId = e.detail
	feedback = feedback.filter((item) => item.id !== itemId)
  }
</script>

<main class="container">
  <FeedbackList {feedback} on:delete-feedback={deleteFeedback}/>
  
</main>
