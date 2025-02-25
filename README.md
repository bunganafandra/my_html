# my_html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SK Tim SAKIP 2024</title>
    <style>
        table {
            width: 100%;
            border-collapse: collapse;
        }
        th, td {
            border: 1px solid black;
            padding: 8px;
            text-align: left;
        }
        th {
            background-color: #f2f2f2;
        }
    </style>
</head>
<body>

    <h2>SK Tim SAKIP 2024 (Permindok 13)</h2>

    <table>
        <thead>
            <tr>
                <th>Kriteria/Subkriteria</th>
                <th>Jawaban Operator Evaluasi Kab/Kota</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>2.1.3.1 Terdapat SK Tim SAKIP</td>
                <td>
                    <select onchange="saveAnswer('2.1.3.1', this.value)">
                        <option value="Ya">Ya</option>
                        <option value="Tidak">Tidak</option>
                    </select>
                </td>
            </tr>
            <tr>
                <td>2.1.3.2 SK Tim SAKIP telah memuat nama dan kedudukan dalam Tim</td>
                <td>
                    <select onchange="saveAnswer('2.1.3.2', this.value)">
                        <option value="Ya">Ya</option>
                        <option value="Tidak">Tidak</option>
                    </select>
                </td>
            </tr>
            <tr>
                <td>2.1.3.3 SK Tim SAKIP telah mengakomodir perwakilan dari Tim Kerja Penanggungjawab IKU</td>
                <td>
                    <select onchange="saveAnswer('2.1.3.3', this.value)">
                        <option value="Ya">Ya</option>
                        <option value="Tidak">Tidak</option>
                    </select>
                </td>
            </tr>
            <tr>
                <td>2.1.3.4 SK Tim SAKIP telah memuat uraian tugas untuk tiap kedudukan dalam Tim</td>
                <td>
                    <select onchange="saveAnswer('2.1.3.4', this.value)">
                        <option value="Ya">Ya</option>
                        <option value="Tidak">Tidak</option>
                    </select>
                </td>
            </tr>
            <tr>
                <td>2.1.3.5 SK Tim SAKIP telah memuat tugas untuk melakukan monitoring target jangka menengah</td>
                <td>
                    <select onchange="saveAnswer('2.1.3.5', this.value)">
                        <option value="Ya">Ya</option>
                        <option value="Tidak">Tidak</option>
                    </select>
                </td>
            </tr>
            <tr>
                <td>2.1.3.6 SK Tim SAKIP telah memuat tugas untuk melakukan monitoring target triwulanan</td>
                <td>
                    <select onchange="saveAnswer('2.1.3.6', this.value)">
                        <option value="Ya">Ya</option>
                        <option value="Tidak">Tidak</option>
                    </select>
                </td>
            </tr>
        </tbody>
    </table>

    <script>
        // Fungsi untuk menyimpan jawaban ke localStorage
        function saveAnswer(key, value) {
            localStorage.setItem(key, value);
        }

        // Fungsi untuk memuat kembali jawaban yang tersimpan
        function loadAnswers() {
            document.querySelectorAll("select").forEach(select => {
                const key = select.getAttribute("onchange").match(/'(.+?)'/)[1];
                const savedValue = localStorage.getItem(key);
                if (savedValue) {
                    select.value = savedValue;
                }
            });
        }

        // Panggil fungsi saat halaman dimuat
        window.onload = loadAnswers;
    </script>

</body>
</html>
