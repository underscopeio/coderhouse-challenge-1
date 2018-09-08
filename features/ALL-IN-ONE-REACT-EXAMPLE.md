### Ejemplo completo de ES2015 en React

Este es un ejemplo _all in one_ de los features de ES2015 que suelen usarse en React.

La _arrow function_ es quizas una de las funcionalidades más útiles. Gracias a ellas podemos definir funciones de una manera mucho más _cómoda_:

- gracias a la nueva sintaxis podemos ahorrarnos las palabras clave `function` y `return`
- al compartir el contexto de quien la define, resuelve de manera más corta y simple la mayoría de los casos

Las _arrow function_ se definen con `() =>` (de ahí el nombre de _flecha_). Veamos la nueva sintaxis en más detalle con ejemplos en código.

#### En código

Pongamos como ejemplo la función `saludar`

```javascript
```

#### ¿Y cuándo lo uso?

En todos lados: cada vez que hagas un _forEach_ o un _map_, al definir cualquier función en la misma línea y cuando quieras usar el contexto _del padre_ de la función.
En React/React Native es muy útil para definir _handlers_ de eventos, donde quiero usar el `this` del componente (para setear el _state_ por ejemplo).

```javascript
class MiComponente extends Component {
  // NO funciona
  handleClick() {
    this.setState({ hizoClick: true }) // `this` NO hace referencia al contexto de `MiComponente` porque es una función tradicional
  }

  // Funciona
  handleClick = () => {
    this.setState({ hizoClick: true }) // `this` es el mismo que el de `MiComponente` pues alli se definió esta _arrow function_
  }

  render() {
    return <Botón onClick={this.handleClick} />
  }
}
```
