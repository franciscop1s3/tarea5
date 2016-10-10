#RecyclerView

Para usar Recyclerview-v7 recordar que hay que agregar la libreria mediante gradlecom.android.support:recyclerview-v7:+ es recomendable sustituir el smbolo + por el numero especifico de version.
Sabemos que un RecyclerView es una clase que hereda de ViewGroup, que al igual queListView y GridView nos va permitir mostrar grandes colecciones o conjuntos de datos con la unica diferencia que solo se dedica a reciclar vistas delegando la tarea de renderizado a otros componentes que seran los que determinen la forma de acceder a los datos y como mostrarlos.
LayoutManager
Es una clase estetica abstracta que se encuentra dentro de la clase RecyclerView su tarea es definir el orden en que se mostraran nuestras vistas de elementos y determinar la poltica de cuando reciclar las vistas que ya no son visibles para el usuario.
Filosofia
Ha dejado de ser una patron por extension recordar que las clases ListView y GridView heredan de la clase abstracta AbsListView (que a su vez esta hereda de la clase abstractaAdapterView la cual hereda de ViewGroup.) quien es la encargada de virtualizar una lista de elementos y delegar a sus subclases la decision de como mostrar sus elementos, por esta razon un ListView es quien decide que los elementos deben ser mostrados de forma lineal y en forma de cuadricula en el caso de GridView.
RecyclerView necesita del metodo setLayoutManager(LayoutManager layout) para asiganar un tipo de layout que le indique como debe renderizar, dando origen a un patron por composicion.
Es sensato mencionar que con la llegada de RecyclerView y la forma en que fue disenada su implementacion se cumple un Design Principle Favor composition over inheritance. el cual tiene como objetivo dar flexibilidad.
Tipos de LayoutManager
Existen tres implementaciones diferentes de LayoutManager que vienen incluidos dentro de la librera Recyclerview-v7 LinearLayoutManager, GridLayoutManager yStaggeredGridLayoutManager, tienen la habilidad de facilitar el uso de RecyclerView indicando la forma en que los elementos deben ser mostrados.

