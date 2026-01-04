# 🐍 Projeto de Testes com Pytest

Este repositório reúne uma série de exercícios práticos para aprender e aplicar conceitos de **testes automatizados em Python** utilizando o framework **Pytest**.  
O objetivo é praticar a criação de fixtures, uso de marcadores, parametrização de testes e utilização de fixtures builtin.

---

## 📚 Exercícios

### 1. Crie uma fixture
- **Arquivo:** `tests/conftest.py`
- **Tarefa:** Criar a fixture `custom_fixture` com escopo de módulo ou sessão.  
- **Retorno esperado:** uma lista Python com os números de 1 a 10.  

---

### 2. Use um marcador
- **Arquivo:** `tests/marker_test.py`
- **Tarefa:** Criar a função `test_dependency_mark` marcada com `@pytest.mark.dependency`.  
- **Resultado esperado:** o teste deve sempre passar (`assert True`).  

---

### 3. Crie testes parametrizados
- **Arquivo:** `tests/parametrized_test.py`
- **Tarefa:** Criar a função `test_converter` parametrizada para testar `src.hex_converter.hexadecimal_to_decimal`.  
- **Parâmetros:**
  - `"8" → 8`
  - `"9" → 9`
  - `"a" → 10`
  - `"b" → 11`
  - `"c" → 12`
  - `"e" → 14`
  - `"f" → 15`

---

### 4. Use fixtures builtin — monkeypatch
- **Arquivo:** `tests/built_in_fixtures_test.py`
- **Tarefa:** Criar `test_monkeypatch` usando a fixture `monkeypatch`.  
- **Objetivo:** validar que `src.hex_converter.main` retorna `10` quando a entrada simulada é `"a"`.  

---

### 5. Use fixtures builtin — capsys
- **Arquivo:** `tests/built_in_fixtures_test.py`
- **Tarefa:** Criar `test_capsys` usando a fixture `capsys`.  
- **Objetivo:** validar que `print_hexadecimal_to_decimal("a")` imprime `"10\n"` na saída padrão e nada na saída de erro.  

---

### 6. Use fixtures builtin — tmp_path
- **Arquivo:** `tests/built_in_fixtures_test.py`
- **Tarefa:** Criar `test_tmp_path` usando a fixture `tmp_path`.  
- **Objetivo:** criar um arquivo temporário `output.txt`, passar esse caminho para `write_hexadecimal_to_decimal("a", output_path)` e verificar que o conteúdo é `"10"`.  

---

