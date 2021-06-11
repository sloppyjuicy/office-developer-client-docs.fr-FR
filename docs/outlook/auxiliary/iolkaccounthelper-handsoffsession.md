---
title: IOlkAccountHelperHandsOffSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9f71fdef-5df5-0892-b64c-293a2f22f5c3
description: Libère l’objet de session MAPI renvoyé par IOlkAccountHelper::GetMapiSession.
ms.openlocfilehash: c481cee1ecb8c2bd3997cdee8ae86c9c3b5a712e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418630"
---
# <a name="iolkaccounthelperhandsoffsession"></a><span data-ttu-id="a011a-103">IOlkAccountHelper::HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="a011a-103">IOlkAccountHelper::HandsOffSession</span></span>

<span data-ttu-id="a011a-104">Libère l’objet de session MAPI qui a été renvoyé par - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span><span class="sxs-lookup"><span data-stu-id="a011a-104">Releases the MAPI session object that was returned by - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a011a-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="a011a-105">Quick info</span></span>

<span data-ttu-id="a011a-106">Voir [IOlkAccountHelper](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="a011a-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::HandsOffSession( );
```

## <a name="return-values"></a><span data-ttu-id="a011a-107">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="a011a-107">Return values</span></span>

|<span data-ttu-id="a011a-108">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="a011a-108">**HRESULT**</span></span>|<span data-ttu-id="a011a-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="a011a-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a011a-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="a011a-110">S_OK</span></span>  <br/> |<span data-ttu-id="a011a-111">Si votre implémentation **d’IOlkAccountHelper** crée sa propre session MAPI qui est renvoyée dans **IOlkAccountHelper::GetMapiSession,** vous devez libérer la session ici et renvoyer S_OK.</span><span class="sxs-lookup"><span data-stu-id="a011a-111">If your implementation of **IOlkAccountHelper** creates its own MAPI session that is returned in **IOlkAccountHelper::GetMapiSession**, you must release the session here and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="a011a-112">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="a011a-112">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="a011a-113">Si votre implémentation **d’IOlkAccountHelper** n’a pas créé sa propre session MAPI, vous devez renvoyer uniquement E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="a011a-113">If your implementation of **IOlkAccountHelper** did not create its own MAPI session, you must return only E_NOTIMPL.</span></span> <span data-ttu-id="a011a-114">Dans ce cas, il s’agit de la seule valeur de retour prise en charge.</span><span class="sxs-lookup"><span data-stu-id="a011a-114">In this case, this is the only supported return value.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a011a-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a011a-115">See also</span></span>

- [<span data-ttu-id="a011a-116">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="a011a-116">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="a011a-117">IOlkAccountHelper::GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="a011a-117">IOlkAccountHelper::GetMapiSession</span></span>](iolkaccounthelper-getmapisession.md)

