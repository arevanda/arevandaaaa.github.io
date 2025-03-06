<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kalkulator Sederhana</title>
    <style>
        table {
            border: 3px solid rgb(0, 0, 0);
            margin: 50px auto;
            text-align: center;
            background: #faf7f7;
            padding: 15px;
        }
        td {
            padding: 22px;
            border: 3px solid rgb(23, 23, 24);
            width: 50px;
            text-align: center;
        }
        input {
            width: 100%;
            text-align: right;
            padding: 5px;
            margin-bottom: 5px;
        }
        td:hover {
            background: #d7d7d5;
        }
        .operator {
            background: #d36c05;
            color: white;
        }
    </style>
</head>
<body>
<table>
    <tr>
        <td colspan="4">
            <input type="text" id="layar" disabled>
        </td>
    </tr>
    <tr>
        <td class="operator" onclick="operator('+')">+</td>
        <td class="operator" onclick="operator('-')">-</td>
        <td class="operator" onclick="operator(':')">:</td>
        <td class="operator" onclick="operator('*')">*</td>
    </tr>
    <tr>
        <td onclick="tambahLayar('7')">7</td>
        <td onclick="tambahLayar('8')">8</td>
        <td onclick="tambahLayar('9')">9</td>
        <td rowspan="4" class="operator" onclick="hitung()">=</td>
    </tr>
    <tr>
        <td onclick="tambahLayar('4')">4</td>
        <td onclick="tambahLayar('5')">5</td>
        <td onclick="tambahLayar('6')">6</td>
    </tr>
    <tr>
        <td onclick="tambahLayar('1')">1</td>
        <td onclick="tambahLayar('2')">2</td>
        <td onclick="tambahLayar('3')">3</td>
    </tr>
    <tr>
        <td onclick="tambahLayar('0')">0</td>
        <td class="tambahLayar" onclick="operator('.')">.</td>
        <td class="operator" onclick="hapusLayar()">C</td>
    </tr>
</table>
<script>
    function tambahLayar(nilai) {
        document.getElementById("layar").value += nilai;
    }
    function operator(nilai) {
        document.getElementById("layar").value += nilai;
    }
    function hitung() {
       
            let hasil = eval(document.getElementById("layar").value.replace(':', '/'));
            document.getElementById("layar").value = hasil;
        
        }


    function hapusLayar() {
        document.getElementById("layar").value = "";
    }
</script>
</body>
</html>
