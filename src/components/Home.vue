<template>
  <div class="home">
    <h1>Let's Chrome Tab Challenge!!</h1>
    <button @click="start()">Start（自己責任でお願いします。開発者は一切の責任を負いません。）</button>
    
    <p>Startボタンをクリックすると、タブが100個開きます。（ポップアップを許可する必要あり）</p>
    <p>いいパソコンの指標って、「Chromeのタブをどれくらい開けるか」ですよね？<br>
      当Webアプリは、Chromeのタブをどれくらい開くことができるかでパソコンのスペック比較する未来を目指し開発を進めてまいります。
    </p>

    <h2>使い方</h2>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/D_2-L0RFXDY" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe><br>

    <a href="https://rkdora.hatenablog.com/entry/2020/06/24/003240">[rkdora's Blog] VueでWebアプリを爆速デプロイしていく</a><br>
    <a href="https://github.com/rkdora/chrome-tab-challenge/blob/master/src/components/Home.vue">ソースコード</a>
  </div>
</template>

<script>
export default {
  name: 'home',
  methods: {
    start() {
      for (let i = 0; i < 100; i++) {
        if (window.open('https://www.yahoo.co.jp/')) {
          console.log('No.' + i + ' success!');
        } else {
          console.log('No.' + i + ' blocked.');
        }
      }
    }
  }
}
</script>

<style scoped>
</style>
