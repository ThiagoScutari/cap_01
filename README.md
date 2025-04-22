# FIAP - Faculdade de Informática e Administração Paulista

<p align="center">
  <a href="https://www.fiap.com.br/">
    <img src="logo-fiap.png" alt="FIAP - Faculdade de Informática e Administração Paulista" width="40%">
  </a>
</p>

<br>

# 🌿 Sistema de Monitoramento e Otimização Agrícola - FarmTech Solutions

## 📌 Grupo: 81

## 👨‍🎓 Integrantes:
- Thiago Scutari da Silva - RM562831 | thiago.silva@amctextil.com.br
- Marcos Fernandes - RM564998 | mareligumarcos@gmail.com
- Henrique Ribeiro Siqueira - RM565044 | henrique.ribeiro1201@gmail.com
- Victor Emmanuel Lucioli Barbosa - RM562884 | victorluciolibarbosa.2004@gmail.com
- Mariana Cavalcante Oliveira - RM561678 | mari.kvalcant@gmail.com

## 👩‍🏫 Professores:

### Tutor  
- Leonardo Ruiz Orabona

### Coordenador  
- Andre Godoi Chiovato

---

## 📜 Descrição

Este projeto foi desenvolvido com o objetivo de atender a uma demanda real do agronegócio moderno: a **monitoria de culturas agrícolas com sensores** e a aplicação controlada de recursos como **água e nutrientes (NPK)**.  

A solução envolve a modelagem de um banco de dados relacional que permita:

- Armazenar leituras de sensores em tempo real (umidade, pH, nutrientes)
- Registrar aplicações de água com data/hora e volume
- Otimizar o uso de recursos com base em dados históricos
- Gerar relatórios para suporte à tomada de decisão

O modelo foi construído com base nos conceitos de MER e DER utilizando o **Oracle SQL Developer Data Modeler**, respeitando os princípios de integridade referencial, normalização e relacionamentos do tipo 1:N.

---

## 🧩 Entidades e Atributos (MER)

- **Cultura**
  - `id_cultura` (PK)
  - `nome`
  - `area_hectares`

- **Sensor**
  - `id_sensor` (PK)
  - `tipo` *(S1 = Umidade, S2 = pH, S3 = Nutrientes NPK)*
  - `descricao`

- **Leitura_Sensor**
  - `id_leitura` (PK)
  - `id_sensor` (FK)
  - `id_cultura` (FK)
  - `data_hora`
  - `valor`

- **Aplicacao_Agua**
  - `id_aplicacao` (PK)
  - `id_cultura` (FK)
  - `data_hora`
  - `quantidade_litros`

---

## 🔗 Relacionamentos

- Cultura 1:N Leitura_Sensor
- Sensor 1:N Leitura_Sensor
- Cultura 1:N Aplicacao_Agua

---

## 🗃 Arquivos entregues no repositório

```
cap_01/
├── modelo.dmd                  # Modelo criado no Oracle SQL Developer Data Modeler
├── DER.png                    # Diagrama visual do modelo relacional
├── README.md                  # Documentação explicativa do MER
└── exemplos_consultas.sql     # Exemplos de consultas SQL (opcional)
```

---

## 🚀 Objetivos e Benefícios do Modelo

- Obter métricas como variação de pH ao longo do tempo
- Calcular a quantidade de água aplicada por mês por cultura
- Auxiliar decisões sobre irrigação e adubação com base em histórico
- Integrar sensores diversos com rastreabilidade de dados

---

## 📋 Licença

Este projeto foi desenvolvido como parte do curso da FIAP e está licenciado sob [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/?ref=chooser-v1).

---

[LinkedIn](https://www.linkedin.com/in/thiago-scutari-2aa0a097)  
[GitHub](https://github.com/ThiagoScutari)