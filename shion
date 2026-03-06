<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<title>ガチャゲーム</title>

<style>
body{
    font-family: sans-serif;
    background: linear-gradient(135deg,#4facfe,#00f2fe);
    text-align:center;
    padding-top:50px;
    color:white;
}

h1{
    font-size:40px;
}

.gacha-box{
    margin:30px auto;
    width:300px;
    height:200px;
    background:white;
    color:black;
    border-radius:15px;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:24px;
    font-weight:bold;
    box-shadow:0 10px 20px rgba(0,0,0,0.3);
}

button{
    padding:15px 40px;
    font-size:20px;
    border:none;
    border-radius:10px;
    background:gold;
    cursor:pointer;
    transition:0.2s;
}

button:hover{
    transform:scale(1.1);
}

.spin{
    animation:spin 0.5s linear infinite;
}

@keyframes spin{
    from{transform:rotateY(0deg);}
    to{transform:rotateY(360deg);}
}

.rarity-SSR{color:red;}
.rarity-SR{color:purple;}
.rarity-R{color:blue;}
.rarity-N{color:gray;}

</style>
</head>

<body>

<h1>🎰 ガチャゲーム 🎰</h1>

<div id="result" class="gacha-box">
    ガチャを回そう！
</div>

<button onclick="drawGacha()">ガチャを引く</button>

<script>

const characters = [
    {name:"伝説のドラゴン", rarity:"SSR", rate:3},
    {name:"天空の騎士", rarity:"SR", rate:12},
    {name:"魔法使い", rarity:"SR", rate:12},
    {name:"弓使い", rarity:"R", rate:30},
    {name:"戦士", rarity:"R", rate:30},
    {name:"村人", rarity:"N", rate:13}
];

function drawGacha(){

    const resultBox = document.getElementById("result");

    resultBox.classList.add("spin");
    resultBox.innerText="抽選中...";

    setTimeout(()=>{

        resultBox.classList.remove("spin");

        let rand = Math.random()*100;
        let sum = 0;

        for(let c of characters){

            sum += c.rate;

            if(rand <= sum){

                resultBox.className="gacha-box rarity-"+c.rarity;
                resultBox.innerHTML = `
                ${c.rarity}<br>
                ${c.name}
                `;
                break;
            }
        }

    },2000);

}

</script>

</body>
</html>
