<!-- scriptの中はjsでその中にはんすうを作っている -->
<script>
	// name変数を宣言する
	let name = 'world';
	// src変数
	let src = 'favicon.png';
	// string変数
	let string = `this string contains some <strong>HTML!!!</strong>`;
	// count変数
	let count = 0;
	// count変数を二倍にするにしたものdoubled変数に入れる
	// $:意味がわからない,letにすると計算してくれない（だから計算白的な意味？）
	$: doubled = count * 2;

	
	$: if (count >= 10) {
		alert('count is dangerously high!');
		count = 9;
	}
// HTML側の引数handleClickが押されたとき
	// functionはjsの引数に指定したものに返すもの？
	function handleClick() {
		count += 1;
	}
</script>

<!-- Hello world!にtailwindcssでスタイルをつける -->
<h1 class="text-3xl font-bold underline">Hello world!</h1>
<!-- マークアップからnameを参照する -->
<h2>Hello {name}!</h2>
<!-- srcを参照 -->
<img {src} alt="svelte" />
<!-- {@html ...} という特別なタグを使う https://svelte.jp/tutorial/html-tags -->
<p>{@html string}</p>

<!--　handleClickはbuttonが押されたときの動き -->
<!-- on:clickはボタンがclickしたときに起動する処理(handleClick変数の処理) -->
<button on:click={handleClick}>
	<!-- ?がif文っぽいtrue->time false->times -->
	Clicked {count} {count === 1 ? 'time' : 'times'}

	
</button>

<!-- count変数の中とcountの値を２倍したdoubled変数 -->
<p>{count} doubled is {doubled}</p>