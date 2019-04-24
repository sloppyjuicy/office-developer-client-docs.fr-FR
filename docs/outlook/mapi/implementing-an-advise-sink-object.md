---
title: Implémentation d'un objet de récepteur de notifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7461c4f6-7030-4ba2-ada4-26ebfbbfa001
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ecaad65d28f74b843b86ca82dab9a833ade77363
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351099"
---
# <a name="implementing-an-advise-sink-object"></a>Implémentation d'un objet de récepteur de notifications

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un client peut implémenter ses propres objets de récepteur de notification ou utiliser une fonction utilitaire, [HrAllocAdviseSink](hrallocadvisesink.md). **HrAllocAdviseSink** crée un objet de récepteur de notifications avec une implémentation de **OnNotify** qui appelle une fonction de rappel. 
  
L'utilisation de **HrAllocAdviseSink**présente des avantages et des inconvénients. Elle peut enregistrer le travail, mais elle ne fournit aucun contrôle sur le décompte de référence de l'objet récepteur de notification qu'il crée. Par conséquent, les clients qui doivent contrôler soigneusement la version du récepteur de notification ou qui ont des interdépendances entre leur récepteur de notification et un autre objet client doivent créer leur propre implémentation **IMAPIAdviseSink** et éviter d'utiliser ** HrAllocAdviseSink** . 
  
Un client qui met en œuvre son propre récepteur de notification doit en faire un objet indépendant qui n'est pas lié à ou dépendant d'autres objets afin d'éviter toute complications potentielles dans le décompte de références et la version d'objet. Toutefois, si vous devez implémenter votre récepteur de notifications dans le cadre d'un autre objet ou inclure un pointeur vers un autre objet en tant que membre de données, il est recommandé de conserver deux compteurs de référence distincts: un pour l'objet référencé par le récepteur de notifications et un pour le récepteur de notifications. 
  
Lorsque le décompte de références de l'objet référencé est égal à zéro, toutes ses méthodes peuvent échouer et sa vtable peut être détruite, mais la mémoire pour le récepteur de notifications doit demeurer intacte jusqu'à ce que son nombre de références tombe également à zéro. Cela signifie que la méthode **Release** du récepteur de notification doit décrémenter son décompte de référence et finir de détruire l'objet lorsque ce nombre atteint zéro. Si deux décomptes de références distincts ne sont pas maintenus, il est facile de détruire accidentellement le récepteur de notifications dans le cadre du processus de **publication** de l'objet englobant. 
  
Les clients qui utilisent **HrAllocAdviseSink** pour implémenter un récepteur de notifications doivent être également vigilants pour ne pas inclure leur fonction de rappel en tant que méthode dans un autre objet de récepteur de notification. Pour les clients C++, il est tentant de le faire et de transmettre le pointeur _This_ en tant que paramètre. Il s'agit d'une stratégie dangereuse, car les clients libèrent généralement un objet lorsque son nombre de références atteint zéro. La libération de la mémoire pour l'objet récepteur de notification rend le pointeur _This_ non valide. 
  
Selon le type d'événement et la source de notification, votre méthode **OnNotify** peut gérer les événements de différentes manières. Le tableau suivant présente des suggestions de gestion de certains événements standard. 
  
|**Type d'événement**|**Gestion dans OnNotify**|
|:-----|:-----|
|Objet déplacé  <br/> |Si le parent d'origine de l'objet déplacé est lié au nouveau parent, mettez à jour l'affichage en commençant par le conteneur ou le conteneur du carnet d'adresses le plus haut dans la hiérarchie. Si les deux conteneurs parents ne sont pas liés, mettez à jour ces deux vues.  <br/> |
|Nouveau message  <br/> |Modifier l'interface utilisateur pour informer l'utilisateur de l'arrivée d'un ou plusieurs nouveaux messages. Placez le dossier de réception dans l'affichage actuel.  <br/> |
|Error  <br/> |Pour tous les objets à l'exception de la session, consignez l'erreur si nécessaire et renvoyez-la. Pour l'objet session, déconnectez-vous dans la mesure du possible.  <br/> |
|Recherche terminée  <br/> |Aucun traitement nécessaire.  <br/> |
   
> [!NOTE]
> Les gestionnaires de notification doivent être réentrants. 
  

