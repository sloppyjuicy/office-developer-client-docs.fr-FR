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
# <a name="mapi-object-inheritance-hierarchy"></a><span data-ttu-id="0ccb8-103">Hiérarchie d’héritage d’objets MAPI</span><span class="sxs-lookup"><span data-stu-id="0ccb8-103">MAPI object inheritance hierarchy</span></span>

<span data-ttu-id="0ccb8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ccb8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ccb8-105">Toutes les interfaces implémentées par les objets MAPI héritent finalement [d’IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), l’interface OLE qui permet aux objets de communiquer.</span><span class="sxs-lookup"><span data-stu-id="0ccb8-105">All interfaces implemented by MAPI objects ultimately inherit from [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), the OLE interface that enables objects to communicate.</span></span> <span data-ttu-id="0ccb8-106">La plupart des interfaces héritent directement **d’IUnknown,** mais certaines héritent de l’une des deux autres interfaces de base : [IMAPIProp : IUnknown](imapipropiunknown.md) ou [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="0ccb8-106">Most interfaces directly inherit from **IUnknown**, but some inherit from one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) or [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md).</span></span> <span data-ttu-id="0ccb8-107">L’illustration suivante montre la hiérarchie d’héritage complète dans MAPI.</span><span class="sxs-lookup"><span data-stu-id="0ccb8-107">The following illustration shows the complete inheritance hierarchy in MAPI.</span></span>
  
<span data-ttu-id="0ccb8-108">**Hiérarchie d’héritage MAPI**</span><span class="sxs-lookup"><span data-stu-id="0ccb8-108">**MAPI inheritance hierarchy**</span></span>
  
<span data-ttu-id="0ccb8-109">![Hiérarchie d’héritage MAPI -]Hiérarchie(media/amapi_06.gif "d’héritage MAPI")</span><span class="sxs-lookup"><span data-stu-id="0ccb8-109">![MAPI inheritance hierarchy](media/amapi_06.gif "MAPI inheritance hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0ccb8-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ccb8-110">See also</span></span>

- [<span data-ttu-id="0ccb8-111">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0ccb8-111">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md) 
- [<span data-ttu-id="0ccb8-112">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0ccb8-112">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)
- [<span data-ttu-id="0ccb8-113">Vue d’ensemble de l’interface et de l’objet MAPI</span><span class="sxs-lookup"><span data-stu-id="0ccb8-113">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

