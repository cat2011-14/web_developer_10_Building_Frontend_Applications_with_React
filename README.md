# web_developer_10_Building_Frontend_Applications_with_React

## Browser Compatibility and Transpilation
двух важных инструментах для решения проблем совместимости браузера.

caniuse.com - веб-сайт, который предоставляет данные о совместимости веб-браузера для функций HTML, CSS и JavaScript. Вы узнаете, как использовать его для поиска поддержки функций ES6.

Babel - библиотека Javascript, которую можно использовать для преобразования нового неподдерживаемого JavaScript (ES6) в более старую версию (ES5), которая распознается большинством современных браузеров.

### caniuse.com I
После выпуска ECMAScript2015 (ES6) в Ecma, компании-разработчики постепенно добавили поддержку функций и синтаксиса ES6. Хотя большинство новых версий браузеров поддерживают большую часть библиотеки ES6, есть еще несколько источников проблем совместимости:

Некоторые пользователи не обновили до последней версии веб-браузера, поддерживаемого ES6.
Некоторые функции ES6, такие как модули, по-прежнему не поддерживаются большинством веб-браузеров.
Поскольку компании постепенно добавляют поддержку функций ES6, вам важно знать, как искать поддержку браузеров для каждой отдельной функции. Сайт caniuse.com - лучший ресурс для поиска информации о совместимости браузера.

В caniuse вы можете ввести функцию ES6, например let, и увидеть процент браузеров, которые ее распознают. Вы также можете увидеть, когда в каждом крупном веб-браузере (Chrome, Safari, Edge и т. Д.) Добавлена поддержка ключевого слова.


### Why ES6?
Версия JavaScript, которая предшествовала ES6, называется JavaScript ES5. Ниже перечислены три причины обновления ES5 до ES6:

Читаемость и экономия кода. Новый синтаксис часто проще для понимания (более читабелен) и требует меньше символов для создания той же функциональности (экономия кода).

Адреса источников ошибок ES5 - Некоторые синтаксис ES5 привел к распространенным ошибкам. С ES6 Ecma ввела синтаксис, который смягчает некоторые из наиболее распространенных ошибок.

Сходство с другими языками программирования - JavaScript ES6 синтаксически больше похож на другие языки объектно-ориентированного программирования. Это приводит к меньшему трению, когда опытные разработчики, не использующие JavaScript, хотят изучать JavaScript.

Поскольку ES6 решала вышеупомянутые проблемы, Ecma знала, что принятие веб-разработчиками произойдет быстро, в то время как поддержка веб-браузера отстала.

Чтобы ограничить влияние проблем совместимости браузера ES6, Ecma сделала новый синтаксис обратно совместимым, что означает, что вы можете сопоставить код JavaScript ES6 с ES5.

### Transpilation With Babel
Поскольку ES6 предсказуемо обратно совместим, группа программистов JavaScript разработала библиотеку JavaScript под названием Babel, которая переносит ES6 JavaScript в ES5.

Трансплантация - это процесс преобразования одного языка программирования в другой.

```
npm install babel-cli
```

### npm init
как настроить проект JavaScript, который переносит код при запуске npm run buildиз корневого каталога проекта JavaScript.

Первый шаг - поместить файл ES6 JavaScript в каталог с именем src . Из корневого каталога путь к файлу ES6: ./src/main.js.

Перед установкой Babel нам нужно настроить наш проект на использование менеджера пакетов узла (npm) . Разработчики используют npm для доступа и управления пакетами Node. Пакеты Node - это каталоги, которые содержат код JavaScript, написанный другими разработчиками. Вы можете использовать эти пакеты, чтобы уменьшить дублирование работы и избежать ошибок.

Прежде чем мы сможем добавить Babel в наш каталог проектов, нам нужно запустить npm init. Команда npm initсоздает файл package.json в корневом каталоге.

Package.json файл содержит информацию о текущем проекте JavaScript. Часть этой информации включает в себя:

