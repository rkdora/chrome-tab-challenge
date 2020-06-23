<template>
  <div class="home">
    <h1>Let's Chrome Tab Challenge!!</h1>
    <button @click="start()">Start（自己責任でお願いします。開発者は一切の責任を負いません。）</button>
    
    <p>Startボタンをクリックすると、タブが100個開きます。（ポップアップを許可する必要あり）</p>
    <p>いいパソコンの指標って、「Chromeのタブをどれくらい開けるか」ですよね？<br>
      当Webアプリは、Chromeのタブをどれくらい開くことができるかでパソコンのスペック比較する未来を目指し開発を進めてまいります。
    </p>
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
