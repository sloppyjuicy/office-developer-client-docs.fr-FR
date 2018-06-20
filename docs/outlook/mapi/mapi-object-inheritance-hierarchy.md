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
# <a name="mapi-object-inheritance-hierarchy"></a><span data-ttu-id="45f48-103">Hiérarchie d’héritage MAPI objet</span><span class="sxs-lookup"><span data-stu-id="45f48-103">MAPI object inheritance hierarchy</span></span>

<span data-ttu-id="45f48-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="45f48-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="45f48-105">Toutes les interfaces implémentées par les objets MAPI héritent en dernier ressort [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), l’interface OLE aux objets de communiquer.</span><span class="sxs-lookup"><span data-stu-id="45f48-105">All interfaces implemented by MAPI objects ultimately inherit from [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), the OLE interface that enables objects to communicate.</span></span> <span data-ttu-id="45f48-106">La plupart des interfaces héritent directement **IUnknown**, mais certaines héritent d’une des deux autres interfaces de base : [IMAPIProp : IUnknown](imapipropiunknown.md) ou [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="45f48-106">Most interfaces directly inherit from **IUnknown**, but some inherit from one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) or [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md).</span></span> <span data-ttu-id="45f48-107">L’illustration suivante montre la hiérarchie d’héritage complet MAPI.</span><span class="sxs-lookup"><span data-stu-id="45f48-107">The following illustration shows the complete inheritance hierarchy in MAPI.</span></span>
  
<span data-ttu-id="45f48-108">**Hiérarchie d’héritage MAPI**</span><span class="sxs-lookup"><span data-stu-id="45f48-108">**MAPI inheritance hierarchy**</span></span>
  
<span data-ttu-id="45f48-109">![Hiérarchie d’héritage MAPI] (media/amapi_06.gif "Hiérarchie d’héritage MAPI")</span><span class="sxs-lookup"><span data-stu-id="45f48-109">![MAPI inheritance hierarchy](media/amapi_06.gif "MAPI inheritance hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="45f48-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45f48-110">See also</span></span>

- [<span data-ttu-id="45f48-111">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="45f48-111">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md) 
- [<span data-ttu-id="45f48-112">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="45f48-112">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)
- [<span data-ttu-id="45f48-113">Objet MAPI et vue d’ensemble de l’Interface</span><span class="sxs-lookup"><span data-stu-id="45f48-113">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

