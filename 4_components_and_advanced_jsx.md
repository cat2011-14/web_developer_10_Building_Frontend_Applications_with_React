# Components and advanced jsx

## Использование многострочного JSX в компоненте
Однако многострочное JSX-выражение всегда должно быть заключено в скобки! Вот почему QuoteMakerоператор return содержит круглые скобки.

```
import React from 'react';
import ReactDOM from 'react-dom';

class QuoteMaker extends React.Component {
  render() {
    return (
    	<blockquote>
  			<p>
    			What is important now is to recover our senses.
  			</p>
  			<cite>
    		  <a target="_blank" href="https://en.wikipedia.org/wiki/Susan_Sontag">
      	    Susan Sontag
    		  </a>
  			</cite>
			</blockquote>
    );
  }
};

ReactDOM.render(
  <QuoteMaker />,
  document.getElementById('app')
);
```

## Используйте атрибут переменной в компоненте
Взгляните на этот объект JavaScript с именем redPanda:
```
const redPanda = {
  src:  'https://upload.wikimedia.org/wikipedia/commons/b/b2/Endangered_Red_Panda.jpg',
  alt: 'Red Panda',
  width:  '200px
};
```
Вы можете и часто будете вставлять JavaScript в JSX внутри функции рендеринга.

```
import React from 'react';
import ReactDOM from 'react-dom';


const owl = {
  title: 'Excellent Owl',
  src: 'https://s3.amazonaws.com/codecademy-content/courses/React/react_photo-owl.jpg'
};

// Component class starts here:
class Owl extends React.Component{
  render(){
    return (
      <div>
        <h1>{owl.title}</h1>
        <img 
          src={owl.src}
          alt = {owl.title} />
      </div>
    )
  }
}

ReactDOM.render(
  <Owl />,
  document.getElementById('app')
)
```
## Put Logic in a Render Function
render()Функция должна иметь returnзаявление. Однако это еще не все .

render()Функция также может быть прекрасным местом для размещения простых вычислений , которые должны произойти прямо перед тем, как компонент делает. Вот пример некоторых вычислений внутри renderфункции:
```
class Random extends React.Component {
  render() {
    // First, some logic that must happen
    // before rendering:
    const n = Math.floor(Math.random() * 10 + 1);
    // Next, a return statement
    // using that logic:
    return <h1>The number is {n}!</h1>;
  }
}
```
