# Corrida VR - Protótipo

Protótipo de aplicação VR com vídeo 360 para Meta Quest.

## Recursos

- Vídeo 360 graus imersivo
- UI com métricas em tempo real:
  - Velocidade (km/h)
  - Contador de passos
  - Distância percorrida (metros)
- Compatível com Meta Quest via navegador

## Como usar

### No computador (desenvolvimento):

1. Abra o arquivo `index.html` em um servidor HTTP local
   - Você pode usar: `python -m http.server 8000`
   - Ou qualquer outro servidor local
2. Acesse: `http://localhost:8000`

### No Meta Quest:

1. Hospede os arquivos em um servidor web (GitHub Pages, Netlify, Vercel, etc)
2. No Meta Quest, abra o navegador
3. Acesse a URL do seu app
4. Clique no ícone VR no canto inferior direito para entrar em modo VR

## Controles

- **WASD**: Mover para frente/trás/esquerda/direita
- **Mouse/Headset**: Olhar ao redor
- **Cursor**: Apontar e clicar no botão PLAY

## Personalizações

### Trocar o vídeo 360:

Substitua a URL do vídeo na linha 25:

```html
<source src="SEU_VIDEO_360.mp4" type="video/mp4">
```

### Ajustar sensibilidade dos passos:

No JavaScript (linha 86), altere o valor de `stepThreshold`:

```javascript
this.stepThreshold = 0.5; // Distância em metros para contar 1 passo
```

## Tecnologias

- **A-Frame 1.4.2**: Framework WebVR
- **Three.js**: Renderização 3D (incluído no A-Frame)
- **WebXR**: API nativa para VR

## Notas

- O vídeo atual é um exemplo genérico - substitua pelo seu vídeo 360
- As métricas são calculadas com base no movimento da câmera VR
- Funciona tanto em desktop quanto em headsets VR
