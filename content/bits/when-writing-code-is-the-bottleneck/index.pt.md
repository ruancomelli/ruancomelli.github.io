+++
title = "Agentes de código quando escrever código é o gargalo"
date = 2025-10-08
description = "Hoje percebi como agentes de código podem ser úteis quando escrever código _é_ o gargalo"

[taxonomies]
tags = ["bits", "trabalho-remoto", "desenvolvimento", "ia", "llm", "agente-de-codigo", "desabafo"]
+++

Com um novo agente de código de IA sendo anunciado quase todo dia, devemos nos lembrar de que [escrever código nunca foi o gargalo](https://ordep.dev/posts/writing-code-was-never-the-bottleneck)...

... exceto quando _é o gargalo, sim_.

---

### O contexto

Trabalhar como autônomo significa lidar com políticas de clientes que não foram projetadas com o meu ambiente de desenvolvimento em mente - ou a minha paz de espírito. O fato de não ser formalmente um empregado faz as contratantes serem mais cautelosas quando se trata de compartilhar informação confidencial ou propriedade intelectual comigo.

Atualmente, estou trabalhando para uma empresa que não permite que código, mensagens ou qualquer outra forma de propriedade intelectual seja armazenada nas máquinas dos contratados. Em vez disso, somos obrigados a nos conectar remotamente a instâncias do Windows Virtual Desktop (WVD)[^1] mesmo se tudo o que queremos é enviar uma mensagem no Microsoft Teams[^2]. E, claro, não há cliente nativo para se conectar a WVDs no Ubuntu (que é o meu sistema operacional) - então preciso usar um cliente web. Até agora, essa interação pode ser representada como no seguinte [diagrama Mermaid](https://mermaid.js.org/):

{% mermaid() %}
sequenceDiagram
participant Meu computador
participant WVD

    Meu computador<<->>WVD: latência
    Note over Meu computador,WVD: via meu navegador web

{% end %}

Você deve achar que isso já é doloroso o suficiente, certo? Errado. Além dessa complicação, todo o desenvolvimento de software é feito em _code servers_ do Azure DevOps acessados via Microsoft Edge[^3] - então o caminho do meu laptop até o código que quero escrever se parece mais ou menos assim:

{% mermaid() %}
sequenceDiagram
participant Meu computador
participant WVD
participant Code Server

    Meu computador<<->>WVD: latência
    WVD<<->>Code Server: mais latência
    Note over Meu computador,WVD: via meu navegador web
    Note over WVD,Code Server: via Edge

{% end %}

Se quiser, você também pode considerar que os navegadores web adicionam ainda mais latência - o fato é que toda essa configuração significa que caracteres que digito no meu teclado às vezes levam 2 segundos para aparecer na tela. Há também um atraso ao mover o mouse que me faz clicar frequentemente na coisa errada. E já mencionei que as nossas instâncias do WVD têm apenas 8GB de RAM, o que _definitivamente não é suficiente_ quando você está executando uma máquina Windows com uma conexão remota (eu), Teams e Edge abertos?

Talvez eu só não seja tão habilidoso quanto você, caro leitor... mas toda essa limitação realmente prejudica minha produtividade. Tarefas simples de escrita de código se transformam em crises de frustração. Digitar código, inspecionar arquivos e até navegar na internet - tudo isso se tornou um pesadelo. De repente, _escrever código se tornou o gargalo_.

Mas, então, entram os agentes de código para salvar o dia.

---

### Agentes de código para a vitória

Os _code servers_ à nossa disposição vêm com [Cline](https://cline.bot/) pré-instalado como uma extensão do VS Code, um agente de código dentro da IDE que não questiona sua própria sanidade com tanta frequência quanto eu. Tenho dependido muito do Cline para escrever código para mim. Ele é capaz de lidar com a maioria das tarefas de codificação, e também é bem rápido. Além disso, nossa equipe de desenvolvimento fez um ótimo trabalho ao definir [`.clinerules`](https://docs.cline.bot/features/cline-rules), o que permite que o bot entende a estrutura da base de código sem que eu tenha que especificar tudo o tempo todo. E, acima de tudo, [o site do Cline é bonitinho](https://web.archive.org/web/20251004184616/https://cline.bot/).

Enquanto o agente de código faz o trabalho pesado, posso focar na visão geral e em aspectos de mais alto nível. Eu penso sobre o problema (uma correção de bug ou a implementaão de uma nova _feature_), projeto a solução, e deixo o Cline lidar com os detalhes da implementação. Também ajuda que o Cline propõe mudanças gradativamente, um arquivo por vez. Isso me permite revisar e melhorar as alterações propostas sem ter que ficar alternando entre múltiplas janelas ou abas, o que é um grande avanço para mim.

Nem tudo são flores, é claro. Agentes de código podem ser muito teimosos, e frequentemente cometem erros que requerem intervenção manual. Além disso, eles não entendem as nuances do projeto ou da tarefa em questão a menos que eu forneça mais contexto ou orientação. Eu também tenho a sensação de que o código gerado por agentes de código é de qualidade mediana na melhor das hipóteses, necessitando diversos ajustes antes de eu me dar por satisfeito.

---

### Considerações finais

Não estou aqui para defender agentes de código e LLMs em geral. Essas ferramentas devem ser usadas com responsabilidade e não são adequadas para todas as tarefas.

O artigo [Writing Code Was Never The Bottleneck](https://ordep.dev/posts/writing-code-was-never-the-bottleneck) está certíssimo, e recomendo fortemente a sua leitura. Só achei engraçado que me encontrar numa situação em que, sim, escrever código era o gargalo - e que um agente de código salvou o dia.

---

### Notas de rodapé

[^1]: Estou _tão feliz_ de estar de volta ao Windows
[^2]: O _melhor_ aplicativo de comunicação para equipes
[^3]: O navegador recomendado pela Microsoft - provavelmente porque é _o melhor_ que existe
