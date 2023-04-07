<h3>JSP 경로</h3>
<hr>
<p>
    자바스크립트 파일에 이미지 파일 경로를 상대경로로 지정하려면 자바스크립트에서 경로가 출발하는 게 아니라, jsp에서 경로가 출발해야 한다.<br>
    <p></p>
    그러나 css 파일에서 백그라운드 이미지 파일 경로를 상대 경로로 지정하려면, css 파일에서부터 경로가 출발해야 한다.<br>
    css폴더와 imgs 폴더는 같은 경로에 존재한다. 그리고, imgs폴더 밑에 바로 이미지 파일을 놓는 게 아니라, priceComapre 폴더 밑에 이미지를 넣었다.<br>
    그래서 "../imgs/priceCompare/cart.png"로 상대경로를 지정했는데 이미지가 나오지 않았다. <br>
    그럴 때, ../ 를 /resources로 바꿨더니 나왔다. <br>
    => /resources/imgs/priceCompare/cart.png
</p>