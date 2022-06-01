---
title: COM (Component Object Model) et MAPI
description: Décrit les règles d’implémentation d’objets conformes au modèle objet de composant et les variantes MAPI de ces règles.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: cca4c70d-b73a-4834-80b5-9cb5889f63cc
ms.openlocfilehash: fdb360bc453099f9566c0f6cb42f0ebfd33b66bb
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816233"
---
# <a name="component-object-model-and-mapi"></a>COM (Component Object Model) et MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La documentation du Kit de développement logiciel (SDK) Windows inclut une présentation complète des règles d’implémentation d’objets conformes au modèle COM (Component Object Model). Ces règles expliquent comment effectuer les opérations suivantes :
  
- Conception d’interfaces et d’objets.
    
- Implémentez l’interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) . 
    
- Gérer la mémoire.
    
- Gérer le comptage des références.
    
- Implémentez des objets à thread d’appartement.
    
Bien que tous les objets MAPI soient considérés comme basés sur COM parce qu’ils implémentent des interfaces qui héritent [d’IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx), MAPI dévie dans certaines situations des règles COM standard. Cet écart permet aux développeurs d’avoir plus de flexibilité dans leurs implémentations. Par exemple, une interface MAPI, comme n’importe quelle interface COM, décrit un contrat entre l’implémenteur et l’appelant. Une fois l’interface créée et publiée, sa définition ne peut pas et ne change pas. MAPI ne s’écarte pas de cette description, mais il assouplit quelque peu la description. Les implémenteurs peuvent choisir de ne pas implémenter des méthodes particulières, en retournant l’une des valeurs d’erreur suivantes à l’appelant : 
  
- MAPI_E_NO_SUPPORT
    
- MAPI_E_TOO_COMPLEX
    
- MAPI_E_BAD_CHARWIDTH
    
- MAPI_E_TYPE_NO_SUPPORT
    
Les autres écarts par rapport aux règles COM standard sont décrits dans le tableau suivant.
  
|**Règle de programmation COM**|**Variation MAPI**|
|:-----|:-----|
|Tous les paramètres de chaîne dans les méthodes d’interface doivent être Unicode. |Les interfaces MAPI sont définies pour autoriser les paramètres de chaîne Unicode ou ANSI. De nombreuses méthodes qui ont un paramètre de chaîne ont également un paramètre **ulFlags** ; la largeur d’un paramètre de chaîne est indiquée par la valeur de l’indicateur MAPI_UNICODE dans **ulFlags**. Certaines interfaces MAPI ne prennent pas en charge Unicode et retournent MAPI_E_BAD_CHARWIDTH lorsque l’indicateur MAPI_UNICODE est défini. |
|Toutes les méthodes d’interface doivent avoir un type de retour HRESULT. |MAPI a au moins une méthode qui retourne une valeur autre que HRESULT : [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md). |
|Les appelants et les implémenteurs doivent allouer et libérer de la mémoire pour les paramètres d’interface à l’aide des allocateurs de tâches COM standard. |Toutes les méthodes MAPI utilisent les allocateurs liés [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md) et [MAPIFreeBuffer](mapifreebuffer.md) pour gérer la mémoire des paramètres d’interface. Toutes les implémentations MAPI des interfaces définies par OLE, telles que [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), utilisent les allocateurs de tâches COM standard. |
|Tous les paramètres de pointeur out doivent être explicitement définis sur NULL en cas d’échec d’une méthode. |Les interfaces MAPI nécessitent que les paramètres de pointeur out soient définis sur NULL ou restent inchangés en cas d’échec d’une méthode. Toutes les implémentations MAPI des interfaces définies par OLE définissent explicitement les paramètres sur NULL en cas d’échec. |
|Implémentez des objets aggregatables dans la mesure du possible. |Les interfaces MAPI ne sont pas aggregatables. |
   
## <a name="see-also"></a>Voir aussi



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[Vue d’ensemble de l’objet et de l’interface MAPI](mapi-object-and-interface-overview.md)

