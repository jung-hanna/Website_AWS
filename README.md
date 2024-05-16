// index HTML코드 & CSS코드
// index파일은 메인 홈에서 상품 목록으로 갈 때 나오는 페이지
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Style 오늘</title>
    <link rel="stylesheet" href="index.css">
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
</head>
<body>
    <div class="sidebar">
        <ul class="menu">
            <li><a href="mainhome.html">Style List</a></li>
            <li><a href="contact.html">Contact</a></li>
            <li><a href="about.html">About</a></li>
            <li><a href="javascript:void(0)" id="mypage-link">My Page</a></li>
        </ul>
    </div>
    <div class="main-content">
        <header>
            <h1>Style 오늘</h1>
            <div class="header-buttons">
                <img src="Black label shopping cart icon free download.png" alt="Cart" class="cart-icon" id="cart-icon">
                <button class="mypage-button" id="mypage-button">마이페이지</button>
                <button class="login-button" onclick="location.href='login.html'">로그인</button>
            </div>
        </header>
        <main>
            <div class="products">
                <!-- 상품 1 -->
                <section class="product">
                    <img src="https://cdn.funshop.co.kr/products/0000118313/vs_image800.jpg?1650765660" alt="오버핏 티셔츠">
                    <h2>오버핏 티셔츠</h2>
                    <p>이 상품은 고품질 재료로 만들어져 있으며, 오랫동안 사용할 수 있습니다.</p>
                    <p class="price">가격: ₩20,000</p>
                    <button type="button" onclick="alert('구매가 완료되었습니다!');">구매하기</button>
                    <button type="button" onclick="addToCart('오버핏 티셔츠', '₩20,000')">장바구니</button>
                </section>
                <!-- 상품 2 -->
                <section class="product">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTizfM_rlIr6aQ4oysXotOuRaBnC2ehgh9U2w&s" alt="캐주얼 바지">
                    <h2>청 바지</h2>
                    <p>평소에 입을 수 있는 데님 일자 핏 청바지 입니다.</p>
                    <p class="price">가격: ₩30,000</p>
                    <button type="button" onclick="alert('구매가 완료되었습니다!');">구매하기</button>
                    <button type="button" onclick="addToCart('청 바지', '₩30,000')">장바구니</button>
                </section>
                <!-- 상품 3 -->
                <section class="product">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTKTimxQ7LeDxuwCO8bw85Fcm2ZOjDEi88Us-GS_2uqXg&s" alt="흑청바지">
                    <h2>흑 청바지</h2>
                    <p>어디에나 매치할 수 있는 데일리 흑청바지입니다.</p>
                    <p class="price">가격: ₩35,000</p>
                    <button type="button" onclick="alert('구매가 완료되었습니다!');">구매하기</button>
                    <button type="button" onclick="addToCart('흑 청바지', '₩35,000')">장바구니</button>
                </section>
                <!-- 상품 4 -->
                <section class="product">
                    <img src="https://argen.kr/web/product/big/201709/532_shop1_991253.jpg" alt="액세서리">
                    <h2>목걸이</h2>
                    <p>가볍게 매치할 수 있는 은 목걸이로 포인트가 되기 좋습니다.</p>
                    <p class="price">가격: ₩15,000</p>
                    <button type="button" onclick="alert('구매가 완료되었습니다!');">구매하기</button>
                    <button type="button" onclick="addToCart('목걸이', '₩15,000')">장바구니</button>
                </section>
            </div>
        </main>
        <nav class="navbar">
            <span class="navbar_logo">Style 오늘</span>
            <ul class="navbar_menu">
                <li><a href="mainhome.html">홈</a></li>
                <li><a href="contact.html">문의 게시판</a></li>
                <li><a href="FAQs.html">FAQs</a></li>
                <li><a href="more.html">More</a></li>
            </ul>
            <ul class="navbar_cls">
                <li><a href="profile.html">Profile</a></li>
                <li><a href="settings.html">Settings</a></li>
            </ul>
            <!-- 모바일 메뉴 버튼 -->
            <a href="#" class="navbar_toogleBtn">☰</a>
        </nav>
    </div>
    <script>
        // 장바구니에 상품을 추가하는 함수
        function addToCart(productName, productPrice) {
            let cart = JSON.parse(localStorage.getItem('cart')) || [];
            cart.push({ name: productName, price: productPrice });
            localStorage.setItem('cart', JSON.stringify(cart));
            alert(productName + '이(가) 장바구니에 추가되었습니다!');
        }

        // 장바구니 페이지로 이동하는 함수
        document.getElementById('cart-icon').addEventListener('click', function() {
            window.location.href = 'cart.html';
        });

        // 마이페이지 버튼 기능
        document.getElementById('mypage-button').addEventListener('click', function() {
            if (localStorage.getItem('loggedIn') === 'true') {
                let username = localStorage.getItem('username');
                alert('로그인한 사용자: ' + username);
            } else {
                window.location.href = 'login.html';
            }
        });

        // 로그인 상태 확인
        window.onload = function() {
            if (localStorage.getItem('loggedIn') === 'true') {
                let username = localStorage.getItem('username');
                document.getElementById('mypage-button').innerText = '마이페이지 (' + username + ')';
            }
        };

        // 모바일 메뉴 토글 기능
        document.querySelector('.navbar_toogleBtn').addEventListener('click', () => {
            document.querySelector('.navbar_menu').classList.toggle('active');
            document.querySelector('.navbar_cls').classList.toggle('active');
        });
    </script>
