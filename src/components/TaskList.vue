<template>
  <div>
    <div class="form-check">
      <label class="form-check-label" for="flexCheckDefault">
        {{ myTask.act }}
      </label>

      <input
        class="form-check-input"
        type="checkbox"
        value=""
        id="flexCheckDefault"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: "TaskList",
  props: ["myTask"],
};
</script>