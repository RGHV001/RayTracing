# Raytracing\_V5

Um projeto de Ray Tracing desenvolvido em C++ que gera imagens realistas por meio do rastreamento de raios de luz, com suporte a múltiplos materiais, iluminação difusa e oCriação de cenas aleatórias com múltiplas esferas.

- Câmera dinâmica que gira ao redor da cena.
- Renderização multithreaded.
- Exportação das imagens em formato BMP.

## 📁 Estrutura do Projeto

```
Raytracing_V5/
│
├── Arquivos de Cabeçalho
│   ├── aabb.h
│   ├── bvh.h
│   ├── camera.h
│   ├── color.h
│   ├── hittable.h
│   ├── hittable_list.h
│   ├── material.h
│   ├── ray.h
│   ├── rtweekend.h
│   ├── sphere.h
│   └── vec3.h
│
├── Arquivos de Origem
│   └── Raytracing_V5.cpp
│
└── Recursos
```

## 🛠️ Compilação e Execução

**Pré-requisitos:**

- Compilador C++ (g++ ou MSVC)
- CMake (opcional, mas recomendado)
- Ambiente Windows/Linux com suporte a threads

**Compilando manualmente (g++):**

```bash
mkdir build
cd build
g++ -o Raytracing_V5 ../Raytracing_V5.cpp -std=c++17 -lpthread
```

**Executando:**

```bash
./Raytracing_V5
```

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

## 🌟 Como Contribuir

1. Faça um fork do repositório.
2. Crie uma branch para sua funcionalidade (`git checkout -b minha-funcionalidade`).
3. Faça o commit das suas alterações (`git commit -m 'Adiciona nova funcionalidade'`).
4. Envie para o repositório remoto (`git push origin minha-funcionalidade`).
5. Abra um Pull Request.

## 📝 Licença

Este projeto é de código aberto e está disponível sob a licença MIT.

---

✨ **Sinta-se à vontade para ajustar o caminho de saída das imagens e experimentar diferentes parâmetros de materiais!**

🚀 Feliz Ray Tracing! 🚀

