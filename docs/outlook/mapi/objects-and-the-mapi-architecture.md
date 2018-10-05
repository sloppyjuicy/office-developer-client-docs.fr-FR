---
title: Objets et l’architecture MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c3bcbda5-820d-4ef5-bffd-c254eea9dff6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4f8bc2a5268d220c17a59148f8b8ba1d320d225b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391037"
---
# <a name="objects-and-the-mapi-architecture"></a>Objets et l’architecture MAPI

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Tous les objets qui définit MAPI peuvent être classées dans une ou plusieurs couches de l’architecture MAPI. La couche d’interface client contient tous les objets qu’une application cliente, une visionneuse de formulaire ou un serveur de formulaire peut implémenter. La couche d’interface de service fournisseur contient les objets qui permettre mettre en œuvre un fournisseur de services d’un type quelconque. Cette couche inclut des objets implémentés par les carnets d’adresses, les banques de messages, les fournisseurs de transport et bibliothèques de formulaires. La couche qui représente le sous-système MAPI est placée entre les couches de l’interface fournisseur client et le service. La couche MAPI contient tous les objets implémentés par MAPI pour les clients ou fournisseurs de services à utiliser. 
  
L’illustration suivante montre où chacun des objets MAPI correspond à l’architecture MAPI. Les objets sont représentées par les noms de leurs interfaces dérivées. Par exemple, un objet de récepteur advise est signalée comme étant [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md), l’interface qui dérive de [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) et qui implémente tous les objets récepteur advise. Les interfaces reliant les calques sont utilisés ou implémentées par plusieurs composants. Bien que la couche MAPI s’affiche pour séparer les couches client et le fournisseur, ce qui implique que toutes les communications doivent passer par l’interface MAPI, ce n’est pas le cas. Les clients peuvent et communiquent directement aux objets de fournisseur de service. 
  
**Couches d’objets dans MAPI**
  
![Couches d’objets dans MAPI] (media/amapi_38.gif "Couches d’objets dans MAPI")
  
## <a name="see-also"></a>Voir aussi

- [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)
- [Objet MAPI et vue d’ensemble de l’Interface](mapi-object-and-interface-overview.md)

