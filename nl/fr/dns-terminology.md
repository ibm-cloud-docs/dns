---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Terminologie DNS

## Mise en cache et durée de vie 

En raison du volume considérable de requêtes générées par un système tel que DNS, les concepteurs ont fourni un mécanisme permettant de réduire la charge sur chaque serveur DNS, comme suit :  

Lorsqu'un programme de résolution DNS (c'est-à-dire un client) reçoit une réponse DNS, il met en cache cette réponse pendant une période de temps donnée, appelée durée de vie. La valeur de durée de vie est définie par l'administrateur du serveur DNS qui distribue la réponse. Lorsqu'une réponse arrive dans le cache, le programme de résolution consulte sa réponse mise en cache (stockée). Ce n'est que lorsque la durée de vie arrive à expiration (ou lorsqu'un administrateur efface manuellement la réponse dans la mémoire du programme de résolution) que le programme de résolution contacte le serveur DNS pour lui demander ces mêmes informations. 

## Paramètres d'enregistrement Start of Authority (SOA)

Généralement, la durée de vie est spécifiée dans l'enregistrement Start of Authority (SOA). Les paramètres SOA sont les suivants : 

### Série 

Numéro de révision de ce fichier de zone. Incrémentez ce nombre chaque fois que le fichier de zone est modifié afin que les modifications soient distribuées à tous les serveurs DNS secondaires. 

### Actualiser 

Durée en secondes pendant laquelle un serveur de noms secondaire doit patienter pour rechercher une nouvelle copie d'une zone DNS à partir du serveur de noms principal du domaine. Si un fichier de zone a été modifié, le serveur DNS secondaire met à jour sa copie de la zone pour la faire correspondre à la zone du serveur DNS principal. 

### Réessayer 

Durée en secondes pendant laquelle le serveur (ou les serveurs) de noms principal d'un domaine doit patienter si une tentative d'actualisation par un serveur de noms secondaire a échoué avant de tenter à nouveau d'actualiser la zone d'un domaine avec ce serveur de noms secondaire. 

### Expirer

Durée en secondes pendant laquelle un serveur (ou des serveurs) de noms secondaire conserve une zone avant qu'elle ne soit considérée comme faisant autorité. 

### Minimum

Durée en secondes pendant laquelle les enregistrements de ressources d'un domaine sont valides. Egalement nommée durée de vie minimale, elle peut être remplacée par la durée de vie d'un enregistrement de ressource individuel. 

### Durée de vie (TTL)

Durée en secondes de mise en cache locale d'un nom de domaine avant son expiration et son renvoi vers les serveurs de noms faisant autorité pour actualisation de ses informations. 
