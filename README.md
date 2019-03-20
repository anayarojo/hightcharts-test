## Highcharts

#### Ejemplo básico
```javascript
const properties = {
    chart: {
        type: 'line',
        renderTo: 'hight-chart-container'
    },
    title: {
        text: 'Hightchart Title'
    },
    xAxis: {
        title: {
            text: 'X Axis'
        }
    },
    yAxis: {
        allowDecimals: true,
        title: {
            text: 'Y Axis'
        }
    },
    series: [
        {
            name: 'Raul',
            data: [1, 2, 3, 4, 5]
        },
        {
            name: 'Sergio',
            data: [10, 15, 20, 25, 30]
        },
        {
            name: 'Francisco',
            data: [2, 4, 8, 16, 32]
        },
    ],
    tooltip: {
        formatter: function () {
            return `<b> ${(this.series.name || '')} </b><br/> 
                    ${this.point.y } ${(this.point.name || '').toLowerCase()}`;
        }
    }
};

const chart = Highcharts.chart(properties);
```

#### Documentación
https://www.highcharts.com/docs/
