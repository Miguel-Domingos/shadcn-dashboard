<script setup lang="ts">
definePageMeta({
  alias: "/404",
  layout: false,
});

const router = useRouter();
</script>

<template>
  <div class="h-svh">
    <div
      class="m-auto px-4 flex h-full w-full flex-col items-center justify-center gap-2"
    >
      <h1 class="text-[7rem] leading-tight font-bold">404</h1>
      <span class="font-medium">Oops! Page Not Found!</span>
      <p class="text-muted-foreground text-center flex flex-col">
        <span> It seems like the page you're looking for </span>
        <span> does not exist or might have been removed. </span>
      </p>
      <div class="mt-6 flex gap-4">
        <Button variant="outline" @click="router.go(-1)"> Go Back </Button>
        <Button @click="router.push('/')">Back to Home</Button>
      </div>
    </div>
  </div>
</template>
