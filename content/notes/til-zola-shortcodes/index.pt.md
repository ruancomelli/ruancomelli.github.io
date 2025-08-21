+++
title = "TIL: Shortcodes do Zola aceitam parâmetros nomeados"
date = 2025-01-15
description = "Descoberta rápida sobre a flexibilidade dos shortcodes do Zola"

[taxonomies]
tags = ["zola", "web-dev", "til"]

[extra]
kind = "TIL"
+++

Estava lutando para passar dados complexos para shortcodes, até descobrir que posso fazer:

Revolucionário para minhas galerias de imagens! Acabou a confusão com parâmetros posicionais.

Também aprendi que posso misturar posicionais e nomeados:

```
{{ image_gallery("caminho/pasta", alt="Descrição da galeria", lazy=true) }}
```

A documentação do Zola menciona isso mas é fácil passar batido. Às vezes as melhores descobertas vêm da frustração com o jeito "óbvio" não funcionando.
