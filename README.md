# 📧 Neurolake Email Templates

**Repositório de templates de emails padronizados para o Neurolake.**

---

## 📂 Estrutura dos Templates

Os templates são arquivos **HTML** prontos para uso.  
Você pode utilizar o **template default** substituindo os marcadores abaixo pelo conteúdo desejado:

| Marcador     | Descrição                            |
|--------------|----------------------------------------|
| `#title#`    | Título do e-mail                      |
| `#content#`  | Conteúdo textual do e-mail            |
| `#@#`        | Link que será usado no botão          |
| `#button#`   | Texto que aparecerá no botão          |

## ⚙️ Como Usar

É possível fazer a substituição diretamente no arquivo HTML ou por meio de um método na linguagem utilizada no seu projeto, transformando o conteúdo do template em uma string e usando substituições simples.  

### 🐍 Exemplo em Python:

```python
# Carrega o conteúdo do template como string
with open('templates/default.html', 'r') as file:
    email_template = file.read()

# Substitui os marcadores pelos valores reais
email_final = (
    email_template
    .replace('#title#', 'Redefinição de Senha')
    .replace('#content#', 'Clique no botão abaixo para redefinir sua senha.')
    .replace('#@#', 'https://example.com/reset-password')
    .replace('#button#', 'Redefinir Senha')
)
