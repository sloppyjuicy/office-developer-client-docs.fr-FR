---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 59f43e8b3b0819b0178d60fa357e01937ae19d81
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389735"
---
# <a name="iolkenum"></a><span data-ttu-id="a668d-102">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="a668d-102">IOlkEnum</span></span>

<span data-ttu-id="a668d-103">Prend en charge l’énumération des comptes en tant qu’objets [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a668d-103">Supports enumerating accounts as [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) objects.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a668d-104">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="a668d-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a668d-105">Hérite de :</span><span class="sxs-lookup"><span data-stu-id="a668d-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="a668d-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="a668d-106">IUnknown</span></span>](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|<span data-ttu-id="a668d-107">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="a668d-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="a668d-108">Outlook</span><span class="sxs-lookup"><span data-stu-id="a668d-108">Outlook</span></span>  <br/> |
|<span data-ttu-id="a668d-109">Fourni par :</span><span class="sxs-lookup"><span data-stu-id="a668d-109">Provided by:</span></span>  <br/> |[<span data-ttu-id="a668d-110">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="a668d-110">IOlkAccountManager::EnumerateAccounts</span></span>](iolkaccountmanager-enumerateaccounts.md) <br/> |
|<span data-ttu-id="a668d-111">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="a668d-111">Called by:</span></span>  <br/> |<span data-ttu-id="a668d-112">Client</span><span class="sxs-lookup"><span data-stu-id="a668d-112">Client</span></span>  <br/> |
|<span data-ttu-id="a668d-113">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="a668d-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a668d-114">IID_IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="a668d-114">IID_IOlkEnum</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a668d-115">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="a668d-115">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a668d-116">GetCount</span><span class="sxs-lookup"><span data-stu-id="a668d-116">GetCount</span></span>](iolkenum-getcount.md) <br/> |<span data-ttu-id="a668d-117">Obtient le nombre de comptes dans l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="a668d-117">Gets the number of accounts in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="a668d-118">Reset</span><span class="sxs-lookup"><span data-stu-id="a668d-118">Reset</span></span>](iolkenum-reset.md) <br/> |<span data-ttu-id="a668d-119">Réinitialise l’énumérateur au début.</span><span class="sxs-lookup"><span data-stu-id="a668d-119">Resets the enumerator to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="a668d-120">GetNext</span><span class="sxs-lookup"><span data-stu-id="a668d-120">GetNext</span></span>](iolkenum-getnext.md) <br/> |<span data-ttu-id="a668d-121">Obtient le compte suivant dans l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="a668d-121">Gets the next account in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="a668d-122">Ignorer</span><span class="sxs-lookup"><span data-stu-id="a668d-122">Skip</span></span>](iolkenum-skip.md) <br/> |<span data-ttu-id="a668d-123">Ignore un nombre spécifié de comptes dans l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="a668d-123">Skips a specified number of accounts in the enumerator.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a668d-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="a668d-124">Remarks</span></span>

<span data-ttu-id="a668d-125">Cette interface est retournée par **IOlkAccountManager::EnumerateAccounts** lors de l’obtention d’un énumérateur de comptes.</span><span class="sxs-lookup"><span data-stu-id="a668d-125">This interface is returned by **IOlkAccountManager::EnumerateAccounts** when obtaining an enumerator of accounts.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a668d-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a668d-126">See also</span></span>

- [<span data-ttu-id="a668d-127">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="a668d-127">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="a668d-128">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="a668d-128">Constants (Account management API)</span></span>](constants-account-management-api.md)

