# workAround-Explorer


**Explorador de WorkAround**

WorkAround es una organización de investigación que proporciona datos sobre las tendencias salariales en la industria tecnológica. Abra salaryData.js para ver los datos que han recopilado. Notará que también han creado algunas funciones para filtrar esos datos y obtener subconjuntos de datos por función y por empresa.

WorkAround ahora quiere lanzar una nueva aplicación web llamada WorkAround Explorer para que sus datos sean más fácilmente visibles. Esta aplicación web debería permitir a los usuarios elegir roles y empresas específicas en la industria de la tecnología para ver la siguiente información:

-El salario para el puesto elegido en la empresa elegida.

-El promedio de la industria para el rol elegido.

-El salario promedio de la empresa elegida en todos los roles.

-El salario promedio de la industria en todos los roles y todas las empresas.

**Renderice los botones de radio usando el módulo salarioData**
1 . Estas primeras cuatro tareas se centrarán en representar los <input>elementos utilizando los nombres de las empresas y los diferentes roles disponibles en los datos salariales recopilados.

Abra salaryData.js donde encontrará los datos recopilados en la variable salaryData. A continuación se muestran cuatro funciones para filtrar estos datos.

Necesitas:

-Exporte las cuatro funciones de salaryData.js utilizando la exportsintaxis denominada ES6 .

-Exporte la salaryDatamatriz como defaultexportación.


Abra main.js y eche un vistazo a la función renderInputButtons(). Esta función acepta una gran variedad de etiquetas que se utilizan para crear individuales de estilo de radio <input>elementos . La función también acepta una cadena que se utiliza como nombre para ese grupo de entrada.

Actualmente, esta función se llama dos veces con las variables companiesy rolescomo primeros argumentos. Sin embargo, a cada una de estas variables se le asignan matrices vacías.

En su lugar, utilizará las funciones getRoles()y getCompanies()de salaryData.js para inicializar estas variables.

Primero, en la parte superior de main.js , use la importsintaxis con nombre de ES6 para importar getRolesy getCompaniesdesde salaryData.js . Compruebe el sistema de archivos para determinar la ruta relativa desde main.js

Ahora, vuelva a colocar las matrices vacías asignadas a companies y roles con llamadas de función a getCompanies()y getRoles(), respectivamente.


Incluso si completó correctamente las tareas anteriores, los <input>elementos de estilo de radio aún no se procesarán. Esto se debe a que ahora debemos especificar que main.js está usando módulos.

En index.html , agregue un typeatributo <script src='main.js'>con el valor correcto para indicar que el script main.js está usando módulos.

Después de completar esta tarea, debería ver los <input>elementos de estilo de radio representados en su aplicación.
  
  
**Crear el workAroundModule**

¡Gran trabajo! Ahora tiene <input>elementos de estilo de radio para las diferentes empresas y roles representados en el conjunto de datos salariales. Intente seleccionar una combinación de empresa y función y verá que los datos no se están calculando. En cambio, los cuatro valores se muestran como $ 0.

Abra workAroundModule.js donde encontrará cuatro funciones, cada una de las cuales calcula un valor de datos diferente que queremos mostrar. Actualmente están incompletos.

Para completar estas cuatro funciones, necesitará algunos datos de salaryData.js .

-Importe las funciones getDataByRole()y getDataByCompany()desde salaryData.js utilizando una importsintaxis con nombre .
  
-Importe salaryDatadesde salaryData.js utilizando la importsintaxis predeterminada .
  
  Cada una de las funciones incompletas en workAroundModule.js contiene una matriz vacía ( []) que necesita ser reemplazada. Deberá usar los datos / funciones importados apropiados del módulo salaryData.js para reemplazar estas matrices.
  
  
Como paso final, para que estas funciones estén disponibles para main.js , exporte las cuatro funciones usando la export sintaxis nombrada .
  
  
**Calcule y renderice los datos cuando cambie la entrada del usuario**
  
Ahora todos estamos configurados para usar las funciones definidas en workAroundModule.js para calcular y representar los datos en función de las selecciones de entrada del usuario.

En main.js , importe las cuatro funciones de workAroundModule.js .
  
 Y finalmente, échale un vistazo updateResults(). Esta función se llama cada vez que el usuario selecciona uno de los elementos de entrada de radio.

En la parte superior de la definición de updateResults(), los companyy roleseleccionados por el usuario se extraen de los <input>elementos. Estos valores se pueden usar en combinación con las funciones importadas de workAroundModule.js para calcular las cuatro variables siguientes:

const averageSalaryByRole = 0;
const averageSalaryByCompany = 0;
const salary = 0;
const industryAverageSalary = 0;
Como puede ver, todos están asignados en 0lugar de los datos calculados correspondientes. Reemplace cada uno 0con una llamada a la función importada apropiada desde workAroundModule.js usando uno (o ambos) companyy rolecomo argumentos.
  
  
