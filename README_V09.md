# TEX Drive V0.9 — candidato a homologação

## Publicação
1. Extraia o ZIP e envie o conteúdo (index.html na raiz) a um repositório GitHub.
2. Na Vercel, importe o repositório como projeto estático, preset Other, sem comando de build, diretório de saída raiz.
3. Abra a URL HTTPS no Safari do iPad. Permita localização durante uso.
4. Compartilhar > Adicionar à Tela de Início. Abra o ícone e teste novamente.
5. Pare o veículo antes de configurar destinos, mídia ou registros. Não use como único navegador até homologação.

## Uso
- Dashboard: ative GPS; em Navegação pesquise destino, selecione, calcule e inicie orientação.
- Mídia: selecione rádio ou arquivo local. Spotify abre o serviço oficial; não há autenticação integrada.
- Computador de bordo: inicie e encerre registro GPS.
- Meu Peugeot: informe odômetro, abastecimentos e lembretes; não há leitura OBD2.
- Viagens: informe distância, consumo e preço; pedágios não incluídos.
- Configurações: temas, modo leve, exportação JSON (não há restauração automática).

## Testes realizados
Node --check: scripts inline e Service Worker OK. Chromium 1024x768: oito telas, cálculo de viagem (100 km, 10 km/L, R$6/L = R$60), registro de odômetro, modo condução, tema; zero exceções JS observadas. HTML injetado, armazenamento simulado em memória, rede externa bloqueada; navegação file:// e HTTPS de teste bloqueadas pelo ambiente. Não confirma persistência após fechar, GPS, SW, áudio ou APIs.

## Checklist no iPad (pendente)
- Identificar modelo, iOS e espaço livre; verificar diagnóstico.
- Permissões GPS, precisão, velocidade e interrupção de sinal.
- Pesquisa de endereço, mapa e cálculo de rota; testar parado ou com passageiro operando.
- Voz, recálculo e rota alternativa; conferir avisos de perda de precisão.
- Rádio, arquivos locais, Bluetooth, Spotify externo e retorno ao app.
- Registros locais após fechar e reabrir; exportar backup.
- Instalação e reabertura offline após primeira carga; mapa e rotas online somente.
- Verificar legibilidade, aquecimento, consumo de bateria, desempenho e posicionamento físico seguro.

## Alterações V0.9
Validação de alternativas de rota e números de viagem; ocultação de estimativas quando GPS impreciso/desatualizado ou fora da rota; recuperação após permissão GPS negada; limpeza do URL de backup; abertura Spotify sem acesso ao opener; cache v09. Design V0.8 preservado. OBD2 e mapa offline continuam pendentes. Não há trânsito ao vivo. Dados locais e posição enviada a serviços externos conforme funcionalidade; não há sincronização na nuvem.