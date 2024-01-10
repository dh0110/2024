<!DOCTYPE html>
<html>
<head>
    <title>My Page</title>
    <style>
        .center {
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: row;
            height: 60vh; /* height 값을 60vh로 조정 */
        }

        .team {
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            margin: 10px;
        }

        h1, input {
            margin: 10px;
            font-size: 84%;
        }

        .sub-title {
            text-align: center;
            font-size: 1.5em;
            margin-top: 50vh; /* 소제목 위치 조정 */
        }

        button {
            margin-top: 20px;
        }

        #data {
            margin-top: 20px;
            text-align: center;
            border: 1px solid black;
            padding: 10px;
        }
    </style>
</head>
<body>
    <h1 class="sub-title">장입수량</h1>

    <div class="center">
        <div class="team">
            <h1>품번</h1>
            <input id="productNumber" type="text" placeholder="텍스트와 숫자를 입력하세요">
        </div>
        <div class="team">
            <h1>쇼트</h1>
            <input id="short" type="number" placeholder="숫자를 입력하세요">
        </div>
        <div class="team">
            <h1>피막</h1>
            <input id="coating" type="number" placeholder="숫자를 입력하세요">
        </div>
        <button onclick="saveData()">저장</button>
    </div>

    <div id="data"></div>

    <script>
        function saveData() {
            var short = document.getElementById('short').value;
            var productNumber = document.getElementById('productNumber').value;
            var coating = document.getElementById('coating').value;

            var dataDiv = document.getElementById('data');
            dataDiv.innerHTML += '품번: ' + productNumber + ', 쇼트: ' + short + ', 피막: ' + coating + '<br>';
        }
    </script>

</body>
</html>
