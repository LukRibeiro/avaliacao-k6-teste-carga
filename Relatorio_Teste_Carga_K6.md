# Relatório de Teste de Carga

## Objetivo 

Avaliar o comportamento de uma API pública sob carga de 100 usuários simultâneos, utilizando a ferramenta K6 integrada ao Grafana Cloud. 

## Ferramentas Utilizadas 

- K6 (via Grafana Cloud) 

- API pública: https://jsonplaceholder.typicode.com/posts 

- Script em JavaScript para configuração de carga 

- Dashboard de monitoramento do Grafana Cloud 

## Resultado

Métrica 

Valor 

Duração do Teste 

8 minutos 

Usuários Simultâneos (VUs) 

100 

Total de Requisições 

298 

Pico de Throughput (RPS) 

20.33 req/s 

p95 Response Time 

38 ms 

## Análise Técnica 

Durante o teste com 100 usuários simultâneos acessando o endpoint `https://jsonplaceholder.typicode.com/posts`, a API respondeu com excelente desempenho. O tempo de resposta no percentil 95 foi de apenas 38ms, e nenhuma falha HTTP foi registrada. A performance foi consistente, com throughput médio de 20.33 requisições por segundo. 
 
Observação: O número de usuários foi limitado a 100 devido à restrição do plano gratuito da K6 Cloud. O script é escalável e pode ser executado localmente com até 500 usuários. 

## Conclusão 

A API testada demonstrou estabilidade e desempenho satisfatório sob carga moderada. Recomenda-se esse tipo de teste regularmente para avaliar possíveis variações de performance em versões futuras do serviço. 