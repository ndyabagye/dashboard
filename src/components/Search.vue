<template>
  <div>
    <div class="input-group py-4 px-5">
      <div class="input-group-text">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="16"
          height="16"
          fill="currentColor"
          class="bi bi-search"
          viewBox="0 0 16 16"
        >
          <path
            d="M11.742 10.344a6.5 6.5 0 1 0-1.397 1.398h-.001c.03.04.062.078.098.115l3.85 3.85a1 1 0 0 0 1.415-1.414l-3.85-3.85a1.007 1.007 0 0 0-.115-.1zM12 6.5a5.5 5.5 0 1 1-11 0 5.5 5.5 0 0 1 11 0z"
          />
        </svg>
      </div>
      <input
        type="text"
        class="form-control"
        v-model="text"
        aria-label="Text input with radio button"
        placeholder="Search...."
      />
    </div>
    <div class="ps-5 position-relative mt-5">
      <h2>
        Hi, {{ username }}
        <span
          class="badge bg-danger position-absolute top-0 start-100 translate-middle rounded-circle"
          >{{ notifications }}</span
        >
      </h2>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      notifications: 23,
      username: 'Mickey',
      text: '',
    };
  },
};
</script>

<style>
.input-group-text,
.bi bi-search,
.form-control {
  background-color: #f7f8fa !important;
}

.start-100 {
  left: 28% !important;
}
</style>
