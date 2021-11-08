# Tarea #8

## Autor
1. Luis German Henao Ortiz

## Ejercicio #1


```jsx
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <div id="root">
    </div>
    <script src="https://unpkg.com/react@16/umd/react.development.js"></script>
    <script src="https://unpkg.com/react-dom@16/umd/react-dom.development.js"></script>
    <script src="https://unpkg.com/babel-standalone@6/babel.min.js"></script>
    <script type="text/babel">

const dato = {
  title_1: "Plato de la semana",
  title_2: "Berenjenas fritas",
  paragraph_1: "Comensales: 4 personas",
  paragraph_2: "Tiempo de preparacion: 10 minutos",
  paragraph_3: "Tiempo de cocción: 12 minutos",
  title_list_1: "Ingredientes:",
  title_list_2: "Preparacion:",
  list_1: ["4 Berenjenas ", "Sal ", "Pimienta ", "4 cucharas de harina y aceite "],
  list_2: ["Lavar las Berenjenas ",
           "Cortarlas en rodajas ",
           "Espolvorearlas con sal ",
           "Dejar que suelten el agua durante 30 minutos ",
           "Enharizarlas, ponerlas a freir durante 5 minutos en aceite bien caliente "],
}

const title_one = <h1>{dato.title_1}</h1>;
const subtitle = <h2>{dato.title_2}</h2>;
const paragraph_one = <p>{dato.paragraph_1}</p>;
const paragraph_two = <p>{dato.paragraph_2}</p>;
const paragraph_three = <p>{dato.paragraph_3}</p>;
const title_list_one = <p>{dato.title_list_1}</p>;
const title_list_two = <p>{dato.title_list_2}</p>;

const list_one = <p>{dato.list_1[0]}</p>;
const list_one1 = <p>{dato.list_1[1]}</p>;
const list_one2 = <p>{dato.list_1[2]}</p>;
const list_one3 = <p>{dato.list_1[3]}</p>;

const list_two = <p>{dato.list_2[0]}</p>;
const list_two1 = <p>{dato.list_2[1]}</p>;
const list_two2 = <p>{dato.list_2[2]}</p>;
const list_two3 = <p>{dato.list_2[3]}</p>;
const list_two4 = <p>{dato.list_2[4]}</p>;

const element = (
  <div>
    {title_one}
    {subtitle}
    {paragraph_one}
    {paragraph_two}
    {paragraph_three}
    <br/>
    <strong>{title_list_one}</strong>
    {list_one}
    {list_one1}
    {list_one2}
    {list_one3}
    <br/><br/>
    <strong>{title_list_two}</strong>
    {list_two}
    {list_two1}
    {list_two2}
    {list_two3}
    {list_two4}
  </div>
);

ReactDOM.render(
  element,
  document.getElementById('root')
);
    </script>
  </body>
</html>
```

## Ejercicio #2

```jsx
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <div id="root">
    </div>
    <script src="https://unpkg.com/react@16/umd/react.development.js"></script>
    <script src="https://unpkg.com/react-dom@16/umd/react-dom.development.js"></script>
    <script src="https://unpkg.com/babel-standalone@6/babel.min.js"></script>
    <script type="text/babel">

const dato = {
  title_1: "Página oficial de Juan Tuesta",
  title_2: "Enlaces Favoritos:",
  paragraph_1: ["Bienvenido a mi página personal. Soy un alumno de la universidad de Deusto",
                " y esta es mi página inicial, con la lista de mis enlaces favoritos y otra información de interés."],
  paragraph_2: "Juan Tuesta, Universidad de Deusto, Marzo 2002.",
  list_1: ["Internet", "Google", "Aldea global", "Manual de HTML"],
}

const title_one = <h1>{dato.title_1}</h1>;
const subtitle = <h2>{dato.title_2}</h2>;
const paragraph_one = <p>{dato.paragraph_1}</p>;
const paragraph_two = <p>{dato.paragraph_2}</p>;
const list_one = <p>{dato.list_1.map((datos) => <li>{datos}</li>)}</p>;

const element = (
  <div>
    <strong>{title_one}</strong>
    {paragraph_one}
    <strong>{subtitle}</strong>
    <ol>{list_one}</ol>
    {paragraph_two}
  </div>
);

ReactDOM.render(
  element,
  document.getElementById('root')
);
    </script>
  </body>
</html>
```

