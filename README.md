# Automação de Sistemas com Python

Este projeto demonstra como automatizar tarefas do dia a dia utilizando **Python** e bibliotecas como `pyautogui`, `pyperclip` e `pandas`.

O fluxo cobre desde abrir navegadores, exportar relatórios, calcular indicadores de vendas até o envio automático de e-mails para a diretoria.

---

## Fluxo do Projeto

1. **Abrir o navegador e acessar o Google Drive**
   - O código utiliza `pyautogui` para abrir o Chrome e navegar até a pasta compartilhada no Google Drive.

2. **Exportar o relatório**
   - A automação localiza a pasta e exporta o arquivo desejado.

3. **Calcular indicadores**
   - Com `pandas`, o relatório exportado é processado para calcular:
     - **Faturamento Total**
     - **Quantidade Total de Produtos**

4. **Enviar e-mail automático**
   - Via automação de interface, o Gmail é aberto, o destinatário é definido e o corpo do e-mail com os indicadores é colado e enviado automaticamente.

5. **Utilitário extra**
   - Um código auxiliar permite capturar a posição atual do mouse na tela (`pyautogui.position()`), útil para ajustar cliques nos pontos corretos.

---

## Bibliotecas Utilizadas

- `pyautogui` → Automação de mouse e teclado
- `time` → Gerenciamento de atrasos
- `pyperclip` → Manipulação da área de transferência (copiar/colar textos)
- `pandas` → Manipulação e análise de planilhas Excel

---

##  Estrutura

```
.
├── automacao.ipynb                # Notebook original
├── README_Automacao_Python.md     # Este README
```

---

## ⚙️ Como Executar

1. Crie um ambiente virtual (opcional, mas recomendado):
   ```bash
   python -m venv .venv
   source .venv/bin/activate   # Linux/Mac
   .venv\Scripts\activate    # Windows
   ```

2. Instale as dependências necessárias:
   ```bash
   pip install pyautogui pyperclip pandas openpyxl
   ```

3. Execute o notebook no Jupyter:
   ```bash
   jupyter notebook automacao.ipynb
   ```

---

##  Observações Importantes

- Os cliques (`pyautogui.click(x, y)`) utilizam **coordenadas fixas**, que variam de computador para computador.  
  ➝ Use o trecho `pyautogui.position()` para capturar as posições corretas da sua tela.

- É necessário ter o **Google Chrome** instalado e acesso ao **Google Drive** e ao **Gmail** da empresa.

- O arquivo `Vendas - Dez.xlsx` deve estar disponível no caminho especificado no notebook.

---

---

## 📜 Licença

Este projeto pode ser utilizado para fins de estudo e adaptação em ambientes corporativos. Defina aqui a licença de sua preferência (ex.: MIT).

