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
import './App.css';

function App() {

  const Li = ({children, estado}) => {
    return (
      <li className='clase-li'>{children} - {estado}</li>
    )
  }
  const valor = 'Kiwi';

  return (   
    <ul className='clase-ul'>
      <Li estado={'Listo'}>Holiwi {valor}</Li>
    </ul>    
  );
}

export default App;
```