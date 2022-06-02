---
title: Implémentation d’un objet récepteur Conseiller
description: Un client peut implémenter son propre objet récepteur de conseils ou utiliser la fonction HrAllocAdviseSink, qui crée un objet récepteur de conseils avec une implémentation d’OnNotify.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 7461c4f6-7030-4ba2-ada4-26ebfbbfa001
ms.openlocfilehash: eb9dc35d866c5ae0cc599744e88c7038c748fab5
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828424"
---
# <a name="implementing-an-advise-sink-object"></a>Implémentation d’un objet récepteur Conseiller

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un client peut implémenter ses propres objets récepteurs de conseils ou utiliser une fonction utilitaire, [HrAllocAdviseSink](hrallocadvisesink.md). **HrAllocAdviseSink** crée un objet récepteur de conseils avec une implémentation **d’OnNotify** qui appelle une fonction de rappel. 
  
L’utilisation de **HrAllocAdviseSink** présente des avantages et des inconvénients. Il peut enregistrer le travail, mais il ne fournit aucun contrôle sur le comptage des références de l’objet récepteur de conseils qu’il crée. Par conséquent, les clients qui doivent contrôler soigneusement la mise en production de leur récepteur de conseils ou qui ont des interdépendances entre leur récepteur de conseils et un autre objet client doivent construire leur propre implémentation **IMAPIAdviseSink** et éviter d’utiliser **hrAllocAdviseSink** tout à fait. 
  
Un client qui implémente son propre récepteur de conseils doit en faire un objet indépendant qui n’est pas lié ou dépendant d’autres objets afin d’éliminer les complications potentielles dans le comptage des références et la libération d’objets. Toutefois, si vous devez implémenter votre récepteur de conseils dans le cadre d’un autre objet ou inclure un pointeur arrière vers un autre objet en tant que membre de données, il est recommandé de conserver deux nombres de références distincts : un pour l’objet référencé par le récepteur conseiller et un pour le récepteur de conseils. 
  
Lorsque le nombre de références de l’objet référencé tombe à zéro, toutes ses méthodes peuvent échouer et sa table virtuelle peut être détruite, mais la mémoire du récepteur de conseils doit rester intacte jusqu’à ce que le nombre de références tombe également à zéro. Cela signifie que la méthode **release** du récepteur de conseils doit décrémenter son nombre de références et terminer la destruction de l’objet lorsque ce nombre atteint zéro. Si deux nombres de références distincts ne sont pas conservés, il serait facile de détruire par inadvertance le récepteur de conseils dans le cadre du processus de **mise en production** de l’objet englobant. 
  
Les clients qui utilisent **HrAllocAdviseSink** pour implémenter un récepteur de conseils doivent également veiller à ne pas inclure leur fonction de rappel comme méthode dans un autre objet récepteur de conseils. Pour les clients C++, il est tentant de le faire et de passer  _ce_ pointeur en tant que paramètre. Il s’agit d’une stratégie dangereuse, car les clients libèrent généralement un objet lorsque son nombre de références atteint zéro. La libération de la mémoire de l’objet récepteur conseiller rendrait  _ce_ pointeur non valide. 
  
Selon le type d’événement et la source de conseil, votre méthode **OnNotify** peut gérer les événements de différentes manières. Le tableau suivant propose des suggestions sur la façon de gérer certains des événements standard. 
  
|**Type d’événement**|**Gestion dans OnNotify**|
|:-----|:-----|
|Objet déplacé  <br/> |Si le parent d’origine de l’objet déplacé est lié au nouveau parent, mettez à jour la vue commençant par le dossier ou le conteneur de carnet d’adresses le plus élevé dans la hiérarchie. Si les deux conteneurs parents ne sont pas liés, mettez à jour leurs deux vues. |
|Nouveau message  <br/> |Modifiez l’interface utilisateur pour informer l’utilisateur de l’arrivée d’un ou de plusieurs nouveaux messages. Placez le dossier de réception dans l’affichage actuel. |
|Erreur  <br/> |Pour tous les objets à l’exception de la session, consignez l’erreur si nécessaire et retournez-la. Pour l’objet de session, déconnectez-vous si possible. |
|Recherche terminée  <br/> |Aucun traitement n’est nécessaire. |
   
> [!NOTE]
> Les gestionnaires de notifications doivent être réentrants. 
  

