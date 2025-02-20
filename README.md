# POC - Sistema de Recomendação de Imagens por Similaridade

## Descrição
Este projeto implementa um sistema de recomendação baseado em similaridade visual de imagens. Ele utiliza a rede neural convolucional **ResNet50** para extrair características visuais de imagens e o **FAISS** para busca eficiente de imagens similares. O usuário pode fazer upload de um **dataset** contendo imagens de diferentes classes e, posteriormente, fazer upload de uma imagem para buscar as mais similares dentro do banco de dados criado.

## Bootcamp
**Bootcamp:** BairesDev - Machine Learning Practitioner - Fevereiro 2025  
**Aluno:** Marcello S. Bastos  

## Funcionamento
1. O usuário faz upload de um arquivo **ZIP** contendo imagens organizadas em pastas por classe.
2. O script extrai o ZIP e constrói um **banco de características visuais** com embeddings extraídos da ResNet50.
3. O usuário faz upload de uma **imagem de consulta**.
4. O sistema retorna as **4 imagens mais similares**.

## Tecnologias Utilizadas
- **Python** (Google Colab)
- **TensorFlow/Keras** (ResNet50)
- **FAISS** (Facebook AI Similarity Search)
- **Matplotlib** (Visualização)
- **PIL (Pillow)** (Manipulação de Imagens)

## Estrutura do Projeto
```
├── dataset_tools/   # Diretório onde o dataset é extraído
│   ├── classe_1/    # Exemplo: martelo
│   ├── classe_2/    # Exemplo: chave inglesa
│   ├── classe_3/    # Exemplo: serra
│   ├── classe_4/    # Exemplo: furadeira
├── script_colab.ipynb  # Código principal do projeto
```

## Como Utilizar no Google Colab
### 1️⃣ Instalar Dependências
O script automaticamente instala as dependências necessárias, incluindo **FAISS**.

### 2️⃣ Fazer Upload do Dataset
1. Organize as imagens em pastas correspondentes às classes dentro de um diretório chamado `dataset_tools`.
2. Compacte `dataset_tools` em um arquivo ZIP.
3. Faça o upload do ZIP quando solicitado no Colab.

### 3️⃣ Construção do Banco de Features
Após o upload, o script **extrai os embeddings das imagens** e cria o banco de dados.

### 4️⃣ Fazer Upload de uma Imagem de Consulta
1. Faça o upload de uma imagem quando solicitado.
2. O sistema irá buscar e exibir as **4 imagens mais similares**.

## Exemplo de Execução
```python
# Upload do dataset (ZIP) e criação do banco de features
Faça o upload do arquivo ZIP contendo as imagens organizadas em pastas por classe.

# Upload da imagem de consulta
Agora, faça o upload de uma imagem para buscar similares.
```

## Conclusão
Este projeto demonstra como utilizar **Deep Learning** para criar um **sistema de recomendação por similaridade visual**. Com a combinação de **ResNet50** para extração de features e **FAISS** para busca eficiente, conseguimos identificar e recomendar imagens semelhantes rapidamente.

Este código pode ser expandido para aplicações reais em e-commerce, catálogos de imagens, ou sistemas de busca visual.

---
Desenvolvido para fins de **prova de conceito (POC)** no Bootcamp **BairesDev - Machine Learning Practitioner - Fevereiro 2025**.
