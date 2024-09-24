1.
rails new mysite --database=postgresql -j esbuild --css bootstrap 
2.
npm install global yarn

3.
test:
  <<: *default
  database: mysite_test
  username: postgres
  password: olida
  port: 5432


production:
  <<: *default
  database: mysite_production
  username: postgres
  password: olida
  port: 5432



rails g controller Render


repositorio mysite


# The original asset pipeline for Rails [https://github.com/rails/sprockets-rails]
gem "sprockets-rails"


rails routes
root: render#index

git init
git add . 
git commit -m "first commit"





Paso 1:
Crear la aplicación con el nombre basic-form.
rails new basic-form --database=postgresql
● Paso 2:
Generamos un modelo llamado Post que tendrá los campos title y content.
rails g rails g model Post title content

Paso 3:
A continuación, vamos a crear la base de datos en nuestra aplicación y a correr
las migraciones.
rails db:create db:migrate
● Paso 4:
Vamos a generar un controlador llamado posts el cual tendrá las acciones y
vistas para index, create y new

Paso 5:
Posteriormente, vamos a generar un formulario HTML con el builder
form_with. Este formulario estará vinculado al modelo Post para que al ser
llenado ingrese información a la base de datos.
Este formulario lo vamos a incorporar en la vista new.html.erb que se generó al
momento de crear el controlador.





1. rails new modelos_rails --database=postgresql
2. rails g model user name
3. /* Correr las migraciones */
4. rails db:create.
5. rails db:migrate.

6. rails g migration addColumnToModel column:datatype

7. rails g migration addAgeToUser age:integer
8. rails db:migrate.
rails db:rollback
rails db:migrate:status

rubygems.org

<%= form_with model: @post, method: :post do |form| %> <div> <%= form.label :title, "Post Title" %> <%= form.text_field :title %> </div> <div> <%= form.label :content, "Post Content" %> <%= form.text_field :content %> </div> <div> <%= form.submit %> </div><% end %>

Paso 1:
Generar una aplicación llamada faker_app con postgresql como motor de
base de datos y ejecutar el comando para crear la base de datos.
● Paso 2:
Generar un modelo llamado Beer con los campos brand, name y
alcoholic_grade: rails g model Beer brand name alcoholic_grade
Analicemos a continuación la sintaxis de importación de gemas en profundidad.

Paso 3:
Agregar la gema faker al final del Gemfile con la versión fijada
gem 'faker', '~> 2.23'
Otra forma de fijar una versión es indicarla sin el operador de especificación.
gem 'faker', '2.23'

Paso 4:
Una vez agregada la gema debemos correr el comando bundle install para que
se instale en la aplicación.
● Paso 5:
Ahora, vamos a configurar el seed para incorporar los datos de prueba de
ofrece la gema faker. Para ello utilizaremos su documentación oficial en Github
específicamente el generador de datos para Beer.
Veamos el código del seed a continuación:


20.times do |i|
   Beer.create(brand: Faker::Beer.brand, name: Faker::Beer.name,alcoholic_grade: Faker::Beer.alcohol)
end


Al ingresar al rails console
podremos verificar si los datos se crearon.
● Accedemos con rails c.
● Escribimos Beer.all.
● Esto despliega los registros que se hayan incorporado a través del seed.


Para este ejercicio deberás continuar con el desarrollo anterior. En esta ocasión
deberás realizar las siguientes acciones:
1. Generar una migración para modificar la base de datos y agregar un campo
llamado yeast_type para conocer el tipo de malta de la cerveza.
2. yeast_type al ser un nuevo campo agregado debe incorporarse corriendo la
migración.
3. Generar los datos para yeast_type con la gema faker usando su
documentación para Beers.
Tip: Para correr el seed utiliza rails db:drop db:create db:migrate db:seed.


