Primer encabezado | Segundo encabezado
--- | ---
Celda de contenido | Celda de contenido
Celda de contenido | Celda de contenido

Primer encabezado | Segundo encabezado
--- | ---
Celda de contenido | Celda de contenido
Celda de contenido | Celda de contenido

![Ciudadela](https://vignette.wikia.nocookie.net/masseffect/images/d/d7/MassEffect2Citadel.jpg/revision/latest?cb=20100721191415)

Alineado a la izquierda | Centro alineado | Alineado a la derecha
:-- | :-: | --:
la columna 3 es | algún texto prolijo | **$1600**
la columna 2 es | centrado | $12
rayas de cebra | son limpios | ~~$1~~

Dillinger es un editor HTML5 Markdown con tecnología AngularJS, habilitado para la nube, listo para dispositivos móviles y con almacenamiento fuera de línea. (овнер)

- Escribe algo de Markdown a la izquierda (овнер)
- Ver HTML a la derecha
- magia

# verdadero

- Import a HTML file and watch it magically convert to Markdown
- Drag and drop images (requires your Dropbox account be linked)

Tú también puedes:

- Importe y guarde archivos desde GitHub, Dropbox, Google Drive y One Drive
- Arrastre y suelte archivos HTML y de rebajas en Dillinger
- Exportar documentos como Markdown, HTML y PDF

Markdown es un lenguaje de marcado ligero basado en las convenciones de formato que la gente utiliza naturalmente en el correo electrónico. Como escribe [John Gruber] en el [sitio de Markdown][df1]

> El objetivo primordial del diseño de la sintaxis de formato de Markdown es hacerla lo más legible posible. La idea es que un documento con formato Markdown se pueda publicar tal cual, como texto sin formato, sin que parezca que ha sido marcado con etiquetas o instrucciones de formato.

¡Este texto que ves aquí *en realidad* está escrito en Markdown! Para tener una idea de la sintaxis de Markdown, escriba algo de texto en la ventana izquierda y observe los resultados en la derecha.

### FALSO (мод2)

Dillinger utiliza varios proyectos de código abierto para funcionar correctamente: (мод2)

- [AngularJS] - ¡HTML mejorado para aplicaciones web!
- [Ace Editor] - impresionante editor de texto basado en web
- [markdown-it] - Analizador de Markdown bien hecho. Rápido y fácil de ampliar.
- [Twitter Bootstrap]: excelente plantilla de interfaz de usuario para aplicaciones web modernas
- [node.js] - E/S con eventos para el backend
- [Express] - marco rápido de aplicación de red node.js [@tjholowaychuk]
- [Gulp] - el sistema de compilación de streaming
- [Breakdance](https://breakdance.github.io/breakdance/) - Conversor de HTML a Markdown
- [jQuery] - claro

Y, por supuesto, Dillinger es de código abierto con un [repositorio público][eneldo] en GitHub.

### Instalación

![ilos](https://lh3.googleusercontent.com/proxy/DDV8a7sLIWurhJtW8Ego9bq-JlwpfFFoR0tkLJQKKYXEXoWHB6ZUP5jGKD2VcYt3z1QVsgcn6L3GoU1ns8m9fvi3U51GzddA70ZUMHgzHvjl4-i7YOJY9cShBPrfjUhMQhxaJ97WFBp612XmjMXVGypfGkiBarN4PWxhiHkiYYNW7HGbtTpOcyt9GQ4Q23C2noxLTWFXZMcQZhRpQA_qzu2n6_H6CPViBnhSHpEl4JZAPaGCSJqgZg)

Dillinger requiere [Node.js](https://nodejs.org/) v4+ para ejecutarse.

Instale las dependencias y devDependencies e inicie el servidor.

```sh
$ cd dillinger
$ npm install -d
$ node app
```

Para entornos de producción...

```sh
$ npm install --production
$ NODE_ENV=production node app
```

### Complementos

Dillinger actualmente está ampliado con los siguientes complementos. Las instrucciones sobre cómo usarlos en su propia aplicación están vinculadas a continuación.

Enchufar | LÉAME
--- | ---
buzón | [complementos/dropbox/README.md][PlDb]
GitHub | [plugins/github/README.md][PlGh]
Google Drive | [plugins/googledrive/README.md][PlGd]
OneDrive | [complementos/onedrive/README.md][PlOd]
Medio | [plugins/medium/README.md][PlMe]
Google analitico | [plugins/googleanalytics/README.md][PlGa]

### Desarrollo

¿Quieres contribuir? ¡Excelente!

Dillinger utiliza Gulp + Webpack para un desarrollo rápido. ¡Haga un cambio en su archivo y vea instantáneamente sus actualizaciones!

Abra su Terminal favorita y ejecute estos comandos.

Primera pestaña:

```sh
$ node app
```

Segunda pestaña:

```sh
$ gulp watch
```

(opcional) Tercero:

```sh
$ karma test
```

#### Construyendo para fuente

Para lanzamiento de producción:

```sh
$ gulp build --prod
```

Generando archivos zip prediseñados para su distribución:

```sh
$ gulp build dist --prod
```

### Estibador

Dillinger es muy fácil de instalar e implementar en un contenedor Docker.

De forma predeterminada, Docker expondrá el puerto 8080, así que cámbielo dentro del Dockerfile si es necesario. Cuando esté listo, simplemente use Dockerfile para crear la imagen.

```sh
cd dillinger
docker build -t joemccann/dillinger:${package.json.version} .
```

Esto creará la imagen de Dillinger e incorporará las dependencias necesarias. Asegúrese de cambiar `${package.json.version}` por la versión real de Dillinger.

Una vez hecho esto, ejecute la imagen de Docker y asigne el puerto a lo que desee en su host. En este ejemplo, simplemente asignamos el puerto 8000 del host al puerto 8080 de Docker (o cualquier puerto expuesto en el Dockerfile):

```sh
docker run -d -p 8000:8080 --restart="always" <youruser>/dillinger:${package.json.version}
```

Verifique la implementación navegando a la dirección de su servidor en su navegador preferido.

```sh
127.0.0.1:8000
```

#### Kubernetes + Google Cloud

Ver [KUBERNETES.md](https://github.com/joemccann/dillinger/blob/master/KUBERNETES.md)

### Todos
