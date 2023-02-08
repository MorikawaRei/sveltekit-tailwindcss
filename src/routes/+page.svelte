<!-- scriptで変数を作る -->
<script>
	// name変数を宣言する
	let name = 'world';
	// src変数
	let src = 'favicon.png';
	// string変数
	let string = `this string contains some <strong>HTML!!!</strong>`;
</script>

<!-- Hello world!にtailwindcssでスタイルをつける -->
<h1 class="text-3xl font-bold underline">Hello world!</h1>
<!-- マークアップからnameを参照する -->
<h2>Hello {name}!</h2>
<!-- srcを参照 -->
<img {src} alt="svelte" />
<!-- {@html ...} という特別なタグを使う https://svelte.jp/tutorial/html-tags -->
<p>{@html string}</p>
