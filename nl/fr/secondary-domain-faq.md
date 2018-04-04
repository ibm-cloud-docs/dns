---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-06"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# FAQ sur le domaine secondaire 

## Quels serveurs DNS IBM Cloud répondent pour mes domaines secondaires ?

Serveurs DNS faisant autorité, compatibles IPv6, Anycast d'IBM Cloud : 

 * ns1.softlayer.com
 * ns2.softlayer.com

## D'où proviennent les transferts de zone ? 

Les transferts de votre domaine secondaire proviennent de l'une des quatre adresses IP suivantes : 

  * 66.228.118.67
  * 67.228.119.235
  * 208.43.119.235
  * 12.96.161.249

## Après le transfert d'un domaine, combien de temps faut-il pour que ce domaine et les modifications apparaissent ? 

Le domaine et les éventuelles modifications sont visibles sur les serveurs DNS IBM Cloud immédiatement après la fin du transfert. En raison de la nature de la mise en cache et de la propagation sur DNS, il peut se produire un certain temps avant que ces modifications soient visibles sur d'autres serveurs DNS.   

## Les notifications de mise à jour de zone sont-elles prises en charge ? 

Les notifications sont pas prises en charge pour le moment. 

## Dans quelle mesure le bouton Transférer maintenant a-t-il une action immédiate ? 

Lorsque vous cliquez sur le bouton Transférer maintenant, le domaine est transféré au début de la minute suivante. 

## Un maître peut-il être configuré sur le réseau privé ou doit-il passer par le réseau public ? 

Pas pour le moment. Toutes les demandes AXFR sont effectuées sur le réseau public. 

## Les esclaves sont-ils supprimés après un certain nombre de jours pendant lesquels le maître est indisponible ? 

Vous cessez de tenter de transférer un domaine si son maître est en panne ou incorrectement configuré pendant une période prolongée. Le portail fournit des commentaires aux clients (onglet Messages d'erreur) et une méthode de réactivation d'un domaine (onglet Transfert de zone manuel) en cas de problèmes de transfert de la zone, et le domaine est désactivé en conséquence. 

## Est-ce que 1 minute est la fréquence de transfert la plus basse ? 

Oui.

## Si la fréquence est réglée sur 1920 minutes, puis revient à 10, les 1920 minutes doivent-elles expirer avant que la nouvelle fréquence entre en vigueur ? 

Non. Le système calcule la file d'attente du retransfert en ajoutant la fréquence à l'heure de la dernière tentative de transfert. Donc, si vous avez défini la fréquence sur 1920 et l'avez modifiée ensuite sur 10 minutes, tant que vous n'avez pas effectué de nouvelle tentative de transfert depuis au moins 10 minutes, vous pouvez réessayer immédiatement, puis faire une nouvelle tentative toutes les 10 minutes par la suite. 
