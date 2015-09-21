# angularjs
My Angularjs test codes

app.controller('MainController', function($scope) {
  $scope.mcMsg = 'MainController';
});

app.controller('PhoneListController', function($scope, $http) {
  $http.get('phones.json').success(function(data) {
    $scope.phones = data;
  });
  $scope.plMsg = "PhoneListController";
  $scope.orderProp = 'age';
});