## Ejercicio #3

```jsx
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <div id="root">
    </div>
    <style>
    a{
    color: blue;
    }
    </style>
    <script src="https://unpkg.com/react@16/umd/react.development.js"></script>
    <script src="https://unpkg.com/react-dom@16/umd/react-dom.development.js"></script>
    <script src="https://unpkg.com/babel-standalone@6/babel.min.js"></script>
    <script type="text/babel">

const dato = {
  title_1: "Página oficial de Juan Tuesta",
  title_2: "Enlaces Favoritos:",
  paragraph_1: ["Bienvenido a mi página personal. Soy un alumno de la universidad de Deusto",
                " y esta es mi página inicial, con la lista de mis enlaces favoritos y otra información de interés."],
  paragraph_2: "Juan Tuesta, Universidad de Deusto, Marzo 2002.",
  list_1: ["Internet", <a href="https://www.google.com/">"Google"</a>, "Aldea global", <a href="https://desarrolloweb.com/manuales/manual-html.html">"Manual de HTML"</a>],
}

const title_one = <h1>{dato.title_1}</h1>;
const subtitle = <h2>{dato.title_2}</h2>;
const paragraph_one = <p>{dato.paragraph_1}</p>;
const paragraph_two = <p>{dato.paragraph_2}</p>;
const list_one = <p>{dato.list_1.map((datos) => <li>{datos}</li>)}</p>;

const element = (
  <div>
    <strong>{title_one}</strong>
    {paragraph_one}
    <strong>{subtitle}</strong>
    <ol>{list_one}</ol>
    {paragraph_two}
  </div>
);

ReactDOM.render(
  element,
  document.getElementById('root')
);
    </script>
  </body>
</html>
```

## Ejercicio #4

```jsx
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <div id="root">
    </div>
    <script src="https://unpkg.com/react@16/umd/react.development.js"></script>
    <script src="https://unpkg.com/react-dom@16/umd/react-dom.development.js"></script>
    <script src="https://unpkg.com/babel-standalone@6/babel.min.js"></script>
    <script type="text/babel">

const dato = {
  title_1: "Página oficial de Juan Tuesta",
  title_2: "Enlaces Favoritos:",
  paragraph_1: ["Bienvenido a mi página personal. Soy un alumno de la universidad de Deusto",
                " y esta es mi página inicial, con la lista de mis enlaces favoritos y otra información de interés."],
  paragraph_2: "Juan Tuesta, Universidad de Deusto, Marzo 2002.",
  list_1: ["Páginas Personales", "Paginas de referencia", "Portales", "Medios de comunicación"],
  list_2: ["Charkes F. Golfarb", "Lou Burnard", "Tim Berners-Lee"],
}

const title_one = <h1>{dato.title_1}</h1>;
const subtitle = <h2>{dato.title_2}</h2>;
const paragraph_one = <p>{dato.paragraph_1}</p>;
const paragraph_two = <p>{dato.paragraph_2}</p>;
const list_one = <p><dt>{dato.list_1[0]}</dt></p>;
const list_one1 = <p><dt>{dato.list_1[1]}</dt></p>;
const list_one2 = <p><dt>{dato.list_1[2]}</dt></p>;
const list_one3 = <p><dt>{dato.list_1[3]}</dt></p>;
const list_two = <p>{dato.list_2.map((dat) => <li key={dat.toString()}><dd>{dat}</dd></li>)}</p>;


const element = (
  <div>
    <strong>{title_one}</strong>
    {paragraph_one}
    <strong>{subtitle}</strong>
    <ol><dl>
      <li class="num">{list_one}</li>
      <ul>{list_two}</ul>
      <li class="num">{list_one1}</li>
      <li class="num">{list_one2}</li>
      <li class="num">{list_one3}</li>
    </dl></ol>
    {paragraph_two}
  </div>
);

ReactDOM.render(
  element,
  document.getElementById('root')
);
    </script>
  </body>
</html>
```


## Ejercicio #5

