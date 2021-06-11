---
title: Objets et architecture MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c3bcbda5-820d-4ef5-bffd-c254eea9dff6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4f8bc2a5268d220c17a59148f8b8ba1d320d225b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279786"
---
# <a name="objects-and-the-mapi-architecture"></a>Objets et architecture MAPI

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Tous les objets que MAPI définit se transforment en une ou plusieurs couches dans l’architecture MAPI. La couche d’interface client contient tous les objets qu’une application cliente, une visionneuse de formulaires ou un serveur de formulaires peut implémenter. La couche d’interface du fournisseur de services contient les objets qu’un fournisseur de services de tout type peut implémenter. Cette couche comprend des objets implémentés par des carnets d’adresses, des magasins de messages, des fournisseurs de transport et des bibliothèques de formulaires. La couche qui représente le sous-système MAPI est positionnée entre les couches d’interface du client et du fournisseur de services. La couche MAPI contient tous les objets que MAPI implémente pour les clients ou fournisseurs de services à utiliser. 
  
L’illustration suivante montre où chacun des objets MAPI s’inscrit dans l’architecture MAPI. Les objets sont représentés avec les noms de leurs interfaces dérivées. Par exemple, un objet de sink de conseil s’affiche comme [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md), l’interface qui dérive de [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) et que chaque objet de sink de conseil implémente. Interfaces utilisées ou implémentées par plusieurs composants. Bien que la couche MAPI semble séparer les couches client et fournisseur, ce qui signifie que toutes les communications doivent passer par MAPI, ce n’est pas le cas. Les clients peuvent et communiquent directement avec les objets du fournisseur de services. 
  
**Couches d’objets dans MAPI**
  
![Couches d’objet dans les couches](media/amapi_38.gif "de l’objet MAPI dans MAPI")
  
## <a name="see-also"></a>Voir aussi

- [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)
- [Vue d’ensemble de l’interface et de l’objet MAPI](mapi-object-and-interface-overview.md)

