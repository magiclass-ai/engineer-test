# engineer-test

O **Serviço de Localização de Usuários em Eventos Públicos** é uma aplicação que permite registrar e consultar a localização atual e o histórico de posicionamento de participantes dentro de um espaço (como shows, feiras, estádios ou centros de convenções). A arquitetura deve ser projetada para ser escalável, eficiente e de alto desempenho.

---

## 🎯 Desafio

Você deverá construir um sistema que permita que usuários de um evento compartilhem sua posição atual dentro do espaço (ex: setor, coordenadas internas) e consulte onde estão seus amigos ou grupos, de forma eficiente.

---

## 📌 Rotas Necessárias

- **Salvar Posição do Usuário**  
  Esta API deve permitir que um usuário envie sua posição atual (ex: coordenada x/y ou localização nomeada como "Setor A").

- **Recuperar Posição Atual do Usuário**  
  Esta API deve retornar a posição atual de um usuário com base no seu ID.

- **Recuperar Histórico das Últimas Posições do Usuário**  
  Deve retornar o histórico das últimas posições registradas para o usuário.

- **Retornar Usuários Próximos a um Local**  
  Deve retornar uma lista de usuários dentro de um raio especificado em relação a uma posição fornecida.

 - **Retornar Usuários em um Setor**  
  Esta API deve retornar todos os usuários localizados atualmente em um determinado setor do evento.

---

## 🧰 Tecnologias Utilizadas

Você tem liberdade para escolher as tecnologias que considerar mais adequadas, mas deve justificar suas escolhas.

**Requisitos obrigatórios:**

- Utilização de Golang.
- O projeto deve ser executável via `docker-compose`.
- O código deve estar documentado e fácil de executar/testar.
- Utilize cache para otimizar leituras frequentes (ex: Redis).
- O banco de dados deve suportar consultas geoespaciais (ex: PostgreSQL + PostGIS, MongoDB com GeoJSON).
- Alterações de posição devem gerar eventos (ex: Kafka, Redis Streams, etc).
- APIs RESTful ou GraphQL bem definidas.

---

## 🏛 Arquitetura e Considerações

- A aplicação deve ser escalável para grandes volumes de usuários e posições simultâneas.
- Utilize microsserviços se considerar adequado, com responsabilidades bem separadas.
- Garanta eficiência nas leituras (ex: posição atual e usuários próximos) e nas gravações concorrentes.
- Pense na estrutura dos dados com foco em performance e escalabilidade.

---

## ✅ Entrega do Projeto

- Crie um repositório público no GitHub.
- Envie o link ao recrutador por e-mail.
- Certifique-se de que haja um `README.md` explicando como rodar e testar o projeto.

Boa sorte 🚀
