1)(2.0)Explique com suas palavras:

1.1) Para que serve o ciclo de vida de uma Activity.
1.2) Qual é a função dos métodos onCreate(), onStart() e onPause().
1.3) Por que o Android pode destruir e recriar Activitys durante a rotação de tela.
1.4) Como onSaveInstanceState() ajuda a salvar um texto digitado mesmo após a rotação, de um exemplo de uso


R: O que é: Activity é uma classe da plataforma Android que desempenha a função de criar uma tela e serve como ponto de entrada para execução da aplicação ou de funções dela. As Activitys podem interagir entre si, solicitando e passando informações.

Respostas:
O ciclo de vida de uma Activity existe para gerenciar os vários estados que a tela do aplicativo passa, desde a sua criação até o momento de destruição, permitindo que o sistema e o desenvolvedor saibam quando inicializar recursos, quando liberar memória e quando salvar dados temporários.
Um exemplo disso é o método onCreate(), que é chamado quando a Activity é criada pela primeira vez e onde configuramos a interface e inicializamos variáveis. Depois de criada, temos o método onStart(), que deixa a Activity visível ao usuário. Já o método onPause() é chamado quando a Activity perde o foco, por exemplo quando outra Activity vai ser exibida, e serve para pausar processos ou salvar informações rápidas.
O Android destrói e recria Activitys durante a rotação de tela porque a mudança de orientação altera a configuração do dispositivo, e assim o sistema recarrega automaticamente o layout e os recursos adequados para a nova orientação, garantindo que a interface se adapte corretamente.
Para não perder dados nesse processo, existe o método onSaveInstanceState(), que salva o estado atual da Activity em um Bundle.
Exemplo de uso:
Se o usuário digitou um texto em um EditText, podemos salvar esse texto em onSaveInstanceState() e depois recuperar no onCreate(), garantindo que mesmo após a rotação o conteúdo digitado continue aparecendo.

2)(2.0)Explique os principais artefatos disponíveis em um projeto Android como manifesto, res , R, Activitys 

Respostas:
No  Android existem alguns artefatos principais que fazem parte da estrutura da aplicação como o AndroidManifest.xml que funciona como um “contrato” entre o aplicativo e o sistema operacional, porque nele ficam informações importantes sobre suas funcionalidades: como o nome do pacote, as permissões que o app precisa, além das Activitys que compõem o aplicativo e outras configurações essenciais.
A pasta res é onde ficam os recursos usados pelo app, como layouts em XML, imagens, ícones, textos, cores e estilos, e esses arquivos são organizados em subpastas como layout, drawable e values para facilitar o acesso. A classe R é um arquivo gerado automaticamente pelo Android Studio durante a compilação e serve para armazenar referências a todos esses recursos, permitindo que o desenvolvedor acesse layouts, strings e imagens de forma simples dentro do código. Já as Activitys são classes que representam cada tela do aplicativo e funcionam como ponto de entrada para interação do usuário, controlando o ciclo de vida da interface e a lógica que acontece em cada parte da aplicação.

# DDM-IMC