```jsx
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <div id="root">
    </div>
    <style>
    a{
      color: blue;
    }

    .divn{
      background-color: black;
      padding: 2px;
    }
    </style>
    <script src="https://unpkg.com/react@16/umd/react.development.js"></script>
    <script src="https://unpkg.com/react-dom@16/umd/react-dom.development.js"></script>
    <script src="https://unpkg.com/babel-standalone@6/babel.min.js"></script>
    <script type="text/babel">

const dato = {
  title_1: "Página oficial de Juan Tuesta",
  title_2: "Enlaces favoritos:",
  title_3: "Páginas Personales:",
  title_4: "Páginas de referencia:",
  title_5: "Portales",
  title_6: "Publicaciones",
  paragraph_1: ["Bienvenido a mi página personal. Soy un alumno de la universidad de Deusto",
                " y esta es mi página inicial, con la lista de mis enlaces favoritos y otra información de interés."],
  paragraph_2: "Juan Tuesta, Universidad de Deusto, Marzo 2002.",
  list_1: [<a href="#t3">Páginas Personales</a>, <a href="#t4">Paginas de referencia</a>, <a href="#t5">Portales</a>, <a href="#t6">Publicaciones</a>],
  list_2: ["Charkes F. Golfarb", "Lou Burnard", "Tim Berners-Lee"],
  list_3: ["Documentalistas", "Historiadores", "Linguistas", "Traductores"],
  list_4: ["Bibliotecas universitarias", "Centros de documentación", "Museos de arte contemporáneo", "Medios de comunicación"],
  list_5: ["Inicia", "Telépolis", "Ciudades", "Terra"],
  list_6: ["Ciberp@is", "Diario tecnologías de la información", "The standart", "Infoworld", "Wired"],
}

const title_one = <h1>{dato.title_1}</h1>;
const title_two = <h2>{dato.title_2}</h2>;
const title_three = <h2>{dato.title_3}</h2>;
const title_four = <h2>{dato.title_4}</h2>;
const title_five = <h2>{dato.title_5}</h2>;
const title_six = <h2>{dato.title_6}</h2>;
const paragraph_one = <p>{dato.paragraph_1}</p>;
const paragraph_two = <p>{dato.paragraph_2}</p>;
const list_one = <p><dt>{dato.list_3[0]}</dt></p>;
const list_one1 = <p><dt>{dato.list_3[1]}</dt></p>;
const list_one2 = <p><dt>{dato.list_3[2]}</dt></p>;
const list_one3 = <p><dt>{dato.list_3[3]}</dt></p>;
const list_two = <p>{dato.list_2.map((dat) => <li key={dat.toString()}><dd>{dat}</dd></li>)}</p>;
const list_three = <p>{dato.list_1.map((datico) => <li key={datico.toString()}>{datico}</li>)}</p>;
const list_four = <p>{dato.list_4.map((datos) => <li key={datos.toString()}>{datos}</li>)}</p>;
const list_five = <p>{dato.list_5.map((d) => <li key={d.toString()}>{d}</li>)}</p>;
const list_six = <p>{dato.list_6.map((da) => <li key={da.toString()}>{da}</li>)}</p>;


const element = (
  <div>
    <strong>{title_one}</strong>
    {paragraph_one}
    <strong>{title_two}</strong>
    <ol>{list_three}</ol>
    <br/>
    <strong>{title_three}</strong>
    <ol><dl>
      <li class="num">{list_one}</li>
      <ul>{list_two}</ul>
      <li class="num">{list_one1}</li>
      <li class="num">{list_one2}</li>
      <li class="num">{list_one3}</li>
    </dl></ol>
    <br/>
    <div class="divn"></div>
    <strong id="#t4">{title_four}</strong>
    <ol>{list_four}</ol>
    <br/>
    <div class="divn"></div>
    <strong id="#t5">{title_five}</strong>
    <ol>{list_five}</ol>
    <br/>
    <div class="divn"></div>
    <strong id="#t6">{title_six}</strong>
    <ol>{list_six}</ol>
    <br/>
    <div class="divn"></div>
    {paragraph_two}
  </div>
);

ReactDOM.render(
  element,
  document.getElementById('root')
);
    </script>
  </body>
</html>
```


## Ejercicio #6