Метаданные - это включает название проекта, описание, авторов и многое другое.
Список пакетов узлов, необходимых для проекта. Если другой разработчик хочет запустить ваш проект, npm просматривает package.json и загружает пакеты из этого списка.
Пары ключ-значение для сценариев командной строки. Вы можете использовать npm для запуска этих сокращенных сценариев для выполнения некоторого процесса. В следующем упражнении мы добавим скрипт, который запускает Babel и переносит ES6 в ES5.
Если на вашем компьютере установлен Node, вы можете создать файл package.json , набрав npm initв терминале.

Терминал предложит вам заполнить поля для метаданных проекта (имя, описание и т. Д.)

От вас не требуется отвечать на запросы, хотя мы рекомендуем, как минимум, добавить свой собственный заголовок и описание. Если вы не хотите заполнять поле, вы можете нажать Enter. npm оставит заполнить эти поля значениями по умолчанию или оставит их пустыми при создании файла package.json .

### Install Node Packages
Мы используем команду npm installдля локальной установки новых пакетов Node. Команда installсоздает папку с именем node_modules и копирует в нее файлы пакета. Команда installтакже устанавливает все зависимости для данного пакета

Чтобы установить Babel, нам нужно npm installдва пакета, babel-cliи babel-preset-env. Однако npm устанавливает более ста других пакетов, которые являются зависимостями для правильной работы Babel.




## JSX
### Why React?
React.js - это библиотека JavaScript. Он был разработан инженерами в Facebook.

Вот лишь несколько причин, по которым люди предпочитают программировать с помощью React:

Реагируйте быстро . Приложения, созданные в React, могут обрабатывать сложные обновления и при этом быстро реагировать.

Реакт является модульным . Вместо того, чтобы писать большие, плотные файлы кода, вы можете написать много меньших, многократно используемых файлов. РЕАКТ модульность может быть красивым решением в JavaScript проблем ремонтопригодности .

Реакция масштабируема . В больших программах, которые отображают много изменяющихся данных, React работает лучше всего.

Реагировать гибко . Вы можете использовать React для интересных проектов, которые не имеют ничего общего с созданием веб-приложения. Люди все еще выясняют потенциал React. Есть место для изучения.

Реакт популярен . Хотя эта причина, по общему признанию, имеет мало общего с качеством React, правда в том, что понимание React сделает вас более трудоспособным.

Если вы новичок в React, то этот курс для вас! Предварительных знаний React не ожидается. Мы начнем с самого начала и будем двигаться медленно.

### Что такое JSX?
JSX - это расширение синтаксиса для JavaScript. Он был написан для использования с React. Код JSX очень похож на HTML.

Что означает «расширение синтаксиса»?

В этом случае это означает, что JSX не является допустимым JavaScript. Веб-браузеры не могут прочитать это!

Если файл JavaScript содержит код JSX, то этот файл необходимо будет скомпилировать . Это означает, что до того, как файл попадет в веб-браузер, JSX-компилятор переведет любой JSX в обычный JavaScript.

### JSX Elements
Базовая единица JSX называется элементом JSX .
```
<h1>Hello world</h1>
```
Этот элемент JSX выглядит в точности как HTML! Единственное заметное отличие состоит в том, что вы найдете его в файле JavaScript, а не в файле HTML.

### JSX Elements And Their Surroundings
Элементы JSX рассматриваются как выражения JavaScript . Они могут идти куда угодно, куда могут идти выражения JavaScript.

Это означает, что элемент JSX может быть сохранен в переменной, передан в функцию, сохранен в объекте или массиве ... вы называете это.

Вот пример сохранения элемента JSX в переменной:
```
const navBar = <nav>I am a nav bar</nav>;
```
Вот пример нескольких элементов JSX, хранящихся в объекте:
```
const myTeam = {
  center: <li>Benzo Walli</li>,
  powerForward: <li>Rasha Loa</li>,
  smallForward: <li>Tayshaun Dasmoto</li>,
  shootingGuard: <li>Colmar Cumberbatch</li>,
  pointGuard: <li>Femi Billon</li>
};
```

### Attributes In JSX
Элементы JSX могут иметь атрибуты , как и элементы HTML.

