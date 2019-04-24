---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 59f43e8b3b0819b0178d60fa357e01937ae19d81
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322098"
---
# <a name="iolkenum"></a><span data-ttu-id="0e8de-102">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="0e8de-102">IOlkEnum</span></span>

<span data-ttu-id="0e8de-103">Prend en charge l'énumération des comptes en tant qu'objets [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0e8de-103">Supports enumerating accounts as [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) objects.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="0e8de-104">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="0e8de-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0e8de-105">Hérite de:</span><span class="sxs-lookup"><span data-stu-id="0e8de-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="0e8de-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="0e8de-106">IUnknown</span></span>](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|<span data-ttu-id="0e8de-107">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="0e8de-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="0e8de-108">Outlook</span><span class="sxs-lookup"><span data-stu-id="0e8de-108">Outlook</span></span>  <br/> |
|<span data-ttu-id="0e8de-109">Fourni par :</span><span class="sxs-lookup"><span data-stu-id="0e8de-109">Provided by:</span></span>  <br/> |[<span data-ttu-id="0e8de-110">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="0e8de-110">IOlkAccountManager::EnumerateAccounts</span></span>](iolkaccountmanager-enumerateaccounts.md) <br/> |
|<span data-ttu-id="0e8de-111">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="0e8de-111">Called by:</span></span>  <br/> |<span data-ttu-id="0e8de-112">Client</span><span class="sxs-lookup"><span data-stu-id="0e8de-112">Client</span></span>  <br/> |
|<span data-ttu-id="0e8de-113">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="0e8de-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="0e8de-114">IID_IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="0e8de-114">IID_IOlkEnum</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="0e8de-115">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="0e8de-115">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="0e8de-116">GetCount</span><span class="sxs-lookup"><span data-stu-id="0e8de-116">GetCount</span></span>](iolkenum-getcount.md) <br/> |<span data-ttu-id="0e8de-117">Obtient le nombre de comptes dans l'énumérateur.</span><span class="sxs-lookup"><span data-stu-id="0e8de-117">Gets the number of accounts in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="0e8de-118">Reset</span><span class="sxs-lookup"><span data-stu-id="0e8de-118">Reset</span></span>](iolkenum-reset.md) <br/> |<span data-ttu-id="0e8de-119">Rétablit l'énumérateur au début.</span><span class="sxs-lookup"><span data-stu-id="0e8de-119">Resets the enumerator to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="0e8de-120">GetNext</span><span class="sxs-lookup"><span data-stu-id="0e8de-120">GetNext</span></span>](iolkenum-getnext.md) <br/> |<span data-ttu-id="0e8de-121">Obtient le compte suivant dans l'énumérateur.</span><span class="sxs-lookup"><span data-stu-id="0e8de-121">Gets the next account in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="0e8de-122">Skip</span><span class="sxs-lookup"><span data-stu-id="0e8de-122">Skip</span></span>](iolkenum-skip.md) <br/> |<span data-ttu-id="0e8de-123">Ignore un nombre spécifié de comptes dans l'énumérateur.</span><span class="sxs-lookup"><span data-stu-id="0e8de-123">Skips a specified number of accounts in the enumerator.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e8de-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="0e8de-124">Remarks</span></span>

<span data-ttu-id="0e8de-125">Cette interface est renvoyée par **IOlkAccountManager:: EnumerateAccounts** lors de l'obtention d'un énumérateur de comptes.</span><span class="sxs-lookup"><span data-stu-id="0e8de-125">This interface is returned by **IOlkAccountManager::EnumerateAccounts** when obtaining an enumerator of accounts.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0e8de-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e8de-126">See also</span></span>

- [<span data-ttu-id="0e8de-127">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="0e8de-127">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="0e8de-128">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="0e8de-128">Constants (Account management API)</span></span>](constants-account-management-api.md)

