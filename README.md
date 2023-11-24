<h1 align=center>EcoManga (Tela de Localização</h1>

<h3 align="center">Integrantes: Gustavo Henrique da Silva Souza e Guilherme Sola Gárcia</h3>

<p align=justify>		
  Dando uma explicação/descrição eu e o meu colega de classe criamos esse outro repositório porque o nosso aplicativo original está dando um pequeno erro e então resolvemos criar outro projeto somete com a tela de localização. Mas agora falando sobre o aplicativo em resumo ele encontra pontos de coleta próximos. Com um toque, você vê a localização e pode abrir em apps de mapa.
</p>

<details>
<summary><h1>Busca Rápida de Pontos de Coleta</h1></summary>
<p>  Nosso aplicativo oferece uma maneira simples e eficaz de encontrar um ponto de coleta perto de você. A tela inicial apresenta uma interface minimalista com botões de fácil acesso, campos de texto para exibição de informações e imagens representativas. Após o lançamento, o aplicativo solicita permissão para acessar sua localização para garantir uma experiência personalizada.
  
Ao clicar neste botão você pode receber instantaneamente informações precisas sobre o ponto de coleta mais próximo, com coordenadas de latitude e longitude exibidas. Além disso, oferecemos a facilidade de integração com aplicativos de mapeamento populares como Google Maps, Moovit e muito mais. Essa integração permite que você visualize de forma conveniente e rápida vários pontos de coleta ao seu redor, diretamente no aplicativo de mapa selecionado.

Nosso objetivo é fornecer soluções intuitivas para encontrar facilmente pontos de coleta próximos, ajudando os usuários a tornar o processo de coleta mais conveniente e eficiente. Ao combinar sua localização em tempo real com integrações com aplicativos de mapeamento populares, garantimos que você tenha uma experiência simplificada e eficiente ao encontrar pontos de coleta onde quer que esteja.</p>

</details>

<details>
<summary><h1>Explicando a Lógica</h1></summary>  
<p> Falando um pouco como a lógica funciona na classe MainActivity, são importadas várias classes do Android necessárias para trabalhar com localização, como LocationManager, Intent, AlertDialog, entre outras.

No método onCreate, que é executado quando a atividade é inicializada, o aplicativo solicita permissão para acessar a localização do dispositivo usando ActivityCompat.requestPermissions.

Há um botão (btn) definido no layout (R.layout.activity_main). Quando esse botão é clicado, o método pegarLocalização(View v) é invocado.

Dentro de pegarLocalização(View v), primeiro é verificado se o GPS está ativado usando lm.isProviderEnabled(LocationManager.GPS_PROVIDER). Se não estiver ativado, o método OnGPS() é chamado para pedir ao usuário que ative o GPS.

Se o GPS estiver ativado, o método getLocation() é chamado. Este método verifica se as permissões para acessar a localização foram concedidas. Se não, novamente solicita essas permissões.

Dentro de getLocation(), o aplicativo tenta obter a localização atual do dispositivo através do LocationManager. Ele verifica os provedores de localização disponíveis (GPS_PROVIDER, NETWORK_PROVIDER, PASSIVE_PROVIDER) e obtém a última localização conhecida deles.

Se a localização é obtida com sucesso de qualquer um desses provedores, as coordenadas de latitude e longitude são convertidas em strings e exibidas em um TextView chamado location.

Caso contrário, se não for possível obter a localização, é exibido um aviso (Toast) informando ao usuário que a localização não pôde ser adquirida.

O método OnGPS() exibe um diálogo AlertDialog com opções para o usuário ativar o GPS se estiver desativado ou cancelar a ação.

No final, se todas as condições forem atendidas (permissões concedidas e GPS ativado), o aplicativo cria uma intenção (Intent) para abrir o mapa com base nas coordenadas de latitude e longitude obtidas, utilizando o aplicativo padrão de mapa do dispositivo.</p>
</details>


<details>
	<summary><h1>Detalhes do App</h1></summary>
  <li><Strong>Versão do Android:</Strong>8.0 (Oreo);</li>
<li><strong>Número de Telas:</strong>1;</li>
 <li><strong>Linguagem de Programação:</strong> Java;</li>
<li><strong>IDE:</strong> Android Studio;</li>
</details>


<details>
	<summary><h1>Vídeo Testando o App</h1></summary>


https://github.com/GustavoHenrique444/Tela_Localizacao/assets/127442583/c63b9349-752d-4882-a023-6313fa1c22e2


  
</details>
