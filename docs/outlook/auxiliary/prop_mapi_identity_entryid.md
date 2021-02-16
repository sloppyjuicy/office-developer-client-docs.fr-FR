---
title: PROP_MAPI_IDENTITY_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c64db8ea-d6ad-4fb9-97aa-958e5a0daf8f
description: Récupère ou définit l’ID d’entrée du carnet d’adresses pour le compte.
ms.openlocfilehash: 2352f64b46e9884e95b7bf1f3693321f7cd224ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326431"
---
# <a name="prop_mapi_identity_entryid"></a><span data-ttu-id="248bc-103">PROP_MAPI_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="248bc-103">PROP_MAPI_IDENTITY_ENTRYID</span></span>

<span data-ttu-id="248bc-104">Récupère ou définit l’ID d’entrée du carnet d’adresses pour le compte.</span><span class="sxs-lookup"><span data-stu-id="248bc-104">Retrieves or sets the address book entry ID for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="248bc-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="248bc-105">Quick info</span></span>

<span data-ttu-id="248bc-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="248bc-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="248bc-107">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="248bc-107">Identifier:</span></span>  <br/> |<span data-ttu-id="248bc-108">0x2002</span><span class="sxs-lookup"><span data-stu-id="248bc-108">0x2002</span></span>  <br/> |
|<span data-ttu-id="248bc-109">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="248bc-109">Property type:</span></span>  <br/> |<span data-ttu-id="248bc-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="248bc-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="248bc-111">Balise de propriété :</span><span class="sxs-lookup"><span data-stu-id="248bc-111">Property tag:</span></span>  <br/> |<span data-ttu-id="248bc-112">0x20020102</span><span class="sxs-lookup"><span data-stu-id="248bc-112">0x20020102</span></span>  <br/> |
|<span data-ttu-id="248bc-113">Accès :</span><span class="sxs-lookup"><span data-stu-id="248bc-113">Access:</span></span>  <br/> |<span data-ttu-id="248bc-114">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="248bc-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="248bc-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="248bc-115">Remarks</span></span>

 <span data-ttu-id="248bc-116">**PROP \_ MAPI \_ IDENTITY \_ ENTRYID n’est** pas censé exister sur chaque compte.</span><span class="sxs-lookup"><span data-stu-id="248bc-116">**PROP\_MAPI\_IDENTITY\_ENTRYID** is not expected to exist on every account.</span></span> <span data-ttu-id="248bc-117">Par exemple, un compte Exchange peut avoir **PROP \_ MAPI \_ IDENTITY \_ ENTRYID** définie et non [PROP \_ ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md), tandis que pour un compte SMTP/POP3, la situation est inversée.</span><span class="sxs-lookup"><span data-stu-id="248bc-117">For example, an Exchange account could have **PROP\_MAPI\_IDENTITY\_ENTRYID** set and not [PROP\_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md), while for an SMTP/POP3 account the situation is reversed.</span></span> <span data-ttu-id="248bc-118">**PROP \_ MAPI_IDENTITY_ENTRYID** renvoie un ID d’entrée similaire à la valeur renvoyée par  _lppEntryID_ dans [IMAPISession::QueryIdentity](https://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="248bc-118">**PROP\_MAPI_IDENTITY_ENTRYID** returns an entry ID that is similar to the value returned by  _lppEntryID_ in [IMAPISession::QueryIdentity](https://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="248bc-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="248bc-119">See also</span></span>

- [<span data-ttu-id="248bc-120">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="248bc-120">About the Account Management API</span></span>](about-the-account-management-api.md)

