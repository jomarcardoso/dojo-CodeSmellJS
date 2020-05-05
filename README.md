# Code Smells JS

Na hora de revisar o código podemos ficar atentos para essas pistas de que tem algo errado.

## Dados não formatados

Os dados não formatados são suscetíveis a erros e torna a manutenção mais difícil, pois precisa achar o dado no meio de um monte de sujeita, além disso tudo também deixa o código esquisito, como mostrado abaixo.

### Vetores denecessários

Dado assim não deveria chegar na cadama de renderização.

```html
<div>
 {phoneNumber[0]}
</div>
```

### Objetos desnecessários

Quando o objeto tem apenas um atributo.

**errado**
```js
const phone = {
  number: '55555555',
};
```

**correto*
```js
const phoneNumber = '55555555';
```

### Verificações desnecessárias

Na camada de renderização não deveria ter que verificar se um dado existe.

```jsx
<ul>
  {data?.list((item) => <li>{item}<li>)}
<ul>
```

```jsx
<div>{data.phoneNumber ? 'data.phoneNumber' : ''}</div>
```
