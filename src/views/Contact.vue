<template>
  <div class="contact">
    <h1>Contact me</h1>
    <form class="contact__form" @submit.prevent="sendEmail">
      <label for="name">Name</label>
      <input name="name" type="text" required v-model="name" />
      <label for="email">Email</label>
      <input name="email" type="email" required v-model="email" />
      <label for="message">Message</label>
      <textarea
        name="message"
        type="text"
        required
        maxlength="200"
        v-model="message"
      ></textarea>
      <button type="submit">Send</button>
    </form>
  </div>
</template>

<script>
import emailjs from "emailjs-com";
import { ref } from "vue";
import { useRouter } from "vue-router";

export default {
  setup() {
    const name = ref("");
    const email = ref("");
    const message = ref("");
    const router = useRouter();

    const sendEmail = (e) => {
      try {
        emailjs.sendForm(
          "service_lyn59xl",
          "template_fmr54uh",
          e.target,
          "user_pxiJSeQHXreuruLhEMREn",
          {
            name,
            email,
            message,
          }
        );
        name.value = "";
        email.value = "";
        message.value = "";
        alert("Message sent!");
        router.push("/");
      } catch (error) {
        console.log({ error });
      }
    };

    return {
      name,
      email,
      message,
      sendEmail,
    };
  },
};
</script>

<style scoped>
button {
  background: var(--black);
}
.contact {
  padding: 3rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: fit-content;
  border-radius: 1rem;
  margin: 0 auto;
  margin-top: 4.8rem;
}

.contact__form {
  display: flex;
  flex-direction: column;
  width: 36rem;
}

textarea {
  font: inherit;
  font-size: 1.6rem;
  background: transparent;
  border: none;
  resize: none;
  height: 10rem;
  border-bottom: 1px solid #000;
  margin-bottom: 1rem;
}

textarea:focus {
  outline: none;
}

h1 {
  font-size: 3.6rem;
  margin-bottom: 1.6rem;
}
</style>