Атрибут JSX написан с использованием HTML-подобного синтаксиса: имя , за которым следует знак равенства, а затем значение . Значение должно быть заключено в кавычки, например:
```
my-attribute-name="my-attribute-value"
```
Вот некоторые элементы JSX с атрибутами:
```
<a href="http://www.example.com">Welcome to the Web</a>;

const title = <h1 id="title">Introduction to React.js: Part I</h1>;
```
Один элемент JSX может иметь много атрибутов, как в HTML:
```
const panda = <img src="images/panda.jpg" alt="panda" width="500px" height="500px" />;
```

### Nested JSX
Вы можете вкладывать JВложенные выражения JSX могут быть сохранены как переменные, переданы в функции и т. Д., Как могут быть вложенные выражения JSX! Вот пример вложенного выражения JSX, сохраняемого как переменная:SX элементы внутри других элементов JSX, так же , как в HTML.

Вот пример элемента JSX , вложенного в элемент JSX
```
<a href="https://www.example.com"><h1>Click me!</h1></a>
```
Чтобы сделать это более читабельным, вы можете использовать разрывы строк и отступы в стиле HTML:
```
<a href="https://www.example.com">
  <h1>
    Click me!
  </h1>
</a>
```
Если выражение JSX занимает более одной строки, вы должны заключить многострочное выражение JSX в круглые скобки. Поначалу это выглядит странно, но вы привыкли к этому:
```
(
  <a href="https://www.example.com">
    <h1>
      Click me!
    </h1>
  </a>
)
```
Вложенные выражения JSX могут быть сохранены как переменные, переданы в функции и т. Д., Как могут быть вложенные выражения JSX! Вот пример вложенного выражения JSX, сохраняемого как переменная:
```
const theExample = (
   <a href="https://www.example.com">
     <h1>
       Click me!
     </h1>
   </a>
 );
```

### JSX Outer Elements
Есть правило, которое мы не упомянули: у выражения JSX должен быть ровно один внешний элемент.

Другими словами, этот код будет работать
```
const paragraphs = (
  <div id="i-am-the-outermost-element">
    <p>I am a paragraph.</p>
    <p>I, too, am a paragraph.</p>
  </div>
);
```
Но этот код не будет работать:
```
const paragraphs = (
  <p>I am a paragraph.</p> 
  <p>I, too, am a paragraph.</p>
);
```
Первый открывающий тег и окончательное закрытие тега из выражения JSX должны принадлежать одному и тому же элементу JSX!

Об этом правиле легко забыть, и в итоге возникают ошибки, которые сложно диагностировать.

Если вы заметили, что выражение JSX имеет несколько внешних элементов, решение обычно простое: оберните выражение JSX в div

### Rendering JSX
Для визуализации в себя средство выражения JSX , чтобы сделать вид на экране.

JavaScript чувствителен к регистру, поэтому убедитесь, что ReactDOM правильно написан с большой буквы!

```
ReactDOM.render(<h1>Hello world</h1>, document.getElementById('app'));
```

```
import React from 'react';
import ReactDOM from 'react-dom';
```

### ReactDOM.render() I
Вы можете увидеть то, что называется ReactDOM. Это что?

ReactDOMэто имя библиотеки JavaScript. Эта библиотека содержит несколько специфичных для React методов, каждый из которых так или иначе имеет дело с DOM .

Позже мы поговорим о том, как ReactDOMпопал в ваш файл. Пока просто пойми, что это твое использование.

Перемещение немного вправо, и вы можете увидеть один из ReactDOMметодов «S: ReactDOM.render().

ReactDOM.render()это наиболее распространенный способ рендеринга JSX. Он принимает выражение JSX, создает соответствующее дерево узлов DOM и добавляет это дерево в DOM. Это способ отображения выражения JSX на экране.

ReactDOM.render()Первый аргумент должен быть выражением JSX, и он будет отображаться на экране.

### ReactDOM.render() II
Вы только что узнали , что ReactDOM.render()делает его первый аргумент появляется на экране. Но где на экране должен появиться первый аргумент?

Первый аргумент добавляется к любому элементу, выбранному вторым аргументом.

В редакторе кода выберите index.html . Посмотрите, сможете ли вы найти элемент, который будет выбран document.getElementById('app').

Этот элемент действовал как контейнер для ReactDOM.render()первого аргумента! 

### Passing a Variable to ReactDOM.render()
ReactDOM.render()«S первый аргумент должен оценить для выражения JSX, он не должен буквально быть выражением JSX.

