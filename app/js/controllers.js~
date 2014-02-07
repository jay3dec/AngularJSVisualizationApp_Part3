'use strict';

/* Controllers */
google.load('visualization', '1', {packages:['corechart']});
google.setOnLoadCallback(function () {
    angular.bootstrap(document.body, ['myApp']);
});
angular.module('myApp.controllers', []).
  controller('MyCtrl1', ['$scope',function($scope) {
	var data = google.visualization.arrayToDataTable([
          ['Year', 'Sales', 'Expenses'],
          ['2004',  1000,      400],
          ['2005',  1170,      460],
          ['2006',  660,       1120],
          ['2007',  1030,      540]
        ]);
	var options = {
          title: 'Company Performance'
        };
        var chart = {};
        chart.data = data;
        chart.options = options;

	$scope.chartTypes = [
            { typeName: 'LineChart', typeValue: '1' },
            { typeName: 'BarChart', typeValue: '2' },
            { typeName: 'ColumnChart', typeValue: '3' },
            { typeName: 'PieChart', typeValue: '4' }
            ];
	$scope.selectType = function (type) {
        	$scope.chart.type = type.typeValue;
    	}
        chart.type = $scope.chartTypes[0].typeValue;
        $scope.chartType = $scope.chartTypes[0];
	
        $scope.chart = chart;
        
        
  }])
  .controller('MyCtrl2', [function() {

  }]);

