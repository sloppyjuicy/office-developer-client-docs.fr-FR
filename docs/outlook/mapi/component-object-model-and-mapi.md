---
title: MAPI et component Object Model
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cca4c70d-b73a-4834-80b5-9cb5889f63cc
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: cf687a7bfadb0981ca3440c2f81bc5de8f910924
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783066"
---
# <a name="component-object-model-and-mapi"></a>MAPI et component Object Model

  
  
**S’applique à**: Outlook 
  
La documentation du Kit de développement logiciel Windows comprend des informations complètes sur les règles d’implémentation des objets qui sont conformes à l’objet COM (Component Model). Ces règles expliquent comment effectuer les opérations suivantes :
  
- Concevoir des interfaces et les objets.
    
- Implémenter l’interface [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx) . 
    
- Gérer la mémoire.
    
- Gérer le décompte de références.
    
- Implémenter des objets apartment de thread.
    
Bien que tous les objets MAPI sont considérés comme reposant sur COM, car ils implémentent des interfaces qui héritent de [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx), MAPI écart et dans certaines situations, les règles COM standards. Cette déviation permet aux développeurs une plus grande flexibilité dans leurs implémentations. Par exemple, une interface MAPI, comme une interface COM, décrit un contrat entre l’implémentation et de l’appelant. Une fois que l’interface est créée et publiée, sa définition ne peut pas et ne change pas. MAPI ne s’écarte pas cette description, mais il relâche la description quelque peu. L’implémentation de la possibilité ne pas implémenter des méthodes, renvoi d’une des valeurs d’erreur à l’appelant : 
  
- MAPI_E_NO_SUPPORT
    
- MAPI_E_TOO_COMPLEX
    
- MAPI_E_BAD_CHARWIDTH
    
- MAPI_E_TYPE_NO_SUPPORT
    
Les autres variations de règles COM standard sont décrits dans le tableau suivant.
  
|**Règle de programmation COM**|**Variante MAPI**|
|:-----|:-----|
|Tous les paramètres de chaîne dans les méthodes d’interface doivent être Unicode.  <br/> |Les interfaces MAPI sont définies pour autoriser les paramètres de chaîne Unicode ou ANSI. De nombreuses méthodes qui ont un paramètre de chaîne ont également un paramètre **ulFlags** ; la largeur d’un paramètre de chaîne est indiquée par la valeur de l’indicateur MAPI_UNICODE dans **ulFlags**. Certaines interfaces MAPI ne prend en charge Unicode et renvoyer MAPI_E_BAD_CHARWIDTH lors de l’indicateur MAPI_UNICODE est défini.  <br/> |
|Toutes les méthodes d’interface doivent avoir un type de retour de HRESULT.  <br/> |MAPI a au moins une méthode qui retourne une valeur HRESULT non : [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).  <br/> |
|Les appelants et les responsables de l’implémentation doivent allouer et libérer de la mémoire pour les paramètres de l’interface à l’aide des norme allocateurs de tâche COM.  <br/> |Toutes les méthodes MAPI permet de gérer la mémoire pour les paramètres de l’interface les allocateurs liés [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)et [MAPIFreeBuffer](mapifreebuffer.md) . Toutes les implémentations de MAPI des interfaces définies par OLE, tels [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx), utilisent les allocateurs de tâche COM standards.  <br/> |
|Toutes les paramètres pointeurs doivent explicitement être définies sur la valeur NULL en cas d’échec d’une méthode.  <br/> |Interfaces MAPI nécessitent que les paramètres pointeurs qu'être défini sur NULL ou restent inchangés lorsqu’une méthode échoue. Toutes les implémentations de MAPI des interfaces définies par OLE définir explicitement des paramètres sur la valeur NULL en cas d’échec.  <br/> |
|Implémenter des objets agrégées autant que possible.  <br/> |Interfaces MAPI ne sont pas agrégées.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[Objet MAPI et vue d’ensemble de l’Interface](mapi-object-and-interface-overview.md)

