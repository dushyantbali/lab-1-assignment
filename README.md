# lab-1-assignment
# This is my lab 1 assignment for the course web development 2
<html>
<head>
    <style>
        table {
            border-collapse: collapse;
            width: 200px;
            margin: 20px 0;
            border: 1px solid black;
        }
        td {
            border: 1px solid black;
            padding: 10px;
            text-align: center;
            font-weight: bold;
        }
        .buttons {
            margin-top: 20px;
        }
        .buttons button {
            padding: 10px 20px;
            margin: 5px;
        }
        .message {
            margin-top: 20px;
        }
    </style>
</head>
<body data-new-gr-c-s-check-loaded="14.1193.0" data-gr-ext-installed="" style="">
    <table id="myTable">
        <tr>
            <td>Row1 Col1</td>
            <td>Row1 Col2</td>
        </tr>
        <tr>
            <td>Row2 Col1</td>
            <td>Row2 Col2</td>
        </tr>
        <tr>
            <td>Row3 Col1</td>
            <td>Row3 Col2</td>
        </tr>
        <tr>
            <td>Row4 Col1</td>
            <td>Row4 Col2</td>
        </tr>
        <tr>
            <td>Row5 Col1</td>
            <td>Row5 Col2</td>
        </tr>
        <tr>
            <td>Row6 Col1</td>
            <td>Row6 Col2</td>
        </tr>
    </table>
    <div class="buttons">
        <button onclick="insertRow()">Insert row</button>
        <button onclick="deleteRow()">delete row</button>
    </div>
    <div class="message" id="message">Message:</div>

    <script>
        function insertRow() {
            var table = document.getElementById("myTable");
            var rowCount = table.rows.length;
            var row = table.insertRow(rowCount);
            var cell1 = row.insertCell(0);
            var cell2 = row.insertCell(1);
            cell1.innerHTML = "Row" + (rowCount + 1) + " Col1";
            cell2.innerHTML = "Row" + (rowCount + 1) + " Col2";
            document.getElementById("message").innerHTML = "Message:";
        }

        function deleteRow() {
            var table = document.getElementById("myTable");
            var rowCount = table.rows.length;
            if (rowCount > 0) {
                table.deleteRow(0);
                if (rowCount - 1 === 0) {
                    document.getElementById("message").innerHTML = "Message: No more rows to delete";
                }
            }
        }
    </script>
</body>
</html>