</body>
</html>


//CSS코드

body, html {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
}

header {
    background-color: #f8f8f8;
    text-align: center;
    padding: 30px;
    position: relative;
    margin-left: 205px; /* 사이드바와 5px 간격 */
}

.header-buttons {
    position: absolute;
    right: 20px;
    top: 20px;
    display: flex;
    align-items: center;
}

.cart-icon {
    width: 40px;
    height: 40px;
    cursor: pointer;
    margin-right: 5px;
}

.login-button, .mypage-button {
    padding: 10px 20px;
    background-color: #000;
    color: #fff;
    border: none;
    cursor: pointer;
    margin-left: 5px;
}

.login-button:hover, .mypage-button:hover {
    background-color: #333;
}

main {
    padding: 20px;
    display: flex;
    justify-content: center;
    margin-left: 205px; /* 사이드바와 5px 간격 */
}

.products {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
    justify-items: center;
}

.product {
    text-align: center;
    border: 1px solid #ddd;
    padding: 20px;
    border-radius: 5px;
    width: 200px;
    height: 500px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}

.product img {
    width: 100%;
    height: auto;
}

.price {
    font-size: 20px;
    color: #333;
}

button {
    background-color: #000;
    color: #fff;
    border: none;
    padding: 10px 20px;
    cursor: pointer;
    margin: 5px;
}

button:hover {
    background-color: #333;
}

.navbar {
    position: fixed;
    bottom: 0;
    width: calc(100% - 205px); /* 사이드바와 5px 간격 */
    background-color: #000;
    color: white;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 8px 12px;
    z-index: 100;
    left: 205px;
}

.navbar_logo {
    font-size: 24px;
}

.navbar_menu, .navbar_cls {
    display: flex;
    list-style: none;
    padding: 0;
    margin: 0;
}

.navbar_menu li, .navbar_cls li {
    margin: 0 10px;
}

.navbar_menu li a, .navbar_cls li a {
    color: white;
    text-decoration: none;
}

.navbar_toogleBtn {
    display: none;
}

.sidebar {      
    position: fixed;
    left: 0;
    top: 0;
    width: 200px;
    height: 100%;
    background-color: rgb(61, 61, 61);
    padding: 10px;
    box-sizing: border-box;
    z-index: 101;
}

.sidebar .menu {
    list-style-type: none;
    padding: 0;
    margin: 0;
}

.sidebar .menu li {
    margin: 20px 0;
}

.sidebar .menu li a {
    color: white;
    text-decoration: none;
}

@media screen and (max-width: 768px) {
    .navbar_menu, .navbar_cls {
        display: none;
        flex-direction: column;
    }

    .navbar_menu.active, .navbar_cls.active {
        display: flex;
    }

    .navbar_toogleBtn {
        display: block;
        font-size: 24px;
    }
}

