# Vazao-de-hidreletrica
Script que compila a vazão mensal de hidrelétricas para cada submercado  da diferentes regiões do país

ECMWF
import pandas as pd
tabela = pd.read_excel("ecmwfvazao.xlsx")
display(tabela)

#As ENAs e as semanas foram nomeadas em a,b,c,d,e ao invés de 1,2,3,4,5 para melhor compilação do script
tabela["enaa"]= tabela["sema"]* tabela["produtibilidade"]
tabela["enab"]= tabela["semb"]* tabela["produtibilidade"]
tabela["enac"]= tabela["semc"]* tabela["produtibilidade"]
tabela["enad"]= tabela["semd"]* tabela["produtibilidade"]
tabela["enae"]= tabela["seme"]* tabela["produtibilidade"]
tabela["mlt"]=tabela["enamediamensal"]/tabela["mltjun"]
a = 3*tabela["enaa"]+7*tabela["enab"]+7*tabela["enac"]+7*tabela["enad"]+6*tabela["enae"]
tabela["enamediamensal"]=a/30
tabela.to_excel("ecmwf2.xlsx",index=False)

GEFS


import pandas as pd
tabela = pd.read_excel("gefsvazao.xlsx")
display(tabela)

#As ENAs e as semanas foram nomeadas em a,b,c,d,e ao invés de 1,2,3,4,5 para melhor compilação do script
tabela["enaa"]= tabela["sema"]* tabela["produtibilidade"]
tabela["enab"]= tabela["semb"]* tabela["produtibilidade"]
tabela["enac"]= tabela["semc"]* tabela["produtibilidade"]
tabela["enad"]= tabela["semd"]* tabela["produtibilidade"]
tabela["enae"]= tabela["seme"]* tabela["produtibilidade"]
a = 3*tabela["enaa"]+7*tabela["enab"]+7*tabela["enac"]+7*tabela["enad"]+6*tabela["enae"]
tabela["enamediamensal"]=a/30
tabela["mlt"]=tabela["enamediamensal"]/tabela["mltjun"]
tabela.to_excel("gefs2.xlsx",index=False)


PRECZERO

import pandas as pd
tabela = pd.read_excel("preczerovazao.xlsx")
display(tabela)


#As ENAs e as semanas foram nomeadas em a,b,c,d,e ao invés de 1,2,3,4,5 para melhor compilação do script
tabela["enaa"]= tabela["sema"]* tabela["produtibilidade"]
tabela["enab"]= tabela["semb"]* tabela["produtibilidade"]
tabela["enac"]= tabela["semc"]* tabela["produtibilidade"]
tabela["enad"]= tabela["semd"]* tabela["produtibilidade"]
tabela["enae"]= tabela["seme"]* tabela["produtibilidade"]
a = 3*tabela["enaa"]+7*tabela["enab"]+7*tabela["enac"]+7*tabela["enad"]+6*tabela["enae"]
tabela["enamediamensal"]=a/30
tabela["mlt"]=tabela["enamediamensal"]/tabela["mltjun"]
tabela.to_excel("preczero2.xlsx",index=False)

ONS

import pandas as pd
tabela = pd.read_excel("onsvazao.xlsx")
display(tabela)

#As ENAs e as semanas foram nomeadas em a,b,c,d,e ao invés de 1,2,3,4,5 para melhor compilação do script
tabela["enaa"]= tabela["sema"]* tabela["produtibilidade"]
tabela["enab"]= tabela["semb"]* tabela["produtibilidade"]
tabela["enac"]= tabela["semc"]* tabela["produtibilidade"]
tabela["enad"]= tabela["semd"]* tabela["produtibilidade"]
tabela["enae"]= tabela["seme"]* tabela["produtibilidade"]
a = 3*tabela["enaa"]+7*tabela["enab"]+7*tabela["enac"]+7*tabela["enad"]+6*tabela["enae"]
tabela["enamediamensal"]=a/30
tabela["mlt"]=tabela["enamediamensal"]/tabela["mltjun"]
tabela.to_excel("ons2.xlsx",index=False)

TOK

import pandas as pd
tabela = pd.read_excel("tokvazao.xlsx")
display(tabela)


#As ENAs e as semanas foram nomeadas em a,b,c,d,e ao invés de 1,2,3,4,5 para melhor compilação do script
tabela["enaa"]= tabela["sema"]* tabela["produtibilidade"]
tabela["enab"]= tabela["semb"]* tabela["produtibilidade"]
tabela["enac"]= tabela["semc"]* tabela["produtibilidade"]
tabela["enad"]= tabela["semd"]* tabela["produtibilidade"]
tabela["enae"]= tabela["seme"]* tabela["produtibilidade"]
a = 3*tabela["enaa"]+7*tabela["enab"]+7*tabela["enac"]+7*tabela["enad"]+6*tabela["enae"]
tabela["enamediamensal"]=a/30
tabela["mlt"]=tabela["enamediamensal"]/tabela["mltjun"]
tabela.to_excel("tok2.xlsx",index=False)
