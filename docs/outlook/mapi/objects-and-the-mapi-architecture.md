---
title: Objets et architecture MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c3bcbda5-820d-4ef5-bffd-c254eea9dff6
ms.openlocfilehash: 60f71a8c08033fc6f7b96a35a8099647b7094510
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63368614"
---
# <a name="objects-and-the-mapi-architecture"></a>Objets et architecture MAPI

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Tous les objets que MAPI définit se transforment en une ou plusieurs couches dans l’architecture MAPI. La couche d’interface client contient tous les objets qu’une application cliente, une visionneuse de formulaires ou un serveur de formulaires peut implémenter. La couche d’interface du fournisseur de services contient les objets qu’un fournisseur de services de tout type peut implémenter. Cette couche comprend des objets implémentés par des carnets d’adresses, des magasins de messages, des fournisseurs de transport et des bibliothèques de formulaires. La couche qui représente le sous-système MAPI est positionnée entre les couches d’interface du client et du fournisseur de services. La couche MAPI contient tous les objets que MAPI implémente pour les clients ou fournisseurs de services à utiliser. 
  
L’illustration suivante montre où chacun des objets MAPI s’inscrit dans l’architecture MAPI. Les objets sont représentés avec les noms de leurs interfaces dérivées. Par exemple, un objet de sink de conseil s’affiche comme [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md), l’interface qui dérive [d’IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) et que chaque objet de sink de conseil implémente. Interfaces utilisées ou implémentées par plusieurs composants. Bien que la couche MAPI semble séparer les couches client et fournisseur, ce qui signifie que toutes les communications doivent passer par MAPI, ce n’est pas le cas. Les clients peuvent et communiquent directement avec les objets du fournisseur de services. 
  
**Couches d’objets dans MAPI**
  
![Couches d’objets dans MAPI](media/amapi_38.gif "Couches d’objets dans MAPI")
  
## <a name="see-also"></a>Voir aussi

- [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)
- [Vue d’ensemble de l’interface et de l’objet MAPI](mapi-object-and-interface-overview.md)

