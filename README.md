# Raytracing

Um projeto de Ray Tracing desenvolvido em C++ que gera imagens realistas por meio do rastreamento de raios de luz, com suporte a múltiplos materiais, iluminação difusa e oCriação de cenas aleatórias com múltiplas esferas.

- Câmera dinâmica que gira ao redor da cena.
- Renderização multithreaded.
- Exportação das imagens em formato BMP.

As imagens renderizadas serão salvas na pasta especificada no código (exemplo: `C:\Users\roger\OneDrive\Documentos\Faculdade\8periodo\topicosEspeciais2\testeImagem\`).

## 🎨 Exemplo de Saída

Ao rodar o programa, ele gera 100 frames, com cada frame representando uma imagem BMP da cena em diferentes ângulos. As imagens podem ser combinadas posteriormente em um GIF ou vídeo.

## 🧠 Como Funciona

1. **Geração da Cena:**
   - `random_scene()` cria uma lista de objetos (esferas) com materiais variados.
2. **Ray Tracing:**
   - `ray_color()` calcula a cor de cada raio, lidando com reflexões e refrações.
3. **Renderização Multithreaded:**
   - `trace_lines()` divide o trabalho entre múltiplas threads, acelerando a renderização.
4. **Câmera em Movimento:**
   - A posição da câmera é atualizada a cada frame, criando a rotação circular.

## 📋 Dependências

- C++17 ou superior
- Biblioteca padrão C++ (iostream, thread, string, fstream)

## 📝 Licença

Este projeto é de código aberto e está disponível sob a licença MIT.

