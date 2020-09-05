<template>
  <section class="container">
    <h1>Todoリスト</h1>
    <div class="addArea">
      <input type="text" name="addName" id="addName" placeholder="タスクを入力してください">
      <button id="addButton" class="button button--green">追加</button>
    </div>
    <div class="Filter">
      <button class="button button--gray is-active">全て</button>
      <button class="button button--gray">作業前</button>
      <button class="button button--gray">作業後</button>
      <button class="button button--gray">完了</button>
    </div>
    <table class="Lists">
      <thead>
        <tr>
        <th>タスク</th>
        <th>登録日時</th>
        <th>状態</th>
        <th></th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(item,index) in todos" :key="index">
        <td>テスト</td>
        <td>2020-04-30 17:00</td>
        <td><button class="button button--yet">作業前</button></td>
        <td><button class="button button--delete">削除</button></td>
        </tr>
      </tbody>
    </table>
  </section>
</template>

<script>
export default {}
</script>

<style>
.container {  
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
