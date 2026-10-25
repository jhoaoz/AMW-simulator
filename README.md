# AMW Simulator — Protótipo 0.1.0

Projeto inicial do AMW Simulator feito por código, com interface adaptável para celular e computador.

## O que já existe
- Mapa mundial interativo usando Leaflet e tiles do OpenStreetMap.
- Aeroportos selecionados e rotas desenhadas entre cidades.
- Ícones de aeronaves animados ao longo das rotas (movimento demonstrativo).
- Painel de gestão com visão geral, frota, compras, combustível, manutenção, finanças, aeroportos, notícias, mensagens e configurações.
- Interface responsiva com navegação inferior para celular.
- Estrutura de projeto pronta para empacotamento Android usando Capacitor.

## Requisitos
- Node.js LTS instalado em computador para construir o APK.
- Android Studio e SDK Android para compilar o aplicativo.
- Internet para carregar o mapa cartográfico e as fontes remotas.

## Testar no navegador
Na pasta do projeto:
```bash
npm install
npm run start
```
Abra o endereço local indicado pelo Vite.

## Preparar projeto Android
```bash
npm install
npm run build
npx cap add android
npx cap sync android
npx cap open android
```
No Android Studio, espere o Gradle sincronizar e use **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
O APK de debug normalmente ficará em `android/app/build/outputs/apk/debug/app-debug.apk`.

## Observações importantes
- O mapa depende de internet nesta versão inicial. Os servidores públicos de tiles do OpenStreetMap têm política de uso; para uma publicação comercial ou grande volume, configure um provedor de mapas adequado.
- A movimentação dos aviões é simulada localmente e não representa voos reais.
- Os preços, saldos, rotas, aeronaves e indicadores são dados de demonstração. Nenhuma compra real ou pagamento é efetuado.
- O projeto não inclui ainda salvamento persistente, contas de usuário, backend, economia balanceada, compras funcionais, notificações push ou publicação na Play Store.
- Para publicar na Play Store, serão necessários ajustes de política, assinatura de release, ícone, tela inicial, testes e revisão dos recursos de terceiros.

## Próximas etapas sugeridas
1. Fazer a seleção de aeronaves funcionar e manter o saldo salvo.
2. Implementar compras, vendas e gestão da frota.
3. Implementar combustível, manutenção e custos por voo.
4. Expandir a lista de aeroportos e destinos.
5. Criar sistema de rotas, passageiros, carga, receita e progressão.
6. Preparar assets próprios para ícone, splash screen e aeronaves.
