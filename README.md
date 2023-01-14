# Dimensionamento e Análise de uma Frota de Linha de Ônibus
"Sizing and Analyzing a Bus Line Fleet"

Rotina de cálculo simples para dimensionar a frota para uma linha de transporte e analisar alguns parâmetros de qualidade da linha

Exemplo:
```
# ----------------------------------Exemplo-------------------------------------
# Demandas nas seções - pax/h
P = [100,220,323,445,462,480,415,329,284,139]
# Folga - decimal
f = 0.1
# Capacidade - pax/veic
C = 80
# Tempo de ciclo (calculado com a velocidade comercial) - min
T = 120

# Cálculo da frota
F = MinFleetBusLine(P=max(P),f=f,C=C,T=T,round_up=True)

# Análise da frota
F,H,Q,P = AnalysisFleetBusLine(F=F,T=T,C=C,report=True)
```
Resultado:

```
Frota [veic]: 14
Headways entre veículos [min/veic]: 8.571428571428571
Fluxos de vianges [viagens/h]: 7.0
Capacidade máxima na seção crítica [pax/h]: 560.0
```
