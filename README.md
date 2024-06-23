# Relógio

Este projeto é um relógio digital simples, desenvolvido com HTML, CSS e JavaScript, que exibe as horas, minutos e segundos atualizados em tempo real. A interface é estilizada para proporcionar uma experiência visual agradável.

## Visão Geral

### Funcionalidades
- Exibe horas, minutos e segundos.
- Atualização automática em tempo real.

## Tecnologias Utilizadas
- **HTML**: Estrutura da aplicação.
- **CSS**: Estilização e layout responsivo.
- **JavaScript**: Lógica para atualização do relógio.

## Estrutura do Projeto

### HTML
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="style.css" />
    <title>Relógio</title>
</head>
<body>
    <div class="relogio">
        <div>
            <span id="horas">00</span>
            <span class="tempo">Horas</span>
        </div>
        <div>
            <span id="minutos">00</span>
            <span class="tempo">Minutos</span>
        </div>
        <div>
            <span id="segundos">00</span>
            <span class="tempo">Segundos</span>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>
```

### CSS
```css
* {
    font-family: monospace;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    height: 100vh;
    background: linear-gradient(120deg, #f5d508d8, #39df23da);
    display: flex;
    align-items: center;
    justify-content: center;
}

.relogio {
    display: flex;
    align-items: center;
    justify-content: space-around;
    height: 200px;
    width: 550px;
    background: transparent;
    border-radius: 3px;
    box-shadow: 0px 8px 10px rgba(0, 0, 0, .5);
}

.relogio div {
    height: 170px;
    width: 150px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: white;
    background: rgba(5, 5, 5, 0.9);
    box-shadow: 5px 5px 15px rgba(0, 0, 0, 0.7);
    border-radius: 7px;
    letter-spacing: 3px;
}

.relogio span {
    font-weight: bolder;
    font-size: 60px;
}

.relogio span.tempo {
    font-size: 20px;
}
```

### JavaScript
```javascript
const horas = document.getElementById("horas");
const minutos = document.getElementById("minutos");
const segundos = document.getElementById("segundos");
const relogio = setInterval(function time() {
    let dateToday = new Date();
    let hr = dateToday.getHours();
    let min = dateToday.getMinutes();
    let s = dateToday.getSeconds();

    if (hr < 10) hr = '0' + hr;
    if (min < 10) min = '0' + min;
    if (s < 10) s = '0' + s;

    horas.textContent = hr;
    minutos.textContent = min;
    segundos.textContent = s;
});
```

## Como Usar

1. **Visualizar o relógio**: Ao abrir a página HTML, o relógio digital será exibido no centro da tela.
2. **Tempo real**: O relógio atualiza automaticamente os valores de horas, minutos e segundos.

## Contribuição
Para contribuir com este projeto, faça um fork do repositório, crie um branch com suas alterações e envie um pull request para revisão.

## Autor
Desenvolvido por D1MELLO!

## Licença
Este projeto está licenciado sob a [MIT License](LICENSE).
