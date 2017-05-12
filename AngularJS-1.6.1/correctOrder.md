The correct order for library files to load when using Angular

********************************** Javascript Files **********************************

If using jQuery, it must load before AngularJS
    <script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>

If using Bootstrap JS (3.3.7 latest stable version), it must load before AngularJS, but after jQuery - note: jQuery minimum version is 1.9.0
    <script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/4.0.0-alpha.6/js/bootstrap.min.js"></script>

Recommended order for Angular Libraries
    angularFiles['angularModules']['ngAnimate'],
    angularFiles['angularModules']['ngMessageFormat'],
    angularFiles['angularModules']['ngMessages'],
    angularFiles['angularModules']['ngCookies'],
    angularFiles['angularModules']['ngResource'],
    angularFiles['angularModules']['ngRoute'],
    angularFiles['angularModules']['ngSanitize'],
    angularFiles['angularModules']['ngMock'],
    angularFiles['angularModules']['ngTouch'],
    angularFiles['angularModules']['ngAria']

    <script src="https://cdnjs.cloudflare.com/ajax/libs/angular.js/1.6.1/angular.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/angular.js/1.6.1/angular-animate.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/angular.js/1.6.1/angular-messages.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/angular.js/1.6.1/angular-cookies.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/angular.js/1.6.1/angular-resource.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/angular.js/1.6.1/angular-route.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/angular.js/1.6.1/angular-sanitize.min.js"></script>   
    <script src="https://cdnjs.cloudflare.com/ajax/libs/angular.js/1.6.1/angular-mocks.js"></script>   
    <script src="https://cdnjs.cloudflare.com/ajax/libs/angular.js/1.6.1/angular-touch.js"></script>   
    <script src="https://cdnjs.cloudflare.com/ajax/libs/angular.js/1.6.1/angular-aria.min.js"></script>   


Then, load your internal scripts
    services.js
    controllers.js
    filters.js
    directives.js

Finally, the app.js files
    <script src="js/app.js"></script>
