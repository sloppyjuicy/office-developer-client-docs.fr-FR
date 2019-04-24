---
title: PROP_MAPI_EMSMDB_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8e5b42e3-844f-488c-ba6f-b74c447b1d59
description: Représente une structure ACCT_BIN qui contient l'UID d'un compte Exchange.
ms.openlocfilehash: 6bb529da82cc24e41ddc70c5031f84050a2ece25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326550"
---
# <a name="propmapiemsmdbuid"></a><span data-ttu-id="5a954-103">PROP_MAPI_EMSMDB_UID</span><span class="sxs-lookup"><span data-stu-id="5a954-103">PROP_MAPI_EMSMDB_UID</span></span>

<span data-ttu-id="5a954-104">Représente une structure [ACCT_BIN](acct_bin.md) qui contient l'UID d'un compte Exchange.</span><span class="sxs-lookup"><span data-stu-id="5a954-104">Represents an [ACCT_BIN](acct_bin.md) structure that contains the UID of an Exchange account.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="5a954-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="5a954-105">Quick info</span></span>

<span data-ttu-id="5a954-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="5a954-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5a954-107">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="5a954-107">Identifier:</span></span>  <br/> |<span data-ttu-id="5a954-108">0x2009</span><span class="sxs-lookup"><span data-stu-id="5a954-108">0x2009</span></span>  <br/> |
|<span data-ttu-id="5a954-109">Type de propriété:</span><span class="sxs-lookup"><span data-stu-id="5a954-109">Property type:</span></span>  <br/> |<span data-ttu-id="5a954-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5a954-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5a954-111">Balise de propriété:</span><span class="sxs-lookup"><span data-stu-id="5a954-111">Property tag:</span></span>  <br/> |<span data-ttu-id="5a954-112">0x20090102</span><span class="sxs-lookup"><span data-stu-id="5a954-112">0x20090102</span></span>  <br/> |
|<span data-ttu-id="5a954-113">Access</span><span class="sxs-lookup"><span data-stu-id="5a954-113">Access:</span></span>  <br/> |<span data-ttu-id="5a954-114">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a954-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a954-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="5a954-115">Remarks</span></span>

<span data-ttu-id="5a954-116">Obtenez cette propriété à l'aide de [IOlkAccount:: getprop](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="5a954-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span>
  
<span data-ttu-id="5a954-117">Utilisez [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) pour vérifier s'il s'agit d'un compte Exchange.</span><span class="sxs-lookup"><span data-stu-id="5a954-117">Use [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) to verify if the account is an Exchange account.</span></span> <span data-ttu-id="5a954-118">Si c'est le cas, **prop\_MAPI_EMSMDB_UID** est un **ACCT_BIN** qui contient l' **emsmdbUID**, qui est l'ID unique, pour le compte Exchange.</span><span class="sxs-lookup"><span data-stu-id="5a954-118">If it is, **PROP\_MAPI_EMSMDB_UID** is an **ACCT_BIN** that contains the **emsmdbUID**, which is the unique ID, for the Exchange account.</span></span> <span data-ttu-id="5a954-119">Si le compte n'est pas un compte Exchange, cette propriété n'est pas définie.</span><span class="sxs-lookup"><span data-stu-id="5a954-119">If the account is not an Exchange account, this property is undefined.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5a954-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a954-120">See also</span></span>

- [<span data-ttu-id="5a954-121">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="5a954-121">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="5a954-122">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="5a954-122">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="5a954-123">Utilisation de plusieurs comptes Exchange</span><span class="sxs-lookup"><span data-stu-id="5a954-123">Using Multiple Exchange Accounts</span></span>](https://msdn.microsoft.com/library/4e1804bf-4c50-4942-a7ab-9a8caf1be7e5%28Office.15%29.aspx)  
- [<span data-ttu-id="5a954-124">Propri�t� canonique PidTagExchangeProfileSectionId</span><span class="sxs-lookup"><span data-stu-id="5a954-124">PidTagExchangeProfileSectionId Canonical Property</span></span>](https://msdn.microsoft.com/library/4ad2f417-be8f-4fc8-9321-82097289074b%28Office.15%29.aspx)

