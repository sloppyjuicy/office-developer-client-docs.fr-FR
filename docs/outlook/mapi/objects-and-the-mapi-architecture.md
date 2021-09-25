---
title: Objets et architecture MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c3bcbda5-820d-4ef5-bffd-c254eea9dff6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9f37b5bd452f35e54edee6f98387c6f39d284106
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561179"
---
# <a name="objects-and-the-mapi-architecture"></a>Objets et architecture MAPI

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Tous les objets que MAPI définit se transforment en une ou plusieurs couches dans l’architecture MAPI. La couche d’interface client contient tous les objets qu’une application cliente, une visionneuse de formulaires ou un serveur de formulaires peut implémenter. La couche d’interface du fournisseur de services contient les objets qu’un fournisseur de services de tout type peut implémenter. Cette couche comprend des objets implémentés par des carnets d’adresses, des magasins de messages, des fournisseurs de transport et des bibliothèques de formulaires. La couche qui représente le sous-système MAPI est positionnée entre les couches d’interface du client et du fournisseur de services. La couche MAPI contient tous les objets que MAPI implémente pour les clients ou fournisseurs de services à utiliser. 
  
L’illustration suivante montre où chacun des objets MAPI s’inscrit dans l’architecture MAPI. Les objets sont représentés avec les noms de leurs interfaces dérivées. Par exemple, un objet de sink de conseil s’affiche comme [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md), l’interface qui dérive de [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) et que chaque objet de sink de conseil implémente. Interfaces utilisées ou implémentées par plusieurs composants. Bien que la couche MAPI semble séparer les couches client et fournisseur, ce qui signifie que toutes les communications doivent passer par MAPI, ce n’est pas le cas. Les clients peuvent et communiquent directement avec les objets du fournisseur de services. 
  
**Couches d’objets dans MAPI**
  
![Couches d’objets dans MAPI](media/amapi_38.gif "Couches d’objets dans MAPI")
  
## <a name="see-also"></a>Voir aussi

- [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)
- [Vue d’ensemble de l’interface et de l’objet MAPI](mapi-object-and-interface-overview.md)

