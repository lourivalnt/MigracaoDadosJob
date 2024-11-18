# Data Migration Project with Spring Batch

## 📋 Sumário
- [Sobre o Projeto](#sobre-o-projeto)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Pré-requisitos](#pré-requisitos)
- [Arquitetura do Projeto](#arquitetura-do-projeto)
- [Configuração do Ambiente](#configuração-do-ambiente)
- [Como Executar](#como-executar)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Personalização](#personalização)
- [Testes](#testes)
- [Contribuições](#contribuições)
- [Licença](#licença)

---

## 📌 Sobre o Projeto
Este projeto é uma aplicação **Java 21** que utiliza **Spring Batch** para realizar migração de dados entre diferentes sistemas. Ele foi desenvolvido para processar grandes volumes de dados de forma eficiente e escalável, garantindo integridade e consistência durante o processo de transferência.

### 🚀 O que foi implementado
Foi construído um **Job de migração de dados** utilizando **Spring Batch**, que abrange as seguintes funcionalidades:
- **Leitura de dados** de arquivos.
- **Escrita em banco de dados**.
- **Escrita em arquivos** para relatórios ou backups.
- **Escrita de registros inválidos** em arquivos separados para análise posterior.
- **Otimização do Job** para reduzir o tempo de execução, aproveitando ao máximo a performance e os recursos disponíveis.

Este projeto é ideal para cenários onde é necessário migrar, transformar ou carregar grandes volumes de dados de maneira eficiente e confiável.

---

## 🛠️ Tecnologias Utilizadas
- **Java 21**
- **Spring Boot 3.x**
- **Spring Batch**
- **Spring Data JPA**
- **H2 Database** (para testes)
- **PostgreSQL** (banco de dados de produção)
- **Lombok**
- **Maven**
- **JUnit 5** e **Mockito** (para testes unitários)
- **Docker** (para deploy em containers)

## 🔧 Pré-requisitos
Certifique-se de ter as seguintes ferramentas instaladas em sua máquina:
- **Java 21** (JDK)
- **Maven 3.9.x** ou superior
- **Docker** (opcional, para deploy em containers)
- **Git**

## 🏗️ Arquitetura do Projeto
A aplicação segue a arquitetura modularizada e orientada a tarefas (`job`) do Spring Batch:

- **Job**: Um processo de migração completo que pode incluir múltiplas etapas (steps).
- **Step**: Uma unidade de processamento que pode incluir leitura, processamento e escrita de dados.
- **Reader**: Lê dados da fonte (banco de dados, arquivos CSV, XML, etc.).
- **Processor**: Realiza transformações ou validações nos dados lidos.
- **Writer**: Escreve os dados transformados no destino.

---

## ⚙️ Configuração do Ambiente

### 1. Clonar o Repositório
```bash
git clone https://github.com/lourivalnt/MigracaoDadosJob.git
cd MigracaoDadosJob
