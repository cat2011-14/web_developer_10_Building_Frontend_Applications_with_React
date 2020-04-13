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
