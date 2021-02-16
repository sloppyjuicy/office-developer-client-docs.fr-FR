---
title: À propos des paramètres anti-courrier indésirable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 04e00e49-c12d-4517-8574-410741d0fa06
description: Outlook permet aux utilisateurs de spécifier des paramètres pour chaque compte afin de protéger le compte contre le courrier indésirable. Ces paramètres anti-courrier indésirable sont stockés dans une section désignée pour ce compte dans le profil de l’utilisateur.
ms.openlocfilehash: cf9bce058e9e0bd1c8f6f14637ae0af73f155940
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316960"
---
# <a name="about-anti-spam-settings"></a><span data-ttu-id="5f898-104">À propos des paramètres anti-courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="5f898-104">About anti-spam settings</span></span>

<span data-ttu-id="5f898-105">Outlook permet aux utilisateurs de spécifier des paramètres pour chaque compte afin de protéger le compte contre le courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="5f898-105">Outlook allows users to specify settings for each account to help protect the account from spam.</span></span> <span data-ttu-id="5f898-106">Ces paramètres anti-courrier indésirable sont stockés dans une section désignée pour ce compte dans le profil de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5f898-106">Such anti-spam settings are stored in a section designated for that account in the user's profile.</span></span> <span data-ttu-id="5f898-107">Utilisez la [propriété PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) pour obtenir l’ID unique (UID) de la section du profil qui stocke les préférences de l’utilisateur pour ce compte, y compris les paramètres anti-courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="5f898-107">Use the [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) property to obtain the unique ID (UID) for the section in the profile that stores the user's preferences for this account, including the anti-spam settings.</span></span> 
  
<span data-ttu-id="5f898-108">Utilisez les propriétés suivantes pour obtenir les paramètres anti-courrier indésirable pour le compte :</span><span class="sxs-lookup"><span data-stu-id="5f898-108">Use the following properties to obtain anti-spam settings for the account:</span></span>
  
- <span data-ttu-id="5f898-109">[PidTagSpamJunkSenders](https://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx): spécifie une liste délimitée par des points-virgules d’adresses e-mail et de domaines que l’utilisateur a spécifiés comme expéditeurs bloqués pour le compte.</span><span class="sxs-lookup"><span data-stu-id="5f898-109">[PidTagSpamJunkSenders](https://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as blocked senders for the account.</span></span>
    
- <span data-ttu-id="5f898-110">[PidTagSpamThreshold](https://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx): spécifie le niveau de filtrage du courrier indésirable que l’utilisateur a spécifié pour le compte.</span><span class="sxs-lookup"><span data-stu-id="5f898-110">[PidTagSpamThreshold](https://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)—Specifies the level of spam-filtering that the user has specified for the account.</span></span> <span data-ttu-id="5f898-111">Le tableau suivant indique les valeurs pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5f898-111">The following table shows the supported values.</span></span>
    
|<span data-ttu-id="5f898-112">Valeur prise en charge</span><span class="sxs-lookup"><span data-stu-id="5f898-112">Supported value</span></span> |<span data-ttu-id="5f898-113">Définition</span><span class="sxs-lookup"><span data-stu-id="5f898-113">Definition</span></span> |
|:-----|:-----|
|<span data-ttu-id="5f898-114">Aucun</span><span class="sxs-lookup"><span data-stu-id="5f898-114">None</span></span>  <br/> |<span data-ttu-id="5f898-115">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="5f898-115">0xFFFFFFFF</span></span>  <br/> |
|<span data-ttu-id="5f898-116">Faible</span><span class="sxs-lookup"><span data-stu-id="5f898-116">Low</span></span>  <br/> |<span data-ttu-id="5f898-117">0x00000006</span><span class="sxs-lookup"><span data-stu-id="5f898-117">0x00000006</span></span>  <br/> |
|<span data-ttu-id="5f898-118">Moyen</span><span class="sxs-lookup"><span data-stu-id="5f898-118">Medium</span></span>  <br/> |<span data-ttu-id="5f898-119">0x00000005</span><span class="sxs-lookup"><span data-stu-id="5f898-119">0x00000005</span></span>  <br/> |
|<span data-ttu-id="5f898-120">Élevé</span><span class="sxs-lookup"><span data-stu-id="5f898-120">High</span></span>  <br/> |<span data-ttu-id="5f898-121">0x00000003</span><span class="sxs-lookup"><span data-stu-id="5f898-121">0x00000003</span></span>  <br/> |
   
- <span data-ttu-id="5f898-122">[PidTagSpamTrustedRecipients](https://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx): spécifie une liste délimitée par des points-virgules d’adresses e-mail et de domaines que l’utilisateur a spécifiés comme destinataires fiables pour le compte.</span><span class="sxs-lookup"><span data-stu-id="5f898-122">[PidTagSpamTrustedRecipients](https://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as trusted recipients for the account.</span></span>
    
- <span data-ttu-id="5f898-123">[PidTagSpamTrustedSenders](https://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx): spécifie une liste délimitée par des points-virgules d’adresses e-mail et de domaines que l’utilisateur a spécifiés comme expéditeurs fiables pour le compte.</span><span class="sxs-lookup"><span data-stu-id="5f898-123">[PidTagSpamTrustedSenders](https://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as trusted senders for the account.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5f898-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f898-124">See also</span></span>

- [<span data-ttu-id="5f898-125">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="5f898-125">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="5f898-126">Ajouter des noms aux listes de filtres de courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="5f898-126">Add names to the Junk Email Filter lists</span></span>](https://office.microsoft.com/en-us/outlook-help/add-names-to-the-junk-email-filter-lists-HA010355043.aspx?CTT=1)