```jsx
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <div id="root">
    </div>
    <script src="https://unpkg.com/react@16/umd/react.development.js"></script>
    <script src="https://unpkg.com/react-dom@16/umd/react-dom.development.js"></script>
    <script src="https://unpkg.com/babel-standalone@6/babel.min.js"></script>
    <script type="text/babel">

const dato = {
  title_1: "El Noticiero Next University",
  title_2: "Programas de Tecnología",
  title_3: "Desarrollador Web",
  title_4: "Android",
  title_5: "Programa de Negocio",
  title_6: "Mercadeo Digital",
  paragraph_1: <p><strong>'Next University'</strong>'lanza su programa de formación '<strong>"Desarrollador Web"</strong>con la finalidad de
  capacitar a personas en las tendencias actuales sobre tecnologías, en el caso de desarrollador web, se basa temas relacionados a la implementaciónote
  de Front-End con tecnologias y Frameworks, tales como: HTML5, CSS, JavaScript, Boostrap, entre otros.'</p>,

  paragraph_2: <p>En<strong>'Next University'</strong>'te ofrecemos el programa<strong>'Android'</strong>'que te da las herramientas necesarias
  para diseñar e implementar aplicaciones Android para dispositivos móviles, partiendo de un conocimienti básico de Java, utilizando el
  entorno de desarrollo Android Studio. Aprenderás los aspectos fundamentales para crear aplicaciones Android interactivas, dinámicas y exitosas utilizando
  técnicas para el manejo de recursos, datos, segundos planos, localización, sensores, animaciones, gráficos, multimedia y monetización.'</p>,

  paragraph_3: <p><strong>'Next University'</strong>'coloca a tu disposición de programa de'<strong>"Mercadeo Digital"</strong>'. Sabias que...Mercadeo Digital
  o Digital Marketing es mucho mas que hacer y publicar anuncios. Se trata del consumidor y la estrategia de negocio. Estos son los puntos de partida para
  que cualquier acción de mercadeo digital sea exitosa y optimice la inversion. Este certificado, es un programa completo y practico , que permite entender
  al consumidor, la industria, la competencia y los retos del negocio propio: para crear e implementar estrategias a la medida, en diferentes plataformas
  y medios digitales. Por supuesto, monitoreando los resultados para tomar decisiones en tiempo real'</p>,
}

const title_one = <h1><strong>{dato.title_1}</strong></h1>;
const title_two = <h2><strong>{dato.title_2}</strong></h2>;
const title_three = <h3><strong>{dato.title_3}</strong></h3>;
const title_four = <h3><strong>{dato.title_4}</strong></h3>;
const title_five = <h2><strong>{dato.title_5}</strong></h2>;
const title_six = <h3><strong>{dato.title_6}</strong></h3>;
const para_1 = <p>{dato.paragraph_1}</p>;
const para_2 = <p>{dato.paragraph_2}</p>;
const para_3 = <p>{dato.paragraph_3}</p>;


const element = (
  <div>
    {title_one}
    {title_two}
    {title_three}
    {para_1}
    {title_four}
    {para_2}
    {title_five}
    {title_six}
    {para_3}
  </div>
);

ReactDOM.render(
  element,
  document.getElementById('root')
);
    </script>
  </body>
</html>
```

## Ejercicios #7


