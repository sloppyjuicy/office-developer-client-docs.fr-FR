---
title: Hiérarchie d’héritage MAPI objet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3dc0b79f-e346-416d-ac81-42eba6b6d3b2
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: a03b994a613bbb1f17db3e3220b7e053989c278a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784644"
---
# <a name="mapi-object-inheritance-hierarchy"></a>Hiérarchie d’héritage MAPI objet

**S’applique à**: Outlook 
  
Toutes les interfaces implémentées par les objets MAPI héritent en dernier ressort [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), l’interface OLE aux objets de communiquer. La plupart des interfaces héritent directement **IUnknown**, mais certaines héritent d’une des deux autres interfaces de base : [IMAPIProp : IUnknown](imapipropiunknown.md) ou [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md). L’illustration suivante montre la hiérarchie d’héritage complet MAPI.
  
**Hiérarchie d’héritage MAPI**
  
![Hiérarchie d’héritage MAPI] (media/amapi_06.gif "Hiérarchie d’héritage MAPI")
  
## <a name="see-also"></a>Voir aussi

- [IMAPIProp : IUnknown](imapipropiunknown.md) 
- [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)
- [Objet MAPI et vue d’ensemble de l’Interface](mapi-object-and-interface-overview.md)

