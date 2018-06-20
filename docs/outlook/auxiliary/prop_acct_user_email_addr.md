---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: Spécifie l’adresse de messagerie pour le compte.
ms.openlocfilehash: 7d0bbba2dcb104326c360da6a10f3e19d1740e46
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782817"
---
# <a name="propacctuseremailaddr"></a><span data-ttu-id="cf331-103">PROP_ACCT_USER_EMAIL_ADDR</span><span class="sxs-lookup"><span data-stu-id="cf331-103">PROP_ACCT_USER_EMAIL_ADDR</span></span>

<span data-ttu-id="cf331-104">Spécifie l’adresse de messagerie pour le compte.</span><span class="sxs-lookup"><span data-stu-id="cf331-104">Specifies the email address for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="cf331-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="cf331-105">Quick info</span></span>

<span data-ttu-id="cf331-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="cf331-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cf331-107">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="cf331-107">Identifier:</span></span>  <br/> |<span data-ttu-id="cf331-108">0x000C</span><span class="sxs-lookup"><span data-stu-id="cf331-108">0x000C</span></span>  <br/> |
|<span data-ttu-id="cf331-109">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="cf331-109">Property type:</span></span>  <br/> |<span data-ttu-id="cf331-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cf331-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="cf331-111">Balise de propriété :</span><span class="sxs-lookup"><span data-stu-id="cf331-111">Property tag:</span></span>  <br/> |<span data-ttu-id="cf331-112">0x000C001F</span><span class="sxs-lookup"><span data-stu-id="cf331-112">0x000C001F</span></span>  <br/> |
|<span data-ttu-id="cf331-113">Access :</span><span class="sxs-lookup"><span data-stu-id="cf331-113">Access:</span></span>  <br/> |<span data-ttu-id="cf331-114">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="cf331-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cf331-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="cf331-115">Remarks</span></span>

 <span data-ttu-id="cf331-116">**PROP_ACCT_USER_EMAIL_ADDR** n’est pas censé exister sur chaque compte.</span><span class="sxs-lookup"><span data-stu-id="cf331-116">**PROP_ACCT_USER_EMAIL_ADDR** is not expected to exist on every account.</span></span> <span data-ttu-id="cf331-117">Par exemple, un compte Exchange peut avoir [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) mais pas **PROP_ACCT_USER_EMAIL_ADDR**, tandis que pour un compte SMTP/POP3, la situation est inversée.</span><span class="sxs-lookup"><span data-stu-id="cf331-117">For example, an Exchange account could have [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) but not **PROP_ACCT_USER_EMAIL_ADDR**, while for an SMTP/POP3 account, the situation is reversed.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cf331-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf331-118">See also</span></span>

- [<span data-ttu-id="cf331-119">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="cf331-119">About the Account Management API</span></span>](about-the-account-management-api.md)

