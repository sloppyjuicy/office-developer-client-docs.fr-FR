---
title: PROP_MAPI_EMSMDB_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8e5b42e3-844f-488c-ba6f-b74c447b1d59
description: Représente une structure ACCT_BIN qui contient l’UID d’un compte Exchange.
ms.openlocfilehash: 05e2e61601a08e0cb6f6dc99d265f12a10b19d3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782834"
---
# <a name="propmapiemsmdbuid"></a><span data-ttu-id="43f2c-103">PROP_MAPI_EMSMDB_UID</span><span class="sxs-lookup"><span data-stu-id="43f2c-103">PROP_MAPI_EMSMDB_UID</span></span>

<span data-ttu-id="43f2c-104">Représente une structure [ACCT_BIN](acct_bin.md) qui contient l’UID d’un compte Exchange.</span><span class="sxs-lookup"><span data-stu-id="43f2c-104">Represents an [ACCT_BIN](acct_bin.md) structure that contains the UID of an Exchange account.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="43f2c-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="43f2c-105">Quick info</span></span>

<span data-ttu-id="43f2c-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="43f2c-107">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="43f2c-107">Identifier:</span></span>  <br/> |<span data-ttu-id="43f2c-108">0x2009</span><span class="sxs-lookup"><span data-stu-id="43f2c-108">0x2009</span></span>  <br/> |
|<span data-ttu-id="43f2c-109">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="43f2c-109">Property type:</span></span>  <br/> |<span data-ttu-id="43f2c-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="43f2c-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="43f2c-111">Balise de propriété :</span><span class="sxs-lookup"><span data-stu-id="43f2c-111">Property tag:</span></span>  <br/> |<span data-ttu-id="43f2c-112">0x20090102</span><span class="sxs-lookup"><span data-stu-id="43f2c-112">0x20090102</span></span>  <br/> |
|<span data-ttu-id="43f2c-113">Access :</span><span class="sxs-lookup"><span data-stu-id="43f2c-113">Access:</span></span>  <br/> |<span data-ttu-id="43f2c-114">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="43f2c-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43f2c-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="43f2c-115">Remarks</span></span>

<span data-ttu-id="43f2c-116">Obtenez cette propriété à l’aide de [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="43f2c-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span>
  
<span data-ttu-id="43f2c-117">Utilisez [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) pour vérifier si le compte est un compte Exchange.</span><span class="sxs-lookup"><span data-stu-id="43f2c-117">Use [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) to verify if the account is an Exchange account.</span></span> <span data-ttu-id="43f2c-118">S’il s’agit, **propriétés\_MAPI_EMSMDB_UID** est un **ACCT_BIN** contenant **emsmdbUID**, qui est l’ID unique, pour le compte Exchange.</span><span class="sxs-lookup"><span data-stu-id="43f2c-118">If it is, **PROP\_MAPI_EMSMDB_UID** is an **ACCT_BIN** that contains the **emsmdbUID**, which is the unique ID, for the Exchange account.</span></span> <span data-ttu-id="43f2c-119">Si le compte n’est pas un compte Exchange, cette propriété est non définie.</span><span class="sxs-lookup"><span data-stu-id="43f2c-119">If the account is not an Exchange account, this property is undefined.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="43f2c-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43f2c-120">See also</span></span>

- [<span data-ttu-id="43f2c-121">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="43f2c-121">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="43f2c-122">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="43f2c-122">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="43f2c-123">Utilisation de plusieurs comptes Exchange</span><span class="sxs-lookup"><span data-stu-id="43f2c-123">Using Multiple Exchange Accounts</span></span>](http://msdn.microsoft.com/library/4e1804bf-4c50-4942-a7ab-9a8caf1be7e5%28Office.15%29.aspx)  
- [<span data-ttu-id="43f2c-124">Propri�t� canonique PidTagExchangeProfileSectionId</span><span class="sxs-lookup"><span data-stu-id="43f2c-124">PidTagExchangeProfileSectionId Canonical Property</span></span>](http://msdn.microsoft.com/library/4ad2f417-be8f-4fc8-9321-82097289074b%28Office.15%29.aspx)

