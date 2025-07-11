﻿# 📝 Sistema de Cadastro de Nomes em Python com Tkinter + SQLite

Este é um projeto simples desenvolvido em Python que permite ao usuário cadastrar nomes por meio de uma interface gráfica (GUI) feita com Tkinter, armazenando esses nomes em um banco de dados local SQLite.

Todo o código está **unificado em um único arquivo (`app.py`)** para facilitar o uso, o estudo e a organização do projeto.

---

## 📌 Objetivo do Projeto

O objetivo é demonstrar a integração entre:
- Uma **interface gráfica amigável** com o Tkinter.
- Um **banco de dados leve** (SQLite).
- Uma **estrutura simples e funcional** de aplicação Python.

---

## 🔧 Funcionalidades

- ✅ Cadastro de nomes via formulário
- ✅ Armazenamento local usando SQLite
- ✅ Mensagens de sucesso ou erro
- ✅ Banco criado automaticamente ao iniciar o sistema

---

## 💻 Estrutura Interna do Código

### 📂 `Backend` — Banco de Dados com SQLite

A função `initDB()` é responsável por criar o banco de dados `nomes.db` e a tabela `pessoas`, caso ainda não existam.

```python
def initDB():
    conexao = sqlite3.connect("nomes.db")
    cursor = conexao.cursor()
    cursor.execute("""
        CREATE TABLE IF NOT EXISTS pessoas (
            id INTEGER PRIMARY KEY AUTOINCREMENT,
            nome TEXT NOT NULL
        )
    """)
    conexao.commit()
    conexao.close()

# Escrito e Codificado por: Nicolas Ubaldo Moreira.


