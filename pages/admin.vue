<template>
  <div>
    <h2>Admin</h2>
    <p>{{ resp }}</p>
  </div>
</template>
<script>
export default {
  async asyncData({ $axios }) {
    // 取得先のURL
    const url = "http://localhost:1880/hogeoge";
    // リクエスト（Get）
    const response = await $axios.$get(url);
    // 配列で返ってくるのでJSONにして返却
    return {
      resp: response
    };
  }
};
</script>
