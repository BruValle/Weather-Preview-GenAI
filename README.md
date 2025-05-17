# 🌧️ Monitoramento Simplificado de Risco de Alagamento 🚨

Um módulo inicial de projeto, explorando a previsão meteorológica como indicador de risco de alagamento.

## 😥 Contexto e Motivação

Os recentes e devastadores eventos no **Rio Grande do Sul** em 2025 nos mostraram de forma dolorosa a importância vital do monitoramento e da preparação diante de fenômenos climáticos extremos e seus impactos hídricos. A resiliência das comunidades e a capacidade de resposta a desastres estão diretamente ligadas à qualidade e à antecedência das informações disponíveis. 🙏💔

Inspirado por essa realidade e pela necessidade de contribuir para soluções, este projeto da **Alura** me fez explorar o desenvolvimento de ferramentas de monitoramento e alerta para auxiliar na gestão de riscos associados a chuvas intensas e possíveis alagamentos.

## ✨ Visão Geral do meu TCC envolvendo o Projeto Alura

A visão completa do meu projeto de TCC envolve a criação de um sistema mais abrangente que combine **previsão meteorológica** com **monitoramento em tempo real do nível da água dos rios**. A ideia é integrar um sensor de nível para coletar dados diretos dos corpos d'água. 💡

Com base na análise desses dados (previsão de chuva + nível do rio), o sistema teria o potencial de acionar **bombas de drenagem de forma automática**, otimizando a resposta em situações críticas, como as enfrentadas no Rio Grande do Sul. ⚙️

## 💻 Este Projeto da Alura (O Script Atual)

O repositório que você está vendo agora representa uma etapa fundamental e um **módulo inicial** desse projeto de TCC maior. Este script Python foca especificamente na obtenção e análise da previsão meteorológica como um indicador preliminar de risco. 🔍📊

Ele utiliza a API do **OpenWeatherMap** para buscar dados de chuva e condições do tempo para uma cidade específica e aplica uma lógica simplificada baseada em limiares de precipitação para identificar períodos com potencial para chuva intensa nos próximos 5 dias.

Além disso, integra a API do **Google Gemini** para gerar um resumo textual da análise, tornando a informação mais acessível.

Este script é, portanto, a **base** para a parte de "previsão e início de preparação" do projeto maior. Ele não inclui a interação com sensores de nível ou o controle de bombas, que são objetivos futuros do TCC.

---

## 👇 Como Usar

Este guia rápido explica como configurar e executar o script atual.

### Pré-requisitos

Certifique-se de ter Python instalado em seu sistema.

### Configuração e Execução 🛠️

Siga os passos abaixo para colocar o script em funcionamento:

1.  **Clone o repositório:**
    ```bash
    git clone [link_do_seu_repositorio]
    ```

2.  **Instale as dependências:**
    ```bash
    pip install requests google-generativeai
    ```

3.  **Obtenha suas chaves de API:**
    * Crie uma conta no [OpenWeatherMap](https://openweathermap.org/) e obtenha sua **API Key**.
    * Obtenha uma **API Key** para o Google Gemini (via [Google AI Studio](https://aistudio.google.com/) ou [Google Cloud Platform](https://cloud.google.com/)).

4.  **Configure suas chaves:**
    É altamente recomendado usar variáveis de ambiente ou o gerenciador de segredos do Google Colab para armazenar suas chaves de API de forma segura.
    * **Se estiver usando Google Colab:** Configure os segredos `Weather_API` (para OpenWeatherMap) e `GOOGLE_API_KEY` (para Gemini) no gerenciador de segredos.
    * **Se não estiver usando Colab:** Adapte o código para carregar as chaves de variáveis de ambiente (ex: `import os`, `os.getenv('NOME_DA_VARIAVEL')`).

5.  **Execute o script:**
    ```bash
    python seu_script.py
    ```

6.  **Ajuste a cidade:**
    Modifique a variável `CIDADE` no script para a cidade desejada. Utilize o formato `"Nome da Cidade,Código do País"` (ex: `"London,uk"`).

7.  **Ajuste os limiares:**
    Os limiares de chuva (`LIMIAR_CHUVA_1H_MM`, `LIMIAR
