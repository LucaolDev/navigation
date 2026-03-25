1 Passagem de parâmetros obrigatórios na tela de Perfil

A tela de Perfil recebe parâmetros obrigatórios através da Navigation Compose.

Parâmetros obrigatórios são dados que precisam ser fornecidos para que a navegação funcione. Por exemplo, um ID de usuário é obrigatório para exibir o perfil correto. Se tentar navegar sem fornecer este ID, a navegação não acontece.

Ao definir um parâmetro como obrigatório na rota, o NavController valida se o valor foi fornecido antes de permitir a transição entre telas.

2 Passagem de parâmetros opcionais na tela de Pedidos

A tela de Pedidos implementa parâmetros opcionais, que podem ou não ser enviados.

A diferença dos parâmetros obrigatórios é que os opcionais possuem um valor padrão. Se nenhum valor for fornecido, a tela usa este padrão e funciona normalmente. Exemplo: uma data de entrega preferida que, se não informada, recebe uma data padrão do sistema.

Os parâmetros são definidos na rota com um valor padrão. O NavController não bloqueia a navegação se o parâmetro não for fornecido.

3 Inserindo valor ao parâmetro opcional na tela de Pedidos

Este commit implementa a lógica para processar os parâmetros opcionais quando eles são fornecidos.

O código agora recebe o valor opcional e o utiliza corretamente na interface. Se o parâmetro for fornecido, ele é usado; se não, o valor padrão permanece ativo. A interface se adapta conforme o parâmetro recebido.

A função composable da tela de Pedidos recebe o parâmetro opcional como argumento e o utiliza para atualizar o estado da interface.

4 Passagem de múltiplos parâmetros

Implementação de múltiplos parâmetros sendo enviados simultaneamente entre telas.

Em aplicações reais, é comum precisar enviar vários dados de uma vez — nome, ID, email, status, entre outros. Este commit mostra como estruturar a navegação para lidar com múltiplos parâmetros sem complicações.

A rota é definida para aceitar vários argumentos. Ao navegar, todos os parâmetros são passados simultaneamente e recebidos pela tela destino.

