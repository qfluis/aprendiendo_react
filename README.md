# aprendiendo_react
## Crear una app react
```
npx create-react-app nombre-app
```
### Scripts disponibles
```
npm start           // Inicia el servidor de desarrollo
npm run build       // Genera build de producción
npm test            // Inicia los test
npm run eject       // Opción no recomendada
```
### Estructura carpetas
- public: archivos públicos para los usuarios, contiene el index html, que contendrá nuestra aplicación.
- src: contiene el código de la app.

## Estructura componente
Ejemplo de código de un componente:
```
import './App.css';  // se pueden importar ficheros de estilos

function App() {
  // Estilo inline (utiliza las propiedades de css de javascript)
  // En lugar de kebab-kase utiliza lowerCamelCase (background-color => backgroundColor)
  const estiloLi = {
    backgroundColor: '#990000',
    color: 'white',
    padding: '5px',
    margin: '10px 5px'
  }
  const sombra = {
    boxShadow: '10px 5px 5px black'
  }

  const Li = ({children, estado}) => { // Componente, children es el contenido entre etiquetas.
    return (
      <li style={{...estiloLi, ...sombra}}>{children} - {estado}</li>
    )
  }
  const valor = 'Kiwi';

  return ( // Un componente puede devolver código JSX que será renderizado
    <ul className='clase-ul'>
      <Li estado={'Listo'}>Holiwi {valor}</Li>
      <Li estado={'Pendiente'}>Holiwiwi {valor}</Li>
    </ul>    
  );
}

export default App;
```
### Más ejemplos componente
#### Componente Button:
```
import './Button.css';

const Button = (props) => {
    return (
        <button {...props} className='btn' />
    )
    
}

export default Button
```
Al desestructurar las props en la etiqueta button, esta recibe los eventos y las propiedades pasadas al componente que la contiene.
#### Componente App (importa Button)
```
import Button from './Button';  // importación componente

function App() {  
  return ( 
    <div>
      <h1>Holiwi</h1>
      <Button onClick={()=> console.log('click')}>  
        Enviar
      </Button>      
    </div>
  );
}

export default App;
```


