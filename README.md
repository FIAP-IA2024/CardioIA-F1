# FIAP - Faculdade de Informática e Administração Paulista

<p align="center">
<a href= "https://www.fiap.com.br/"><img src="https://raw.githubusercontent.com/lfusca/templateFiap/main/assets/logo-fiap.png" alt="FIAP - Faculdade de Informática e Admnistração Paulista" border="0" width=40% height=40%></a>
</p>

<br>

## 👨‍🎓 Integrantes do Grupo

- RM559800 - [Jonas Felipe dos Santos Lima](https://www.linkedin.com/in/jonas-felipe-dos-santos-lima-b2346811b/)
- RM560173 - [Gabriel Ribeiro](https://www.linkedin.com/in/ribeirogab/)
- RM559926 - [Marcos Trazzini](https://www.linkedin.com/in/mstrazzini/)
- RM559645 - [Edimilson Ribeiro](https://www.linkedin.com/in/edimilson-ribeiro/)

## 👩‍🏫 Professores

### Coordenador(a)

- [André Godoi](https://www.linkedin.com/in/profandregodoi/)

---

## 📌 Entregas do Projeto

### Fase 1 – Batimentos de Dados: Mapeando o Coração Moderno

---

## **CardioIA: Ecossistema de Cardiologia Inteligente**

### 🎯 Objetivos

O principal objetivo deste projeto é atuar como cientista de dados, buscando, organizando e compreendendo conjuntos de dados cardiológicos. Esses dados servirão como a base para alimentar os módulos inteligentes do projeto CardioIA, com foco em triagem, diagnósticos, monitoramento e assistência remota.

---

### 📚 Análise e Preparação dos Dados

#### Parte 1: Dados Numéricos (IoT)

O dataset numérico é composto por uma planilha de duas tabelas, localizadas na pasta `data`: `Dados_numericos.xlsx`, com 700 linhas de dados simulados de pacientes, e a segunda tabela da mesma planilha, `Legenda.csv`, descreve as variáveis e seus valores de referência. As variáveis incluem **idade, sexo, pressão arterial, colesterol, frequência cardíaca, histórico de doenças e sintomas**.

- **Origem:** Dados simulados com referências clínicas e estatísticas de saúde cardiovascular, utilizando o gerador de dados [**SyntheaTM**](https://synthetichealth.github.io/synthea/?utm_source=chatgpt.com).

**Relevância Clínica para IA:**
Para este projeto, as variáveis mais relevantes são a **Pressão Arterial** e o **Colesterol**.

* **Pressão Arterial:** É um dos indicadores vitais mais diretos e mensuráveis da saúde cardiovascular. Sua inclusão permite ao CardioIA identificar padrões de risco e prever a probabilidade de eventos como AVCs e ataques cardíacos. Por ser uma variável facilmente capturada por dispositivos IoT, é fundamental para o monitoramento contínuo e em tempo real dos pacientes.
* **Colesterol:** Níveis elevados de colesterol são um dos principais fatores de risco para doenças crônicas como a aterosclerose. A IA pode combinar os dados de colesterol com outras variáveis, como a idade e o histórico de doenças, para gerar um score de risco personalizado para cada paciente, auxiliando na triagem e na recomendação de tratamentos preventivos.

#### Parte 2: Dados Textuais (NLP)

Dois artigos científicos, localizados na subpasta `docs`, foram selecionados para esta atividade. Eles foram formatados para estarem limpos e prontos para análise de NLP.

* **Artigo 1:** Este texto é a base para entendermos a percepção do paciente. Ele contém relatos diretos e subjetivos, como a descrição de "sensação de sufocamento" e o "medo de morrer". Para a IA, isso é valioso porque permite ir além do diagnóstico e compreender o impacto emocional da doença. Um modelo de NLP pode ser treinado para:
    * **Análise de Sentimentos e Subjetividade:** Quantificar o grau de desconforto ou ansiedade expresso nos relatos, ajudando a criar um sistema de triagem que prioriza não apenas a gravidade clínica, mas também o sofrimento do paciente.
    * **Extração de Sintomas Detalhados:** Identificar as nuances dos sintomas (ex: "dor no peito do tipo fisgada") e como eles afetam as atividades diárias, o que é crucial para uma assistência médica personalizada.

* **Artigo 2:** Este artigo de revisão é a base para entendermos o contexto mais amplo da jornada do paciente. Como um texto mais conceitual e estruturado, ele permite que a IA compreenda os desafios externos ao tratamento. O NLP aqui pode ser explorado para:
    * **Classificação de Tópicos e Fatores de Risco:** Categorizar automaticamente textos em temas como "Barreiras de Adesão" (custo de medicamentos, complexidade do tratamento) e "Fatores de Suporte" (suporte familiar, relação com profissionais).
    * **Extração de Conceitos-Chave:** Identificar termos e frases que definem a motivação e a adesão, permitindo que a IA analise novos documentos para entender o que pode estar impedindo um paciente de seguir o plano de tratamento.

Em conjunto, a análise de ambos os textos no CardioIA permitirá um diagnóstico e um plano de tratamento que consideram não apenas os sintomas físicos, mas também a experiência subjetiva e as barreiras socioeconômicas e psicológicas do paciente, criando uma solução de IA mais humanizada e eficaz.

#### Parte 3: Dados Visuais (Visão Computacional)

O conjunto de dados visuais, composto por imagens de 700 pacientes que passaram por raios-X torácicos, é a base para o desenvolvimento de um sistema que otimiza o diagnóstico médico. A coleção de imagens pode ser utilizada para:

* **Detecção de Padrões e Anomalias:** As imagens de raio-X são a "linguagem visual" da patologia. Elas contêm padrões de densidade e textura que, quando interpretados por um sistema de análise visual, revelam a presença de doenças. Por exemplo, a imagem de um tórax saudável possui um padrão de densidade uniforme nos pulmões (áreas escuras). Um padrão de maior densidade (áreas brancas) pode indicar anomalias como cardiomegalia (aumento do coração), consolidação ou infiltrações, que podem ser identificadas pelo sistema.

* **Identificação de Bordas e Quantificação:** Cada imagem contém estruturas anatômicas com bordas bem definidas, como as costelas, o coração e os pulmões. O sistema pode identificar essas bordas para delimitar e isolar as estruturas. Com essa delimitação, é possível quantificar e medir a anomalia. Usando os metadados da planilha, que fornecem a dimensão original e o espaçamento de pixels, o sistema pode converter essas medições visuais em unidades físicas, como centímetros, oferecendo ao médico dados precisos e clinicamente relevantes para o diagnóstico.

* **Apoio à Decisão e Relevância para a Saúde:** A capacidade de um sistema de análise visual de detectar e quantificar anomalias em imagens médicas tem um impacto significativo na área da saúde. Ao automatizar a identificação de padrões e a medição de estruturas, ele age como um auxiliar de diagnóstico, permitindo um processo mais rápido e preciso. Isso é especialmente importante em locais com poucos especialistas, onde a tecnologia pode democratizar o acesso a diagnósticos de alta qualidade, otimizando o fluxo de trabalho dos hospitais e, em última análise, melhorando os resultados para os pacientes.

- **Origem:** As imagens e os dados são parte do conjunto de dados acadêmico [**"ChestX-ray"**](https://nihcc.app.box.com/v/ChestXray-NIHCC/folder/36938765345), proveniente do National Institutes of Health Clinical Center (NIH) dos Estados Unidos.

---

### 📁 Estrutura de Pastas/Arquivos

```plaintext
├── docs/                        # Arquivos de texto e artigos científicos
├── data/                        # Datasets numéricos e visuais
└── README.md                  # Este arquivo
```

**Arquivos disponíveis no link:** [CardioIA - IATron](https://drive.google.com/drive/folders/1uwBayV-vaW_-nlxakiNc58MGRLO9M53y?usp=sharing)
 
### 📋 Licença e Bibliografia

Este projeto representa a atividade Capítulo 1 Fase 1 FIAP 2025.2 para o curso de Inteligência Artificial. Trata-se da estruturação de uma database para  análise e monitoramento de doenças cardiovasculares, que utiliza dados clínicos, exames de imagem e *insights* qualitativos para aprimorar a compreensão e o cuidado ao paciente.

O futuro sistema integrará múltiplas fontes de dados, incluindo informações clínicas de pacientes (pressão arterial, colesterol, histórico de saúde), imagens radiológicas de tórax e conhecimento extraído de artigos científicos sobre a experiência e adesão do paciente ao tratamento.

---

#### Fontes de Dados e Licenças

* **Licença do Projeto:** Este projeto segue o modelo de licença da FIAP e está licenciado sob **Attribution 4.0 International**. Para mais informações, consulte o [MODELO GIT FIAP](https://github.com/agodoi/template).


* **Chest X-ray Dataset:** Os dados de radiologia e as imagens de exemplo são provenientes do "ChestX-ray8" dataset, disponibilizado pelo National Institutes of Health (NIH) - Clinical Center. O uso desses dados é destinado a fins acadêmicos. Agradecemos ao NIH pela disponibilização deste recurso valioso. A política de uso do NIH deve ser consultada para qualquer aplicação comercial ou clínica.
    * **Referência Obrigatória:** Conforme a política do NIH, a citação do artigo original é obrigatória:
    > Wang, X., Peng, Y., Lu, L., Lu, Z., Bagheri, M., & Summers, R. M. (2017). ChestX-ray8: Hospital-scale Chest X-ray Database and Benchmarks on Weakly-Supervised Classification and Localization of Common Thorax Diseases. In 2017 IEEE Conference on Computer Vision and Pattern Recognition (CVPR) (pp. 3462-3471). [site](https://nihcc.app.box.com/v/ChestXray-NIHCC/folder/36938765345)

* **Artigos Científicos:** Os artigos utilizados sobre a experiência e adesão de pacientes ao tratamento foram extraídas dos seguintes artigos, e a utilização dessas informações deve ser devidamente citada:
    * **Artigo 1:** Martins, L. K., et al. (2024). Experiência dos sintomas em pessoas com insuficiência cardíaca no contexto da Teoria de Manejo dos Sintomas. Escola Anna Nery, 28, e20240022.  [acesso](https://www.scielo.br/j/ean/a/wvMhTMPC3ysxbpDkYTd3QzR/?format=html&lang=pt)
    * **Artigo 2:** (A ser completado com os detalhes do artigo de revisão integrativa.) [acesso](https://www.scielo.sa.cr/scielo.php?pid=S1409-45682023000200012&script=sci_arttext&utm_source=chatgpt.com)

* **Dados Clínicos Sintéticos:** O arquivo Dados_numericos.xlsx contém dados que, para os fins deste projeto, são tratados como anônimos e sintéticos. A origem desses dados é o gerador de pacientes SyntheaTM, um recurso open-source para pesquisa em saúde.
    * **Referência:** SyntheaTM. (2025). Synthetic Patient Generation. Disponível em: https://synthetichealth.github.io/synthea/