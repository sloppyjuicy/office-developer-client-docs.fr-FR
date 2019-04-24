---
title: Objets et architecture MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c3bcbda5-820d-4ef5-bffd-c254eea9dff6
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 4f8bc2a5268d220c17a59148f8b8ba1d320d225b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279786"
---
# <a name="objects-and-the-mapi-architecture"></a>Objets et architecture MAPI

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Tous les objets que MAPI définit correspondent à une ou plusieurs couches de l'architecture MAPI. La couche d'interface cliente contient tous les objets qu'une application cliente, la visionneuse de formulaire ou le serveur de formulaires peut implémenter. La couche d'interface du fournisseur de services contient les objets pouvant être implémentés par un fournisseur de services de n'importe quel type. Cette couche inclut les objets implémentés par les carnets d'adresses, les banques de messages, les fournisseurs de transport et les bibliothèques de formulaires. La couche qui représente le sous-système MAPI est positionnée entre les couches d'interface client et fournisseur de services. La couche MAPI contient tous les objets que MAPI implémente pour les clients ou les fournisseurs de services à utiliser. 
  
L'illustration suivante montre où chacun des objets MAPI s'intègre à l'architecture MAPI. Les objets sont représentés par les noms de leurs interfaces dérivées. Par exemple, un objet de récepteur de notifications est affiché sous la forme [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md), l'interface qui dérive de [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) et que chaque objet de récepteur de notifications implémente. Les interfaces que les couches de pont sont utilisées ou implémentées par plusieurs composants. Bien que la couche MAPI semble séparer les couches client et fournisseur, ce qui signifie que toutes les communications doivent transiter via MAPI, ce n'est pas le cas. Les clients peuvent communiquer directement avec les objets du fournisseur de services. 
  
**Couches d’objets dans MAPI**
  
![Couches d'objets dans MAPI] (media/amapi_38.gif "Couches d'objets dans MAPI")
  
## <a name="see-also"></a>Voir aussi

- [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)
- [Vue d'ensemble de l'objet et de l'interface MAPI](mapi-object-and-interface-overview.md)

