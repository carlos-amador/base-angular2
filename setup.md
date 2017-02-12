
Project Setup 

1 -
    followed steps on https://angular.io/docs/ts/latest/guide/webpack.html - 2/12/2017

2 - 
    webpack compile errors fix - in webpack.common.js changed - 2/12/2017
      
     from

        {
            test: /\.ts$/,
            loaders: [{
            loader: 'awesome-typescript-loader',
            options: { configFileName: helpers.root('src', 'tsconfig.json') }
            } , 'angular2-template-loader']
        },

      to 

        {
            test: /\.ts$/,
            loaders: [ 'awesome-typescript-loader', 'angular2-template-loader']
        },
      
 3 - 
     webpack compile errors fix - in app.component.html changed - 2/12/2017
    
     from

        <main>
        <h1>Hello from Angular App with Webpack</h1>
        <img src="../../public/images/angular.png">
        </main>

     to 

        <main>
        <h1>Hello from Angular App with Webpack</h1>
        </main>


4 -
    webpack compile errors fix - update typescript from 2.0.10 to 2.1.6 - 2/12/2017


4 -
    removed "~" and "^" from package dependencies version number listed in package.json, to eliminate inadverdent updates when applying
    npm install command 
