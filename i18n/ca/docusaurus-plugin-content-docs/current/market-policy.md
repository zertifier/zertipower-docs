---
title: "Polítiques d'accés al mercat (policy.json)"
sidebar_label: "Polítiques (policy.json)"
---

# Polítiques d'accés al mercat (policy.json)

Als mercats de dades i de serveis (Ocean), cada actiu pot definir les seves regles d'ús mitjançant polítiques declaratives (p. ex., `policy.json`). Aquestes polítiques determinen qui pot comprar/consumir, sota quines condicions i amb quin nivell d'accés.

Què es pot expressar
- Accés granular: camps, columnes o rangs temporals específics.
- Restriccions de propòsit: recerca, ús comercial, entrenament de models, etc.
- Finestres de temps i quotes: nombre d'execucions, durada, caducitat.
- Requisits d'identitat i conformitat: VCs mínimes, rols, jurisdiccions.

Flexibilitat operativa
- Canvis sense redeploy: actualitzar regles sense modificar el dataset ni l'algoritme.
- Auditoria: les decisions d'autorització i els consums queden registrats.
- Delegació: el propietari pot delegar la gestió de polítiques a un gestor de confiança.

Al nostre espai de dades, policy.json s'aplica tant a datasets (lectura/compute) com a algoritmes (qui pot executar i amb quins paràmetres), habilitant models de negoci “pagament per ús” i “subscripció” respectant la sobirania de la dada.
