---
title: IOlkAccountHelperGetIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea8b8f02-959f-cd71-9cfe-5ebdf4bae2bc
description: Obtient le nom du profil d’un compte.
ms.openlocfilehash: d725f309a29b026395e2795a49d31b45a4a49562
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400137"
---
# <a name="iolkaccounthelpergetidentity"></a><span data-ttu-id="db047-103">IOlkAccountHelper::GetIdentity</span><span class="sxs-lookup"><span data-stu-id="db047-103">IOlkAccountHelper::GetIdentity</span></span>

<span data-ttu-id="db047-104">Obtient le nom du profil d’un compte.</span><span class="sxs-lookup"><span data-stu-id="db047-104">Gets the profile name of an account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="db047-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="db047-105">Quick info</span></span>

<span data-ttu-id="db047-106">Voir [IOlkAccountHelper](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="db047-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::GetIdentity (  
    LPWSTR pwszIdentity, 
    DWORD *pcch 
);
```

## <a name="parameters"></a><span data-ttu-id="db047-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db047-107">Parameters</span></span>

<span data-ttu-id="db047-108">_pwszIdentity_</span><span class="sxs-lookup"><span data-stu-id="db047-108">_pwszIdentity_</span></span>
  
> <span data-ttu-id="db047-109">[in] [out] Nom du profil.</span><span class="sxs-lookup"><span data-stu-id="db047-109">[in][out] The profile name.</span></span>
    
<span data-ttu-id="db047-110">_pcch_</span><span class="sxs-lookup"><span data-stu-id="db047-110">_pcch_</span></span>
  
> <span data-ttu-id="db047-111">[in] [out] Lors de l’appel de cette méthode contient la taille (en nombre de caractères) de _pwszIdentity_ qui a été affectée.</span><span class="sxs-lookup"><span data-stu-id="db047-111">[in] [out] Upon calling this method, contains the size (in number of characters) of  _pwszIdentity_ that has been allocated.</span></span> <span data-ttu-id="db047-112">Au retour, contient la longueur réelle, y compris le caractère de fin de 0, le nom de profil retourné.</span><span class="sxs-lookup"><span data-stu-id="db047-112">Upon return, contains the actual length, including the 0-terminating character, of the returned profile name.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="db047-113">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="db047-113">Return values</span></span>

|<span data-ttu-id="db047-114">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="db047-114">**HRESULT**</span></span>|<span data-ttu-id="db047-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="db047-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="db047-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="db047-116">S_OK</span></span>  <br/> |<span data-ttu-id="db047-117">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="db047-117">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="db047-118">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="db047-118">E_OUTOFMEMORY</span></span>  <br/> |<span data-ttu-id="db047-119">Le nom du profil retourné est supérieure à la taille de _pwszIdentity_.</span><span class="sxs-lookup"><span data-stu-id="db047-119">The returned profile name is longer than the size of  _pwszIdentity_.</span></span>  <br/> |
|<span data-ttu-id="db047-120">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="db047-120">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="db047-121">_pcch_ est NULL.</span><span class="sxs-lookup"><span data-stu-id="db047-121">_pcch_ is NULL.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db047-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="db047-122">Remarks</span></span>

<span data-ttu-id="db047-123">Si _pwszIdentity_ est trop petit pour contenir le nom du profil, ne sera pas être défini sur retour et pointe vers la taille requise pour _pwszIdentity_ _pcch_ .</span><span class="sxs-lookup"><span data-stu-id="db047-123">If  _pwszIdentity_ is too small to hold the profile name, it will not be set on return, and  _pcch_ will point to the size required for  _pwszIdentity_.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="db047-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db047-124">See also</span></span>

- [<span data-ttu-id="db047-125">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="db047-125">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="db047-126">PidTagProfileName</span><span class="sxs-lookup"><span data-stu-id="db047-126">PidTagProfileName</span></span>](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx)

