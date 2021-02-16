---
title: Hiérarchie d’héritage d’objets MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3dc0b79f-e346-416d-ac81-42eba6b6d3b2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4b610415089ff19165ffcabc9e13901ed63c907d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345838"
---
# <a name="mapi-object-inheritance-hierarchy"></a>Hiérarchie d’héritage d’objets MAPI

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Toutes les interfaces implémentées par les objets MAPI héritent finalement [d’IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), l’interface OLE qui permet aux objets de communiquer. La plupart des interfaces héritent directement **d’IUnknown,** mais certaines héritent de l’une des deux autres interfaces de base : [IMAPIProp : IUnknown](imapipropiunknown.md) ou [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md). L’illustration suivante montre la hiérarchie d’héritage complète dans MAPI.
  
**Hiérarchie d’héritage MAPI**
  
![Hiérarchie d’héritage MAPI -]Hiérarchie(media/amapi_06.gif "d’héritage MAPI")
  
## <a name="see-also"></a>Voir aussi

- [IMAPIProp : IUnknown](imapipropiunknown.md) 
- [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)
- [Vue d’ensemble de l’interface et de l’objet MAPI](mapi-object-and-interface-overview.md)

