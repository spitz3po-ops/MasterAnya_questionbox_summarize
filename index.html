<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<title>質問箱まとめ</title>

<style>
body {
  font-family: "Hiragino Kaku Gothic ProN", sans-serif;
  margin: 0;
  background: linear-gradient(135deg, #fceff9, #e0f7fa);
}

header {
  background: linear-gradient(90deg, #ff9a9e, #fad0c4);
  color: white;
  padding: 20px;
  text-align: center;
  font-size: 22px;
}

.container { padding: 20px; }

.card {
  background: white;
  padding: 15px;
  margin-bottom: 10px;
  border-radius: 12px;
  cursor: pointer;
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
}

.hidden { display: none; }

button {
  margin-top: 10px;
  padding: 10px;
  border: none;
  border-radius: 8px;
  background: #ff9a9e;
  color: white;
  cursor: pointer;
}

.danger { background: #ff6b6b; }

input, textarea {
  width: 100%;
  margin-top: 8px;
  padding: 8px;
}
</style>
</head>

<body>

<header>文系大学院生アーニャbotの質問箱まとめ</header>

<!-- ホーム -->
<div class="container" id="home">
  <h2>ジャンルを選択</h2>
  <div id="categoryList"></div>

  <button onclick="openCategoryEditor()">＋ 新しいジャンルを追加</button>
</div>

<!-- ジャンル追加ページ -->
<div class="container hidden" id="categoryEditor">
  <h2>ジャンルを追加</h2>

  <input id="newCategory" placeholder="ジャンル名を入力">

  <button onclick="addCategory()">作成</button>
  <button onclick="goHome()">戻る</button>
</div>

<!-- カテゴリ -->
<div class="container hidden" id="categoryPage">
  <h2 id="categoryTitle"></h2>
  <div id="postList"></div>

  <button onclick="openEditor()">＋投稿</button>
  <button onclick="goHome()">戻る</button>
</div>

<!-- 投稿 -->
<div class="container hidden" id="postPage">
  <h2 id="postTitle"></h2>
  <p id="postContent"></p>
  <h3>回答</h3>
  <p id="postAnswer"></p>

  <button onclick="editPost()">編集</button>
  <button class="danger" onclick="deletePost()">削除</button>
  <button onclick="goBack()">戻る</button>
</div>

<!-- 編集 -->
<div class="container hidden" id="editor">
  <h2 id="editorTitle"></h2>

  <label>タイトル</label>
  <input id="titleInput">

  <label>本文</label>
  <textarea id="contentInput"></textarea>

  <label>回答</label>
  <textarea id="answerInput"></textarea>

  <button onclick="savePost()">保存</button>
  <button onclick="goBack()">戻る</button>
</div>

<script>
let categories = JSON.parse(localStorage.getItem("categories")) || ["進路","研究"];
let posts = JSON.parse(localStorage.getItem("posts")) || [];

let currentCategory = "";
let currentPostIndex = null;

renderCategories();

// ジャンル一覧
function renderCategories() {
  const list = document.getElementById("categoryList");
  list.innerHTML = "";

  categories.forEach(cat => {
    const div = document.createElement("div");
    div.className = "card";
    div.innerText = cat;
    div.onclick = () => openCategory(cat);
    list.appendChild(div);
  });
}

// ジャンル追加ページへ
function openCategoryEditor() {
  hideAll();
  document.getElementById("categoryEditor").classList.remove("hidden");
}

// ジャンル追加
function addCategory() {
  const name = document.getElementById("newCategory").value;
  if (!name) return;

  categories.push(name);
  localStorage.setItem("categories", JSON.stringify(categories));

  document.getElementById("newCategory").value = "";

  alert("ジャンルを追加しました");
  goHome();
  renderCategories();
}

// カテゴリ表示
function openCategory(cat) {
  currentCategory = cat;
  hideAll();
  document.getElementById("categoryPage").classList.remove("hidden");
  document.getElementById("categoryTitle").innerText = cat;
  renderPosts();
}

// 投稿一覧
function renderPosts() {
  const list = document.getElementById("postList");
  list.innerHTML = "";

  posts.forEach((p, i) => {
    if (p.category === currentCategory) {
      const div = document.createElement("div");
      div.className = "card";
      div.innerText = p.title;
      div.onclick = () => openPost(i);
      list.appendChild(div);
    }
  });
}

// 投稿表示
function openPost(index) {
  currentPostIndex = index;
  hideAll();
  const p = posts[index];

  document.getElementById("postPage").classList.remove("hidden");
  document.getElementById("postTitle").innerText = p.title;
  document.getElementById("postContent").innerText = p.content;
  document.getElementById("postAnswer").innerText = p.answer;
}

// 編集
function editPost() {
  const p = posts[currentPostIndex];

  hideAll();
  document.getElementById("editor").classList.remove("hidden");
  document.getElementById("editorTitle").innerText = "編集";

  document.getElementById("titleInput").value = p.title;
  document.getElementById("contentInput").value = p.content;
  document.getElementById("answerInput").value = p.answer;
}

// 新規投稿
function openEditor() {
  currentPostIndex = null;
  hideAll();
  document.getElementById("editor").classList.remove("hidden");
  document.getElementById("editorTitle").innerText = "新規投稿";
}

// 保存
function savePost() {
  const newData = {
    category: currentCategory,
    title: document.getElementById("titleInput").value,
    content: document.getElementById("contentInput").value,
    answer: document.getElementById("answerInput").value
  };

  if (currentPostIndex !== null) {
    posts[currentPostIndex] = newData;
  } else {
    posts.push(newData);
  }

  localStorage.setItem("posts", JSON.stringify(posts));

  currentPostIndex = null;

  document.getElementById("titleInput").value = "";
  document.getElementById("contentInput").value = "";
  document.getElementById("answerInput").value = "";

  openCategory(currentCategory);
}

// 削除
function deletePost() {
  if (confirm("削除しますか？")) {
    posts.splice(currentPostIndex, 1);
    localStorage.setItem("posts", JSON.stringify(posts));
    openCategory(currentCategory);
  }
}

// 戻る
function goBack() {
  openCategory(currentCategory);
}

// ホーム
function goHome() {
  hideAll();
  document.getElementById("home").classList.remove("hidden");
}

// 非表示
function hideAll() {
  document.querySelectorAll(".container").forEach(el => el.classList.add("hidden"));
}
</script>

</body>
</html>
