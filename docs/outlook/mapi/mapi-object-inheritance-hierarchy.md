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
# <a name="mapi-object-inheritance-hierarchy"></a><span data-ttu-id="a51ac-103">Hiérarchie d’héritage MAPI objet</span><span class="sxs-lookup"><span data-stu-id="a51ac-103">MAPI object inheritance hierarchy</span></span>

<span data-ttu-id="a51ac-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a51ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a51ac-105">Toutes les interfaces implémentées par les objets MAPI héritent en dernier ressort [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), l’interface OLE aux objets de communiquer.</span><span class="sxs-lookup"><span data-stu-id="a51ac-105">All interfaces implemented by MAPI objects ultimately inherit from [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), the OLE interface that enables objects to communicate.</span></span> <span data-ttu-id="a51ac-106">La plupart des interfaces héritent directement **IUnknown**, mais certaines héritent d’une des deux autres interfaces de base : [IMAPIProp : IUnknown](imapipropiunknown.md) ou [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="a51ac-106">Most interfaces directly inherit from **IUnknown**, but some inherit from one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) or [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md).</span></span> <span data-ttu-id="a51ac-107">L’illustration suivante montre la hiérarchie d’héritage complet MAPI.</span><span class="sxs-lookup"><span data-stu-id="a51ac-107">The following illustration shows the complete inheritance hierarchy in MAPI.</span></span>
  
<span data-ttu-id="a51ac-108">**Hiérarchie d’héritage MAPI**</span><span class="sxs-lookup"><span data-stu-id="a51ac-108">**MAPI inheritance hierarchy**</span></span>
  
<span data-ttu-id="a51ac-109">![Hiérarchie d’héritage MAPI] (media/amapi_06.gif "Hiérarchie d’héritage MAPI")</span><span class="sxs-lookup"><span data-stu-id="a51ac-109">![MAPI inheritance hierarchy](media/amapi_06.gif "MAPI inheritance hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a51ac-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a51ac-110">See also</span></span>

- [<span data-ttu-id="a51ac-111">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a51ac-111">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md) 
- [<span data-ttu-id="a51ac-112">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a51ac-112">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)
- [<span data-ttu-id="a51ac-113">Objet MAPI et vue d’ensemble de l’Interface</span><span class="sxs-lookup"><span data-stu-id="a51ac-113">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

