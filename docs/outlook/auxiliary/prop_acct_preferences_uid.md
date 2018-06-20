---
title: PROP_ACCT_PREFERENCES_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ec0aac33-624e-48f7-8177-8f7b8db6af7d
description: Récupère l’identificateur unique (UID) de la section profil qui stocke les préférences.
ms.openlocfilehash: 70e61264e5525f26e9f52e402bc785b544a0b90e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782818"
---
# <a name="propacctpreferencesuid"></a><span data-ttu-id="3f071-103">PROP_ACCT_PREFERENCES_UID</span><span class="sxs-lookup"><span data-stu-id="3f071-103">PROP_ACCT_PREFERENCES_UID</span></span>

<span data-ttu-id="3f071-104">Récupère l’identificateur unique (UID) de la section profil qui stocke les préférences.</span><span class="sxs-lookup"><span data-stu-id="3f071-104">Retrieves the unique identifier (UID) for the profile section that stores the account preferences.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="3f071-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="3f071-105">Quick info</span></span>

<span data-ttu-id="3f071-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="3f071-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3f071-107">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="3f071-107">Identifier:</span></span>  <br/> |<span data-ttu-id="3f071-108">0 x 0022</span><span class="sxs-lookup"><span data-stu-id="3f071-108">0x0022</span></span>  <br/> |
|<span data-ttu-id="3f071-109">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="3f071-109">Property type:</span></span>  <br/> |<span data-ttu-id="3f071-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3f071-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3f071-111">Balise de propriété :</span><span class="sxs-lookup"><span data-stu-id="3f071-111">Property tag:</span></span>  <br/> |<span data-ttu-id="3f071-112">0x00220102</span><span class="sxs-lookup"><span data-stu-id="3f071-112">0x00220102</span></span>  <br/> |
|<span data-ttu-id="3f071-113">Access :</span><span class="sxs-lookup"><span data-stu-id="3f071-113">Access:</span></span>  <br/> |<span data-ttu-id="3f071-114">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f071-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3f071-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="3f071-115">Remarks</span></span>

<span data-ttu-id="3f071-116">Utilisez **PROP_ACCT_PREFERENCES_UID** dans les appels à [IMAPISupport::OpenProfileSection](http://msdn.microsoft.com/library/cd1fa994-9531-46c4-94e5-505e7f90b884%28Office.15%29.aspx) pour récupérer la section profil qui contient les préférences du compte.</span><span class="sxs-lookup"><span data-stu-id="3f071-116">Use **PROP_ACCT_PREFERENCES_UID** in calls to [IMAPISupport::OpenProfileSection](http://msdn.microsoft.com/library/cd1fa994-9531-46c4-94e5-505e7f90b884%28Office.15%29.aspx) to retrieve the profile section that contains account preferences.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3f071-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f071-117">See also</span></span>

- [<span data-ttu-id="3f071-118">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="3f071-118">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="3f071-119">À propos des paramètres anti-spam</span><span class="sxs-lookup"><span data-stu-id="3f071-119">About anti-spam settings</span></span>](about-anti-spam-settings.md)

