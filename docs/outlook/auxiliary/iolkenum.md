---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: be91a56f93b787f5570139768d96eb4f7fe9ac02
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782749"
---
# <a name="iolkenum"></a><span data-ttu-id="0decc-102">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="0decc-102">IOlkEnum</span></span>

<span data-ttu-id="0decc-103">Prend en charge l’énumération des comptes en tant qu’objets [IUnknown](http://msdn.microsoft.com/library/com.iunknown%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0decc-103">Supports enumerating accounts as [IUnknown](http://msdn.microsoft.com/library/com.iunknown%28Office.15%29.aspx) objects.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="0decc-104">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="0decc-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0decc-105">Hérite de :</span><span class="sxs-lookup"><span data-stu-id="0decc-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="0decc-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="0decc-106">IUnknown</span></span>](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="0decc-107">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="0decc-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="0decc-108">Outlook</span><span class="sxs-lookup"><span data-stu-id="0decc-108">Outlook</span></span>  <br/> |
|<span data-ttu-id="0decc-109">Fourni par :</span><span class="sxs-lookup"><span data-stu-id="0decc-109">Provided by:</span></span>  <br/> |[<span data-ttu-id="0decc-110">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="0decc-110">IOlkAccountManager::EnumerateAccounts</span></span>](iolkaccountmanager-enumerateaccounts.md) <br/> |
|<span data-ttu-id="0decc-111">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="0decc-111">Called by:</span></span>  <br/> |<span data-ttu-id="0decc-112">Client</span><span class="sxs-lookup"><span data-stu-id="0decc-112">Client</span></span>  <br/> |
|<span data-ttu-id="0decc-113">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="0decc-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="0decc-114">IID_IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="0decc-114">IID_IOlkEnum</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="0decc-115">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="0decc-115">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="0decc-116">GetCount</span><span class="sxs-lookup"><span data-stu-id="0decc-116">GetCount</span></span>](iolkenum-getcount.md) <br/> |<span data-ttu-id="0decc-117">Obtient le nombre de comptes dans l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="0decc-117">Gets the number of accounts in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="0decc-118">Reset</span><span class="sxs-lookup"><span data-stu-id="0decc-118">Reset</span></span>](iolkenum-reset.md) <br/> |<span data-ttu-id="0decc-119">Réinitialise l’énumérateur au début.</span><span class="sxs-lookup"><span data-stu-id="0decc-119">Resets the enumerator to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="0decc-120">GetNext</span><span class="sxs-lookup"><span data-stu-id="0decc-120">GetNext</span></span>](iolkenum-getnext.md) <br/> |<span data-ttu-id="0decc-121">Obtient le compte suivant dans l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="0decc-121">Gets the next account in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="0decc-122">Ignorer</span><span class="sxs-lookup"><span data-stu-id="0decc-122">Skip</span></span>](iolkenum-skip.md) <br/> |<span data-ttu-id="0decc-123">Ignore un nombre spécifié de comptes dans l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="0decc-123">Skips a specified number of accounts in the enumerator.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0decc-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="0decc-124">Remarks</span></span>

<span data-ttu-id="0decc-125">Cette interface est retournée par **IOlkAccountManager::EnumerateAccounts** lors de l’obtention d’un énumérateur de comptes.</span><span class="sxs-lookup"><span data-stu-id="0decc-125">This interface is returned by **IOlkAccountManager::EnumerateAccounts** when obtaining an enumerator of accounts.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0decc-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0decc-126">See also</span></span>

- [<span data-ttu-id="0decc-127">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="0decc-127">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="0decc-128">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="0decc-128">Constants (Account management API)</span></span>](constants-account-management-api.md)

