# Azure AI Foundry

## Passo a passo do projeto

### 1 - Abertura do Azure AI Foundry
![Image](https://github.com/user-attachments/assets/578c43fe-a61c-489d-bce1-86b7a0117de7)

### 2 - Criação do Hub "projeto dois"
![Image](https://github.com/user-attachments/assets/518ece6f-7fa7-4156-97c5-af67f86e88e2)  
Dentro do Hub, criei um projeto clicando em **"Launch Azure AI"**.

### 3 - Nomeação do projeto como "proj-dois"
![Image](https://github.com/user-attachments/assets/45fe2a6d-69c1-4d6e-8f15-af8dac7f2f13)  
Criei dois modelos e seus respectivos pontos de extremidade:  
- **gpt-4o**  
- **text-embedding-3-large**

### 4 - Configuração no Playground
Acessei o Playground e alterei o contexto do modelo de exemplo com o texto fornecido pelo instrutor:

> *"Você é um especialista em SNA que irá me ajudar com dúvidas sobre o tema."*

![Image](https://github.com/user-attachments/assets/6b9c7728-00a7-41ea-b062-9bd351523c10)

Em seguida, fui em **"Adicionar seus dados"** e cliquei em **"Adicionar uma nova fonte de dados"**:
![Image](https://github.com/user-attachments/assets/48820048-9a51-4158-8da0-c5d4c0e461d4)
![Image](https://github.com/user-attachments/assets/fdb8dfd6-4c17-4610-9fd1-fe1383865767)

Selecionei a opção de **upload** e carreguei três artigos como referência:
![Image](https://github.com/user-attachments/assets/853a2405-7a8f-4c34-bd98-48001b38a59f)

### 5 - Criação do recurso de Pesquisa de IA do Azure
Criei um novo recurso de **Pesquisa de IA do Azure**:
![Image](https://github.com/user-attachments/assets/cf6cb565-a486-4796-aa23-54d9f56bcd58)

Com o novo grupo de pesquisa criado, retornei à aba **"Adicionar os dados"**, selecionei o serviço de Pesquisa de IA do Azure e prossegui com a integração:

![Image](https://github.com/user-attachments/assets/cf63cd73-ea95-45fc-b185-655562695bda)

Confirmei e criei o **índice de valor**:
![Image](https://github.com/user-attachments/assets/93add048-10ff-4251-b2fe-81425427e018)

Agora, o Azure AI Foundry está carregando os artigos e transformando-os em vetores:

![Image](https://github.com/user-attachments/assets/2c92dd75-299e-41db-b84e-16776fa53150)


O Vetor foi criado


Com a criação do Vetor confirmada é possivel fazer perguntas ao chat com embasamento nos textos enviados pra treinamento


