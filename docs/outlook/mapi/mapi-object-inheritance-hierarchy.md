---
title: Hiérarchie d’héritage MAPI objet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3dc0b79f-e346-416d-ac81-42eba6b6d3b2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4b610415089ff19165ffcabc9e13901ed63c907d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391786"
---
# <a name="mapi-object-inheritance-hierarchy"></a>Hiérarchie d’héritage MAPI objet

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Toutes les interfaces implémentées par les objets MAPI héritent en dernier ressort [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), l’interface OLE aux objets de communiquer. La plupart des interfaces héritent directement **IUnknown**, mais certaines héritent d’une des deux autres interfaces de base : [IMAPIProp : IUnknown](imapipropiunknown.md) ou [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md). L’illustration suivante montre la hiérarchie d’héritage complet MAPI.
  
**Hiérarchie d’héritage MAPI**
  
![Hiérarchie d’héritage MAPI] (media/amapi_06.gif "Hiérarchie d’héritage MAPI")
  
## <a name="see-also"></a>Voir aussi

- [IMAPIProp : IUnknown](imapipropiunknown.md) 
- [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)
- [Objet MAPI et vue d’ensemble de l’Interface](mapi-object-and-interface-overview.md)