```jsx
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <div id="root">
    </div>
    <script src="https://unpkg.com/react@16/umd/react.development.js"></script>
    <script src="https://unpkg.com/react-dom@16/umd/react-dom.development.js"></script>
    <script src="https://unpkg.com/babel-standalone@6/babel.min.js"></script>
    <script type="text/babel">

const dato = {
  title_1: "Destinos Turísticos",
  title_2: "América",
  list_1: ["Argentina", "Brasil", "Chile", "Colombia", "Estados Unidos", "México", "Perú", "Venezuela"],
  list_2: ["Buenos Aires", "Bariloche"],
  list_3: ["Rio de Janeiro", "Brasilia"],
  list_4: ["Santiago", "Valparaiso"],
  list_5: ["Bógota", "Cartagena de Indias"],
  list_6: ["New York", "San Francisco"],
  list_7: ["Cancún", "Acapulco"],
  list_8: ["Lima", "Cuzco"],
  list_9: ["Margarita", "Mérida"],
}

const title_one = <h1><strong><strong>{dato.title_1}</strong></strong></h1>;
const title_two = <h2><strong><strong>{dato.title_2}</strong></strong></h2>;
const l1 = <h3><dt>{dato.list_1[0]}</dt></h3>;
const l2 = <h3><dt>{dato.list_1[1]}</dt></h3>;
const l3 = <h3><dt>{dato.list_1[2]}</dt></h3>;
const l4 = <h3><dt>{dato.list_1[3]}</dt></h3>;
const l5 = <h3><dt>{dato.list_1[4]}</dt></h3>;
const l6 = <h3><dt>{dato.list_1[5]}</dt></h3>;
const l7 = <h3><dt>{dato.list_1[6]}</dt></h3>;
const l8 = <h3><dt>{dato.list_1[7]}</dt></h3>;
const li2 = <p>{dato.list_2.map((a) => <li key={a.toString()}><dd>{a}</dd></li>)}</p>;
const li3 = <p>{dato.list_3.map((b) => <li key={b.toString()}><dd>{b}</dd></li>)}</p>;
const li4 = <p>{dato.list_4.map((c) => <li key={c.toString()}><dd>{c}</dd></li>)}</p>;
const li5 = <p>{dato.list_5.map((d) => <li key={d.toString()}><dd>{d}</dd></li>)}</p>;
const li6 = <p>{dato.list_6.map((e) => <li key={e.toString()}><dd>{e}</dd></li>)}</p>;
const li7 = <p>{dato.list_7.map((f) => <li key={f.toString()}><dd>{f}</dd></li>)}</p>;
const li8 = <p>{dato.list_8.map((g) => <li key={g.toString()}><dd>{g}</dd></li>)}</p>;
const li9 = <p>{dato.list_9.map((h) => <li key={h.toString()}><dd>{h}</dd></li>)}</p>;


const element = (
  <div>
    <dl><ol>
      {title_one}
      {title_two}
      <li>{l1}</li><ol>{li2}</ol>
      <li>{l2}</li><ol>{li3}</ol>
      <li>{l3}</li><ol>{li4}</ol>
      <li>{l4}</li><ol>{li5}</ol>
      <li>{l5}</li><ol>{li6}</ol>
      <li>{l6}</li><ol>{li7}</ol>
      <li>{l7}</li><ol>{li8}</ol>
      <li>{l8}</li><ol>{li9}</ol>
    </ol></dl>
  </div>
);

ReactDOM.render(
  element,
  document.getElementById('root')
);
    </script>
  </body>
</html>
```

## Ejercicio #8

```jsx
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <div id="root">
    </div>
    <script src="https://unpkg.com/react@16/umd/react.development.js"></script>
    <script src="https://unpkg.com/react-dom@16/umd/react-dom.development.js"></script>
    <script src="https://unpkg.com/babel-standalone@6/babel.min.js"></script>
    <script type="text/babel">

const dato = {
  title_1: "Tu concierto",
  title_2: "Bienvenido a este blog de concierto",
}

const title_one = <h2>{dato.title_1}</h2>;
const subtitle = <h3>{dato.title_2}</h3>;


const element = (
  <div>
    <img src="https://www.google.com/url?sa=i&url=https%3A%2F%2Fes.123rf.com%2Fphoto_88611621_ilustraci%25C3%25B3n-blanco-y-negro-de-la-muchedumbre-del-partido-que-anima-en-el-concierto-.html&psig=AOvVaw3Hm4O_Quif4udqcS-QB0uS&ust=1636481947055000&source=images&cd=vfe&ved=0CAsQjRxqFwoTCLC9l76wifQCFQAAAAAdAAAAABAD"/>
    {title_one}
    {subtitle}
    <img src="https://www.google.com/imgres?imgurl=https%3A%2F%2Fwww.institutoorl-iom.com%2Fwp-content%2Fuploads%2F2016%2F02%2Flos-oidos-concierto.jpg&imgrefurl=https%3A%2F%2Fwww.institutoorl-iom.com%2Fblog%2Flos-oidos-en-un-concierto%2F&tbnid=02cBs53r6RinJM&vet=12ahUKEwjT07ehron0AhWIc98KHT_fD-YQMygJegUIARDkAQ..i&docid=18nNrPiCYleBsM&w=800&h=400&itg=1&q=concierto&client=firefox-b-d&ved=2ahUKEwjT07ehron0AhWIc98KHT_fD-YQMygJegUIARDkAQ"/>
  </div>
);

ReactDOM.render(
  element,
  document.getElementById('root')
);
    </script>
  </body>
</html>
```