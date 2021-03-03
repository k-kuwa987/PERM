<template>
  <div>
    <h2>Welcome to PERspective Manager</h2>
    <p>
      これはバスに関する情報を様々なユーザーの視点から確認する際のデモです．
    </p>

    <p>
      各視点におけるコンテンツは，適切な制限や補正が施された上で提供されています
    </p>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      posts: []
    };
  },
  async asyncData({ $axios }) {
    // 取得先のURL
    const url = "http://localhost:1880/hogehoge";
    // リクエスト（Get）
    const response = await $axios.$get(url);
    // 配列で返ってくるのでJSONにして返却
    console.log(response);
    return {
      posts: response
    };
  }
};
</script>
