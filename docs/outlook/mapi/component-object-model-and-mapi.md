---
title: COM (Component Object Model) et MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: cca4c70d-b73a-4834-80b5-9cb5889f63cc
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bfeedf5073e162744099a22b8febcd8fb544da54
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567738"
---
# <a name="component-object-model-and-mapi"></a>COM (Component Object Model) et MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La documentation Windows SDK inclut une discussion complète des règles d’implémentation d’objets conformes au modèle objet composant (COM). Ces règles d mentent la procédure suivante :
  
- Interfaces et objets de conception.
    
- Implémenter [l’interface IUnknown.](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) 
    
- Gérer la mémoire.
    
- Gérer le décompte des références.
    
- Implémenter des objets threadés en location.
    
Bien que tous les objets MAPI soient considérés comme basés sur COM, car ils implémentent des interfaces qui héritent [d’IUnknown,](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)MAPI s’écarte dans certaines situations des règles COM standard. Cet écart permet aux développeurs d’avoir plus de souplesse dans leurs implémentations. Par exemple, une interface MAPI, comme n’importe quelle interface COM, décrit un contrat entre l’implémenteur et l’appelant. Une fois l’interface créée et publiée, sa définition ne peut pas et ne change pas. MAPI ne s’écarte pas de cette description, mais il la relâche un peu. Les implémenteurs peuvent choisir de ne pas implémenter des méthodes particulières, en renvoyant l’une des valeurs d’erreur suivantes à l’appelant : 
  
- MAPI_E_NO_SUPPORT
    
- MAPI_E_TOO_COMPLEX
    
- MAPI_E_BAD_CHARWIDTH
    
- MAPI_E_TYPE_NO_SUPPORT
    
Les autres écarts par rapport aux règles COM standard sont décrits dans le tableau suivant.
  
|**Règle de programmation COM**|**Variante MAPI**|
|:-----|:-----|
|Tous les paramètres de chaîne dans les méthodes d’interface doivent être Unicode.  <br/> |Les interfaces MAPI sont définies pour autoriser les paramètres de chaîne Unicode ou ANSI. De nombreuses méthodes qui ont un paramètre de chaîne ont également **un paramètre ulFlags** ; la largeur d’un paramètre de chaîne est indiquée par la valeur de l’indicateur MAPI_UNICODE dans **ulFlags**. Certaines interfaces MAPI ne prisent pas en charge Unicode et retournent des MAPI_E_BAD_CHARWIDTH lorsque l’MAPI_UNICODE est définie.  <br/> |
|Toutes les méthodes d’interface doivent avoir un type de retour HRESULT.  <br/> |MAPI possède au moins une méthode qui renvoie une valeur non HRESULT : [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).  <br/> |
|Les appelants et les implémenteurs doivent allouer et libérer de la mémoire pour les paramètres d’interface à l’aide des allocations de tâches COM standard.  <br/> |Toutes les méthodes MAPI utilisent les allocateurs liés [MAPIAllocateBuffer,](mapiallocatebuffer.md) [MAPIAllocateMore](mapiallocatemore.md)et [MAPIFreeBuffer](mapifreebuffer.md) pour gérer la mémoire des paramètres d’interface. Toutes les implémentations MAPI des interfaces définies par OLE, telles que [IStream,](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)utilisent les allocations de tâches COM standard.  <br/> |
|Tous les paramètres de pointeur sortant doivent être explicitement définies sur NULL en cas d’échec d’une méthode.  <br/> |Les interfaces MAPI nécessitent que les paramètres de pointeur de sortie soient définies sur NULL ou restent inchangées en cas d’échec d’une méthode. Toutes les implémentations MAPI des interfaces définies par OLE définissent explicitement les paramètres sur NULL en cas d’échec.  <br/> |
|Implémenter des objets aggrégables dans la mesure du possible.  <br/> |Les interfaces MAPI ne sont pas aggrégables.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[Vue d’ensemble de l’interface et de l’objet MAPI](mapi-object-and-interface-overview.md)

