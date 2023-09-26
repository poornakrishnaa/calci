

    <script>
        function appendNumber(number) {
            document.forms["form1"]["answer"].value += number;
        }

        function appendOperator(operator) {
            document.forms["form1"]["answer"].value += operator;
        }

        function appendDecimal() {
            const currentValue = document.forms["form1"]["answer"].value;
            if (!currentValue.includes('.')) {
                document.forms["form1"]["answer"].value += '.';
            }
        }

        function calculate() {
            const expression = document.forms["form1"]["answer"].value;
            try {
                const result = eval(expression);
                document.forms["form1"]["answer"].value = result;
            } catch (error) {
                document.forms["form1"]["answer"].value = 'Error';
            }
        }

        function clearDisplay() {
            document.forms["form1"]["answer"].value = '';
        }

        function backSpace() {
            const currentValue = document.forms["form1"]["answer"].value;
            document.forms["form1"]["answer"].value = currentValue.slice(0, -1);
        }
    </script>
</body>
</html>
