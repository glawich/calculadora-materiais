# 🤖 INSTRUÇÕES PARA COREY - Calculadora de Materiais

**Arquivo Principal**: `CALCULADORA_MATERIAIS.html`  
**Localização**: `C:\Users\GabrielLawich\Documents\GitHub\calculadora-materiais\`

---

## 📋 **PROTOCOLO: Quando Gabriel pedir mudança na calculadora**

### **SEMPRE:**
1. ✅ Editar **DIRETO** o arquivo em: `CALCULADORA_MATERIAIS.html`
2. ✅ Localizar a seção: `<option value=...>`
3. ✅ Fazer a mudança solicitada
4. ✅ **NÃO** copiar/colar, **NÃO** criar arquivos intermediários
5. ✅ Depois de editar, informar: *"Pronto! Você só precisa clicar Commit no GitHub Desktop"*

### **NUNCA:**
- ❌ Pedir para Gabriel copiar/colar arquivos
- ❌ Editar arquivo em outro lugar
- ❌ Fazer o commit (Gabriel clica)
- ❌ Deixar trabalho manual pro Gabriel

---

## 🎯 **EXEMPLOS DE FLUXO**

### **Exemplo 1: Adicionar novo material**

**Gabriel**: "Quero adicionar Nylon (densidade 1,14 g/cm³, NCM 3916.90.90)"

**Corey**:
1. Abre `CALCULADORA_MATERIAIS.html`
2. Localiza seção `<option value=`
3. Adiciona: `<option value="nylon|1.14|3916.90.90">Nylon (1,14 g/cm³) - NCM 3916.90.90</option>`
4. Salva o arquivo
5. Responde: "✅ **Pronto!** Nylon adicionado. Você só precisa clicar **Commit to main** no GitHub Desktop com a mensagem: 'Adicionar Nylon'"

---

### **Exemplo 2: Mudar densidades ou NCM**

**Gabriel**: "Muda a densidade do Alumínio para 2,72"

**Corey**:
1. Abre `CALCULADORA_MATERIAIS.html`
2. Localiza: `aluminio|2.70|`
3. Muda para: `aluminio|2.72|`
4. Salva
5. Responde: "✅ **Pronto!** Alumínio atualizado para 2,72 g/cm³. Clique **Commit** com mensagem: 'Atualizar densidade do Alumínio'"

---

### **Exemplo 3: Mudanças mais complexas**

**Gabriel**: "Quero que a tabela mostre também o custo por peça"

**Corey**:
1. Abre `CALCULADORA_MATERIAIS.html`
2. Localiza a tabela (`<table>`)
3. Adiciona coluna nova
4. Atualiza JavaScript (função `renderizarTabela()`)
5. Testa mentalmente se faz sentido
6. Salva
7. Responde: "✅ **Pronto!** Coluna 'Custo por Peça' adicionada. Teste a calculadora e depois clique **Commit** com: 'Adicionar coluna de custo por peça'"

---

## 📂 **Estrutura do arquivo (para referência)**

```html
<!-- SEÇÃO 1: Seleção de Material -->
<select id="material" onchange="atualizarNCM()">
    <option value="material|densidade|ncm">Nome (densidade) - NCM XXXXX</option>
    <!-- ADICIONE NOVOS MATERIAIS AQUI -->
</select>

<!-- SEÇÃO 2: JavaScript (funções de cálculo) -->
<script>
    function adicionarMaterial() { ... }
    function renderizarTabela() { ... }
    function atualizarResumo() { ... }
</script>
```

---

## 🔍 **Localização de coisas comuns**

| O que? | Onde? | Linha aprox. |
|---|---|---|
| **Lista de materiais** | `<select id="material">` | ~480 |
| **Função de cálculo de peso** | `function calcularPeso()` | ~860 |
| **Função renderizar tabela** | `function renderizarTabela()` | ~930 |
| **Função exportar CSV** | `function exportarCSV()` | ~1020 |

---

## ✅ **Checklist antes de informar "Pronto"**

- [ ] Arquivo editado DIRETO (sem cópias)
- [ ] Sintaxe HTML/JavaScript está correta
- [ ] Mudança faz sentido para o objetivo
- [ ] Informei Gabriel sobre o próximo passo (Commit)
- [ ] Gabriel só precisa clicar, nada mais

---

## 💬 **Resposta padrão ao terminar**

```
✅ **Pronto!** [Descrição da mudança feita]

Próximo passo:
1. Abra GitHub Desktop
2. Você verá a mudança listada
3. Clique: **Commit to main**
4. Mensagem: "[Sua mensagem aqui]"
5. Clique: **Push origin**
6. Pronto! 🚀
```

---

**Este é o protocolo. Seguir à risca!** 🎯
