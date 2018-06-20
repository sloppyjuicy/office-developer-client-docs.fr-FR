---
title: IOlkAccountHelperHandsOffSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9f71fdef-5df5-0892-b64c-293a2f22f5c3
description: Libère l’objet de session MAPI qui a été renvoyée par IOlkAccountHelper::GetMapiSession.
ms.openlocfilehash: 71931be73e75e858224d3da2c92071341ac45e72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782704"
---
# <a name="iolkaccounthelperhandsoffsession"></a><span data-ttu-id="9bfe3-103">IOlkAccountHelper::HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="9bfe3-103">IOlkAccountHelper::HandsOffSession</span></span>

<span data-ttu-id="9bfe3-104">Libère l’objet de session MAPI qui a été renvoyée par - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span><span class="sxs-lookup"><span data-stu-id="9bfe3-104">Releases the MAPI session object that was returned by - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9bfe3-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="9bfe3-105">Quick info</span></span>

<span data-ttu-id="9bfe3-106">Voir [IOlkAccountHelper](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="9bfe3-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::HandsOffSession( );
```

## <a name="return-values"></a><span data-ttu-id="9bfe3-107">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="9bfe3-107">Return values</span></span>

|<span data-ttu-id="9bfe3-108">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="9bfe3-108">**HRESULT**</span></span>|<span data-ttu-id="9bfe3-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="9bfe3-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9bfe3-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="9bfe3-110">S_OK</span></span>  <br/> |<span data-ttu-id="9bfe3-111">Si votre implémentation de **IOlkAccountHelper** crée sa propre session MAPI qui est retournée dans **IOlkAccountHelper::GetMapiSession**, vous devez libérer la session ici et qu’elles retournent S_OK.</span><span class="sxs-lookup"><span data-stu-id="9bfe3-111">If your implementation of **IOlkAccountHelper** creates its own MAPI session that is returned in **IOlkAccountHelper::GetMapiSession**, you must release the session here and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="9bfe3-112">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="9bfe3-112">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="9bfe3-113">Si votre implémentation de **IOlkAccountHelper** n’avez pas créé sa propre session MAPI, vous devez retourner E_NOTIMPL uniquement.</span><span class="sxs-lookup"><span data-stu-id="9bfe3-113">If your implementation of **IOlkAccountHelper** did not create its own MAPI session, you must return only E_NOTIMPL.</span></span> <span data-ttu-id="9bfe3-114">Dans ce cas, il s’agit de la valeur de retour pris en charge uniquement.</span><span class="sxs-lookup"><span data-stu-id="9bfe3-114">In this case, this is the only supported return value.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9bfe3-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9bfe3-115">See also</span></span>

- [<span data-ttu-id="9bfe3-116">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="9bfe3-116">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="9bfe3-117">IOlkAccountHelper::GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="9bfe3-117">IOlkAccountHelper::GetMapiSession</span></span>](iolkaccounthelper-getmapisession.md)

