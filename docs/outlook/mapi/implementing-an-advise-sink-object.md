---
title: Mise en œuvre d’un objet de sink de conseil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 7461c4f6-7030-4ba2-ada4-26ebfbbfa001
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 278a259f59fbec565371b174bed36a440631ac58
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62788226"
---
# <a name="implementing-an-advise-sink-object"></a>Mise en œuvre d’un objet de sink de conseil

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un client peut implémenter ses propres objets de sink de conseil ou utiliser une fonction utilitaire, [HrAllocAdviseSink](hrallocadvisesink.md). **HrAllocAdviseSink** crée un objet de sink de conseil avec une implémentation **de OnNotify** qui appelle une fonction de rappel. 
  
L’utilisation de **HrAllocAdviseSink** a des avantages et des inconvénients. Il peut économiser du travail, mais il ne permet pas de contrôler la référence en comptant l’objet de sink de conseil qu’il crée. Par conséquent, les clients qui doivent contrôler avec soin la publication de leur sink de conseil ou qui ont des dépendances entre leur sink de conseil et un autre objet client doivent construire leur propre implémentation **IMAPIAdviseSink** et éviter d’utiliser **hrAllocAdviseSink** entièrement. 
  
Un client implémentant son propre sink de conseil doit en faire un objet indépendant non lié à ou dépendant d’autres objets afin d’éliminer les complications potentielles dans le comptage des références et la libération d’objets. Toutefois, si vous devez implémenter votre sink de conseil dans le cadre d’un autre objet ou inclure un pointeur arrière vers un autre objet en tant que membre de données, il est recommandé de conserver deux nombres de références distincts : un pour l’objet référencé par le sink de conseil et un pour le sink de conseil. 
  
Lorsque le nombre de références de l’objet référencé tombe à zéro, toutes ses méthodes peuvent échouer et sa table vtable peut être détruite, mais la mémoire du puits de conseil doit rester intacte jusqu’à ce que son nombre de références tombe également à zéro. Cela signifie que la méthode **Release** du sink de conseil doit décrémenter son nombre de références et terminer la destruction de l’objet lorsque ce nombre atteint zéro. Si deux nombres de références distincts ne sont pas conservés, il est facile de détruire par inadvertance le sink de conseil dans le cadre du processus release de **l’objet englobant** . 
  
Les clients qui **utilisent HrAllocAdviseSink** pour implémenter un sink de conseil doivent également faire attention à ne pas inclure leur fonction de rappel en tant que méthode dans un autre objet de sink de conseil. Pour les clients C++, il est tentant de le faire et de transmettre  _ce pointeur_ en tant que paramètre. Il s’agit d’une stratégie dangereuse, car les clients libèrent généralement un objet lorsque son nombre de références atteint zéro. Libérer de la mémoire pour l’objet de sink de conseil rendrait  _ce_ pointeur non valide. 
  
Selon le type d’événement et la source de conseil, votre méthode **OnNotify** peut gérer les événements de différentes manières. Le tableau suivant propose des suggestions sur la façon de gérer certains des événements standard. 
  
|**Type d’événement**|**Gestion dans OnNotify**|
|:-----|:-----|
|Objet déplacé  <br/> |Si le parent d’origine de l’objet déplacé est lié au nouveau parent, mettez à jour l’affichage en commençant par le conteneur de dossier ou de carnet d’adresses le plus élevé dans la hiérarchie. Si les deux conteneurs parents ne sont pas liés, mettez à jour les deux affichages. |
|Nouveau message  <br/> |Modifiez l’interface utilisateur pour informer l’utilisateur de l’arrivée d’un ou de plusieurs nouveaux messages. Placez le dossier de réception dans l’affichage actuel. |
|Error  <br/> |Pour tous les objets à l’exception de la session, enregistrez l’erreur si nécessaire et renvoyez- le. Pour l’objet de session, déconnectez-vous si possible. |
|Recherche terminée  <br/> |Aucun traitement n’est nécessaire. |
   
> [!NOTE]
> Les handlers de notification doivent être réentrants. 
  