Первым аргументом также может быть переменная, если эта переменная оценивается как выражение JSX.

В этом примере мы сохраняем выражение JSX как переменную с именем toDoList. Затем мы передаем toDoListв качестве первого аргумента ReactDOM.render():
```
const toDoList = (
  <ol>
    <li>Learn React</li>
    <li>Become a Developer</li>
  </ol>
);

ReactDOM.render(
  toDoList, 
  document.getElementById('app')
);
```

### The Virtual DOM
Особенность в том, ReactDOM.render()что он обновляет только измененные элементы DOM .

Это означает, что если вы рендерите одну и ту же вещь дважды подряд, второй рендер ничего не сделает:
```
const hello = <h1>Hello world</h1>;

// This will add "Hello world" to the screen:

ReactDOM.render(hello, document.getElementById('app'));

// This won't do anything at all:

ReactDOM.render(hello, document.getElementById('app'));
```
Это важно! Только обновление необходимых элементов DOM - большая часть того, что делает React таким успешным.

React выполняет это благодаря так называемой виртуальной DOM. 

Cтатья

Реагируйте: Виртуальный DOM
Борьба с бесполезной манипуляцией DOM
Эта проблема
Манипулирование DOM - это сердце современной интерактивной сети. К сожалению, это также намного медленнее, чем большинство операций JavaScript.

Эта медлительность усугубляется тем фактом, что большинство JavaScript-фреймворков обновляют DOM гораздо больше, чем нужно.

В качестве примера предположим, что у вас есть список из десяти элементов. Вы отмечаете первый пункт. Большинство фреймворков JavaScript перестраивают весь список . Это в десять раз больше работы, чем необходимо! Только один предмет изменился, но остальные девять были восстановлены именно так, как они были раньше.

Восстановление списка не представляет особой проблемы для веб-браузера, но современные веб-сайты могут использовать огромное количество манипуляций с DOM. Неэффективное обновление стало серьезной проблемой.

Чтобы решить эту проблему, люди в React популяризировали нечто, называемое виртуальным DOM.

Виртуальный ДОМ
В React для каждого объекта DOM существует соответствующий «виртуальный объект DOM». Виртуальный объект DOM - это представление объекта DOM, похожее на облегченную копию.

Виртуальный DOM-объект обладает теми же свойствами, что и реальный DOM-объект, но ему не хватает реальной возможности напрямую изменять то, что находится на экране.

Управление DOM происходит медленно. Управлять виртуальной DOM намного быстрее, потому что на экране ничего не рисуется. Думайте о манипулировании виртуальным DOM как о редактировании плана, а не о перемещении комнат в реальном доме.

Как это помогает
Когда вы визуализируете элемент JSX, каждый виртуальный объект DOM обновляется.

Это звучит невероятно неэффективно, но стоимость незначительна, потому что виртуальный DOM может обновляться так быстро.

После обновления виртуального DOM React сравнивает виртуальный DOM с виртуальным снимком DOM, который был сделан непосредственно перед обновлением.

Сравнивая новый виртуальный DOM с версией, предшествующей обновлению, React точно определяет , какие виртуальные объекты DOM изменились. Этот процесс называется «диффузией».

Как только React узнает, какие виртуальные объекты DOM изменились, React обновит эти объекты и только эти объекты в реальном DOM. В нашем предыдущем примере React был бы достаточно умен, чтобы перестроить ваш один отмеченный элемент списка и оставить остальную часть списка в покое.

Это имеет большое значение! React может обновлять только необходимые части DOM. Репутация React для производительности во многом обусловлена этим нововведением.

Итак, вот что происходит, когда вы пытаетесь обновить DOM в React:

Весь виртуальный DOM обновляется.
Виртуальный DOM сравнивается с тем, как он выглядел до того, как вы обновили его. Реагирует, выясняет, какие объекты изменились.
Измененные объекты и только измененные объекты обновляются в реальном DOM.
Изменения в реальном DOM приводят к изменению экрана.

Если вы хотите узнать больше о виртуальной DOM, вот хорошее место для начала .

https://reactkungfu.com/2015/10/the-difference-between-virtual-dom-and-dom/


