//HTML코드 & CSS코드

//HTML코드
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Style 오늘</title>
    <link rel="stylesheet" href="index.css">
</head>
<body>
    <header>
        <h1>Style list</h1>
    </header>
    <main>
        <!-- 상품 1 -->
        <section class="product">
            <img src="https://cdn.funshop.co.kr/products/0000118313/vs_image800.jpg?1650765660" alt="오버핏 티셔츠" style="width:100%;max-width:300px;">
            <h2>오버핏 티셔츠</h2>
            <p>이 상품은 고품질 재료로 만들어져 있으며, 오랫동안 사용할 수 있습니다.</p>
            <p class="price">가격: ₩20,000</p>
            <button type="button" onclick="alert('구매가 완료되었습니다!');">구매하기</button>
        </section>
        <!-- 상품 2 -->
        <section class="product">
            <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTizfM_rlIr6aQ4oysXotOuRaBnC2ehgh9U2w&s" alt="캐주얼 바지" style="width:100%;max-width:300px;">
            <h2>청 바지</h2>
            <p>평소에 입을 수 있는 데님 일자 핏 청바지 입니다. </p>
            <p class="price">가격: ₩30,000</p>
            <button type="button" onclick="alert('구매가 완료되었습니다!');">구매하기</button>
        </section>
        <!-- 상품 3 -->
        <section class="product">
            <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTKTimxQ7LeDxuwCO8bw85Fcm2ZOjDEi88Us-GS_2uqXg&s" alt="흑청바지" style="width:100%;max-width:300px;">
            <h2>흑 청바지</h2>
            <p>어디에나 매치할 수 있는 데일리 흑청바지입니다.</p>
            <p class="price">가격: ₩35,000</p>
            <button type="button" onclick="alert('구매가 완료되었습니다!');">구매하기</button>
        </section>
        <!-- 상품 4 -->
        <section class="product">
            <img src="https://argen.kr/web/product/big/201709/532_shop1_991253.jpg" alt="액세서리" style="width:100%;max-width:300px;">
            <h2>목걸이</h2>
            <p>가볍게 매치할 수 있는 은 목걸이로 포인트가 되기 좋습니다.</p>
            <p class="price">가격: ₩15,000</p>
            <button type="button" onclick="alert('구매가 완료되었습니다!');">구매하기</button>
        </section>
    </main>
    <footer>
        <nav>
            <ul>
                <li><a href="/">홈</a></li>
                <li><a href="contact.html">문의 게시판</a></li>
                <li><a href="FAQs.html">FAQs</a></li>
                <li><a href="more.html">More</a></li>  


            </ul>
        </nav>
        <p>저작권 © Since 2024 TD.cm 회사 대표 : 토마스 대표 번호 : 032-886-5431
            <br>
            본 회사의 사업 저작권은 회사 대표 토마스에 있으며, 가맹점 관련 문의는 대표의 개인번호로 연락 바랍니다. 
        </p>
    </footer>
</body>
</html>

//CSS코드

/* Body and typography styles */
body {
    font-family: 'Malgun Gothic', '맑은 고딕';
    font-smooth: auto;
    margin: 0;
    padding: 0;
    background: #f4f4f4;
}

header {
    background: #000000;
    color: white;
    padding: 10px 15px;
    text-align: center;
}

main {
    padding: 20px;
    text-align: center;
}

.product img {
    max-width: 100%;
    height: auto;
}

.price {
    font-size: 20px;
    color: #333;
}

/* Button styles */
button {
    background: #000000;
    color: white;
    border: none;
    padding: 10px 20px;
    cursor: pointer;
    font-size: 16px;
}

button:hover {
    background: #747474;
}

/* Footer styles */
footer {
    background: #333;
    color: white;
    text-align: center;
    padding: 10px 0;
    width: 100%;
    box-shadow: 0 -2px 10px rgba(0,0,0,0.1); /* 상단 그림자 효과 추가 */
}

/* Navigation styles */
ul {
    list-style-type: none; 
    padding: 0;           
    margin: 0;             
    display: flex;       
    justify-content: center; 
    flex-wrap: wrap;      
}

li {
    padding: 0 10px; /* Changed from float: left to padding for better spacing */
}

li:not(:last-child)::after {
    content: " | ";
}

a {
    text-decoration: none;
    color: white;
}

a:hover {
    text-decoration: underline;
    color: rgb(113, 113, 255);
}
