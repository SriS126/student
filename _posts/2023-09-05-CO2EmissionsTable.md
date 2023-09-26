---
toc: true
comments: false
layout: post
title: CO2 Emissions Table
description: Find the CO2 Emissions from each year!
type: hacks
courses: { compsci: {week: 3} }
---
<html>
<head>
    <title>CO2 Emissions Table</title>
</head>
<body>
    <h1>CO2 Emissions Table</h1>
    <input type="text" id="searchInput" placeholder="Search for a place">
    <table id="emissionsTable">
        <thead>
            <tr>
                <th>CO2 Emissions (billion metric tons)</th>
                <th>Year</th>
                <th>Place</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>6.0</td>
                <td>2000</td>
                <td>United States</td>
            </tr>
            <tr>
                <td>4.5</td>
                <td>2001</td>
                <td>United States</td>
            </tr>
            <tr>
                <td>5.0</td>
                <td>2002</td>
                <td>United States</td>
            </tr>
            <tr>
                <td>5.2</td>
                <td>2003</td>
                <td>United States</td>
            </tr>
            <tr>
                <td>5.4</td>
                <td>2004</td>
                <td>United States</td>
            </tr>
            <tr>
                <td>5.6</td>
                <td>2005</td>
                <td>United States</td>
            </tr>
            <tr>
                <td>5.8</td>
                <td>2006</td>
                <td>United States</td>
            </tr>
            <tr>
                <td>6.0</td>
                <td>2007</td>
                <td>United States</td>
            </tr>
            <tr>
                <td>6.2</td>
                <td>2008</td>
                <td>United States</td>
            </tr>
            <tr>
                <td>6.0</td>
                <td>2009</td>
                <td>United States</td>
            </tr>
            <tr>
                <td>5.8</td>
                <td>2010</td>
                <td>United States</td>
            </tr>
            <tr>
                <td>5.7</td>
                <td>2011</td>
                <td>United States</td>
            </tr>
            <tr>
                <td>5.5</td>
                <td>2012</td>
                <td>United States</td>
            </tr>
            <tr>
                <td>5.4</td>
                <td>2013</td>
                <td>United States</td>
            </tr>
            <tr>
                <td>5.3</td>
                <td>2014</td>
                <td>United States</td>
            </tr>
            <tr>
                <td>5.2</td>
                <td>2015</td>
                <td>United States</td>
            </tr>
            <tr>
                <td>5.1</td>
                <td>2016</td>
                <td>United States</td>
            </tr>
            <tr>
                <td>5.0</td>
                <td>2017</td>
                <td>United States</td>
            </tr>
            <tr>
                <td>4.9</td>
                <td>2018</td>
                <td>United States</td>
            </tr>
            <tr>
                <td>4.8</td>
                <td>2019</td>
                <td>United States</td>
            </tr>
            <tr>
                <td>4.7</td>
                <td>2020</td>
                <td>United States</td>
            </tr>
            <tr>
                <td>4.6</td>
                <td>2021</td>
                <td>United States</td>
            </tr>
            <tr>
                <td>4.5</td>
                <td>2022</td>
                <td>United States</td>
            </tr>
            <!-- Add more rows as needed -->
        </tbody>
    </table>

    <script>
        // Function to filter the table based on user input
        document.getElementById("searchInput").addEventListener("keyup", function () {
            var input = this.value.toLowerCase();
            var table = document.getElementById("emissionsTable");
            var rows = table.getElementsByTagName("tr");

            // Loop through all table rows and hide those that don't match the search input
            for (var i = 1; i < rows.length; i++) { // Start at 1 to skip the table header row
                var row = rows[i];
                var cells = row.getElementsByTagName("td");
                var match = false;

                for (var j = 0; j < cells.length; j++) {
                    var cell = cells[j];
                    if (cell.innerHTML.toLowerCase().indexOf(input) > -1) {
                        match = true;
                        break;
                    }
                }

                if (match) {
                    row.style.display = "";
                } else {
                    row.style.display = "none";
                }
            }
        });
    </script>
</body>
</html>