---
title: IOlkAccountHelper
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc2972da-80e9-50e2-10b3-585eb63e9103
ms.openlocfilehash: 3c28b1e8ab7e2d72d27cc6545b6ef57834ef5b6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782703"
---
# <a name="iolkaccounthelper"></a><span data-ttu-id="4e2b0-102">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="4e2b0-102">IOlkAccountHelper</span></span>

<span data-ttu-id="4e2b0-103">Fournit des fonctionnalités d’assistance dans la session MAPI en cours pour gérer les comptes.</span><span class="sxs-lookup"><span data-stu-id="4e2b0-103">Provides helper functionality in the current MAPI session to manage accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4e2b0-104">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="4e2b0-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4e2b0-105">Hérite de :</span><span class="sxs-lookup"><span data-stu-id="4e2b0-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="4e2b0-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="4e2b0-106">IUnknown</span></span>](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="4e2b0-107">Fourni par :</span><span class="sxs-lookup"><span data-stu-id="4e2b0-107">Provided by:</span></span>  <br/> |<span data-ttu-id="4e2b0-108">Client</span><span class="sxs-lookup"><span data-stu-id="4e2b0-108">Client</span></span>  <br/> |
|<span data-ttu-id="4e2b0-109">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="4e2b0-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="4e2b0-110">IID_IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="4e2b0-110">IID_IOlkAccountHelper</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="4e2b0-111">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="4e2b0-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="4e2b0-112">PlaceHolder1</span><span class="sxs-lookup"><span data-stu-id="4e2b0-112">Placeholder1</span></span>](iolkaccounthelper-placeholder1.md) <br/> | <span data-ttu-id="4e2b0-113">*Ce membre est un espace réservé et n’est pas pris en charge.*</span><span class="sxs-lookup"><span data-stu-id="4e2b0-113">*This member is a placeholder and is not supported.*</span></span>  <br/> |
|[<span data-ttu-id="4e2b0-114">GetIdentity</span><span class="sxs-lookup"><span data-stu-id="4e2b0-114">GetIdentity</span></span>](iolkaccounthelper-getidentity.md) <br/> |<span data-ttu-id="4e2b0-115">Obtient le nom du profil d’un compte.</span><span class="sxs-lookup"><span data-stu-id="4e2b0-115">Gets the profile name of an account.</span></span>  <br/> |
|[<span data-ttu-id="4e2b0-116">GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="4e2b0-116">GetMapiSession</span></span>](iolkaccounthelper-getmapisession.md) <br/> |<span data-ttu-id="4e2b0-117">Ouvre une session MAPI et conserve une référence à la session pour le Gestionnaire de comptes.</span><span class="sxs-lookup"><span data-stu-id="4e2b0-117">Opens a MAPI session and maintains a reference to the session for the account manager.</span></span>  <br/> |
|[<span data-ttu-id="4e2b0-118">HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="4e2b0-118">HandsOffSession</span></span>](iolkaccounthelper-handsoffsession.md) <br/> |<span data-ttu-id="4e2b0-119">Libère l’objet de session MAPI qui a été renvoyée par [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span><span class="sxs-lookup"><span data-stu-id="4e2b0-119">Releases the MAPI session object that was returned by [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e2b0-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="4e2b0-120">Remarks</span></span>

<span data-ttu-id="4e2b0-121">Cette interface est transmise à [IOlkAccountManager::Init](iolkaccountmanager-init.md) lors de l’initialisation du Gestionnaire de comptes.</span><span class="sxs-lookup"><span data-stu-id="4e2b0-121">This interface is passed to [IOlkAccountManager::Init](iolkaccountmanager-init.md) when initializing the account manager.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4e2b0-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e2b0-122">See also</span></span>

- [<span data-ttu-id="4e2b0-123">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="4e2b0-123">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="4e2b0-124">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="4e2b0-124">Constants (Account management API)</span></span>](constants-account-management-api.md)

