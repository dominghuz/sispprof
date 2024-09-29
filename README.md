# Gestão e Marcação de Presença dos Professores do ISPO-ZANGO

Este projeto consiste no desenvolvimento de um aplicativo mobile para o controle de presença dos professores do Instituto Superior Politécnico do Zango (ISPO-ZANGO). Utilizando QR Codes, o sistema facilita a marcação de presença, monitoramento de assiduidade e geração de relatórios, além de calcular o salário dos professores com base nas presenças e módulos lecionados.

## *Funcionalidades Principais*

- Marcação de presença através de QR Code.
- Monitoramento de assiduidade e pontualidade dos professores.
- Cálculo automático do salário com base no grau acadêmico (Licenciado, Mestre, Doutor).
- Relatórios diários, semanais e mensais de presença.
- Gerenciamento de módulos lecionados por períodos (manhã, tarde, noite).

## *Requisitos do Sistema*

- *Frontend*: Desenvolvido em React Native, permitindo o uso em plataformas Android e iOS.
- *Backend*: Implementado com Node.js e Express.
- *Banco de Dados*: Utilizado MySQL para armazenar informações de professores, presenças, módulos e pagamentos.
- *Leitura de QR Code*: Implementada com a biblioteca react-native-qrcode-scanner.

## *Instalação*
### *Pré-requisitos*

- Node.js (v12 ou superior)
- NPM ou Yarn
- MySQL
- Expo CLI
- Git
- Android Studio ou Xcode (para emuladores ou build de dispositivos móveis)

### *Passos para Clonar o Repositório*

1. Clonar ou repositório:
```bash
git clone https://github.com/seu-usuario/repositorio.git
```
2. Navegue para o diretório do projeto:
```bash
cd nome-do-projeto
```
3. Instalar as dependências:
```bash
npm install
# ou
yarn install
```
4. Configure o banco de dados MySQL:

- Crie um banco de dados no MySQL.
- Configure o arquivo .envcom as credenciais de acesso ao banco de dados
```bash
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=sua-senha
DB_NAME=nome_do_banco
```

5. Execute as migrações do banco de dados:
```bash
npm run migrate
```
6. Início do servidor backend:
```bash
npm run start
```
7. Rodou o aplicativo mobile:
```bash
npx react-native run-android  # Para Android
npx react-native run-ios      # Para iOS
```

## Uso

1. Os professores podem marcar presença utilizando o aplicativo, escaneando um QR Code gerado para cada aula.
2. O administrador pode visualizar relatórios de presença e cálculo do salário dos professores com base no número de módulos lecionados e no grau acadêmico.
3. O sistema calcula automaticamente o pagamento com base no valor por módulo lecionado (6.000 Kz para Licenciados, 6.500 Kz para Mestres e 7.000 Kz para Doutores).

## Estrutura do Projeto

```bash
.
├── src
│   ├── components   # Componentes React Native
│   ├── screens      # Telas do aplicativo
│   ├── services     # Conexões com API e banco de dados
│   └── utils        # Funções utilitárias e constantes
├── backend
│   ├── controllers  # Controladores das rotas
│   ├── models       # Modelos de banco de dados
│   └── routes       # Definição das rotas da API
└── README.md

```


## Contribuição

1. Faça um fork do projeto.
2. Crie um branch para a funcionalidade que deseja implementar
```bash
git checkout -b minha-nova-funcionalidade
```
3. Faça suas alterações:
```bash
git commit -m 'Adiciona nova funcionalidade'
```
4. Faça o push do branch:
```bash
git push origin minha-nova-funcionalidade
```
5. Crie um Pull Request para revisão.

## Licença

Este projeto está licenciado sob uma licença do MIT .
