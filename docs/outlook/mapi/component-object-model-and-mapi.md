---
title: COM (Component Object Model) et MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cca4c70d-b73a-4834-80b5-9cb5889f63cc
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a91ab8497a690fd4b99f76274d0213284253fd06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334467"
---
# <a name="component-object-model-and-mapi"></a>COM (Component Object Model) et MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La documentation du kit de développement logiciel (SDK) Windows inclut une présentation complète des règles d'implémentation des objets conformes au modèle COM (Component Object Model). Ces règles permettent d'effectuer les opérations suivantes:
  
- Concevoir des interfaces et des objets.
    
- Implémentez l'interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) . 
    
- Gestion de la mémoire.
    
- Gérer le décompte de références.
    
- Implémenter des objets thread cloisonnés.
    
Bien que tous les objets MAPI soient considérés comme COM, car ils implémentent des interfaces qui héritent de [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx), MAPI s'écarte parfois des règles com standard. Cette déviation offre aux développeurs une plus grande flexibilité dans leurs implémentations. Par exemple, une interface MAPI, comme n'importe quelle interface COM, décrit un contrat entre l'implémenteur et l'appelant. Une fois que l'interface est créée et publiée, sa définition ne peut pas et ne change pas. MAPI ne s'écarte pas de cette description, mais il assouplit légèrement la description. Les implémenteurs peuvent choisir de ne pas implémenter des méthodes spécifiques, en renvoyant l'une des valeurs d'erreur suivantes à l'appelant: 
  
- MAPI_E_NO_SUPPORT
    
- MAPI_E_TOO_COMPLEX
    
- MAPI_E_BAD_CHARWIDTH
    
- MAPI_E_TYPE_NO_SUPPORT
    
Les autres écarts par rapport aux règles COM standard sont décrits dans le tableau suivant.
  
|**Règle de programmation COM**|**Variante MAPI**|
|:-----|:-----|
|Tous les paramètres de chaîne dans les méthodes d'interface doivent être au format Unicode.  <br/> |Les interfaces MAPI sont définies pour autoriser les paramètres de chaîne Unicode ou ANSI. De nombreuses méthodes qui ont un paramètre de chaîne ont également un paramètre **ulFlags** ; la largeur d'un paramètre de type chaîne est indiquée par la valeur de l'indicateur MAPI_UNICODE dans **ulFlags**. Certaines interfaces MAPI ne prennent pas en charge Unicode et renvoient MAPI_E_BAD_CHARWIDTH lorsque l'indicateur MAPI_UNICODE est défini.  <br/> |
|Toutes les méthodes d'interface doivent avoir un type de retour de HRESULT.  <br/> |MAPI a au moins une méthode qui renvoie une valeur autre que HRESULT: [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md).  <br/> |
|Les appelants et les implémenteurs doivent allouer et libérer de la mémoire pour les paramètres d'interface à l'aide des allocateurs de tâches COM standard.  <br/> |Toutes les méthodes MAPI utilisent les allocateurs liés [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)et [MAPIFreeBuffer](mapifreebuffer.md) pour gérer la mémoire des paramètres d'interface. Toutes les implémentations MAPI d'interfaces définies par OLE, telles que [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), utilisent les allocateurs de tâches com standard.  <br/> |
|Tous les paramètres de pointeur de sortie doivent être explicitement définis sur NULL lorsqu'une méthode échoue.  <br/> |Les interfaces MAPI exigent que les paramètres de pointeur de sortie soient définis sur NULL ou demeurent inchangés lorsqu'une méthode échoue. Toutes les implémentations MAPI d'interfaces définies par OLE définissent explicitement les paramètres sur NULL en cas d'échec.  <br/> |
|Implémentez les objets agrégeables autant que possible.  <br/> |Les interfaces MAPI ne peuvent pas être regroupées.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[Vue d'ensemble de l'objet et de l'interface MAPI](mapi-object-and-interface-overview.md)

