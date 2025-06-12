
# Avaliação Prática – Teste de Carga com K6

Este repositório apresenta a implementação de um teste automatizado de carga utilizando a ferramenta [K6](https://k6.io/), com execução realizada por meio do K6 Cloud (Grafana). O objetivo é validar o desempenho de uma API pública sob uma carga definida de usuários simultâneos.

---

## Objetivo

Avaliar a performance e a estabilidade de uma API pública durante um período contínuo de 5 minutos, com 100 usuários virtuais simultâneos. Ao final da execução, métricas como tempo de resposta, taxa de requisições e falhas foram analisadas.

---

## Ferramentas Utilizadas

* [K6](https://k6.io/) (execução via K6 Cloud / Grafana)
* API utilizada: `https://jsonplaceholder.typicode.com/posts`
* Script de carga desenvolvido em JavaScript
* Dashboard integrado ao K6 Cloud (Grafana)
* Git e GitHub para versionamento

---

## Script de Teste

O script de teste encontra-se no arquivo abaixo e simula o comportamento dos usuários virtuais:

[`teste-carga.js`](./teste-carga.js)

---

## Evidências da Execução

Os gráficos abaixo foram extraídos do dashboard da K6 após a execução do teste:

### Desempenho – Tempo de Resposta

![Response Time](./evidencias/grafico-response-time.png)

### Visão Geral – Taxa de Requisições

![Request Rate](./evidencias/grafico-request-rate.png)

---

## Conclusão

A API avaliada demonstrou estabilidade durante o teste com 100 usuários simultâneos. O tempo de resposta no percentil 95 (p95) manteve-se em aproximadamente **38ms**, sem ocorrência de erros HTTP.

> Observação: o teste foi executado com 100 usuários virtuais devido à limitação do plano gratuito da K6 Cloud. O mesmo script é escalável e pode ser executado com até 500 usuários em ambiente local.

