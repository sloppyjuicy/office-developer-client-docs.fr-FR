---
title: À propos des paramètres anti-courrier indésirable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 04e00e49-c12d-4517-8574-410741d0fa06
description: Outlook permet aux utilisateurs de spécifier les paramètres pour chaque compte pour vous aider à protéger le compte du courrier indésirable. Ces paramètres anti-courrier indésirable sont stockés dans une section désignée pour ce compte dans le profil utilisateur.
ms.openlocfilehash: cf9bce058e9e0bd1c8f6f14637ae0af73f155940
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390379"
---
# <a name="about-anti-spam-settings"></a><span data-ttu-id="a6424-104">À propos des paramètres anti-courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="a6424-104">About anti-spam settings</span></span>

<span data-ttu-id="a6424-105">Outlook permet aux utilisateurs de spécifier les paramètres pour chaque compte pour vous aider à protéger le compte du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="a6424-105">Outlook allows users to specify settings for each account to help protect the account from spam.</span></span> <span data-ttu-id="a6424-106">Ces paramètres anti-courrier indésirable sont stockés dans une section désignée pour ce compte dans le profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a6424-106">Such anti-spam settings are stored in a section designated for that account in the user's profile.</span></span> <span data-ttu-id="a6424-107">Utilisez la propriété [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) pour obtenir l’ID unique (UID) de la section dans le profil qui stocke les préférences de l’utilisateur pour ce compte, y compris les paramètres de blocage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="a6424-107">Use the [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) property to obtain the unique ID (UID) for the section in the profile that stores the user's preferences for this account, including the anti-spam settings.</span></span> 
  
<span data-ttu-id="a6424-108">Pour obtenir les paramètres de blocage du courrier indésirable pour le compte, utilisez les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="a6424-108">Use the following properties to obtain anti-spam settings for the account:</span></span>
  
- <span data-ttu-id="a6424-109">[PidTagSpamJunkSenders](https://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)— spécifie une liste délimitée par des points-virgules d’adresses de messagerie et les domaines qui l’utilisateur a spécifié en tant que des expéditeurs bloqués pour le compte.</span><span class="sxs-lookup"><span data-stu-id="a6424-109">[PidTagSpamJunkSenders](https://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as blocked senders for the account.</span></span>
    
- <span data-ttu-id="a6424-110">[PidTagSpamThreshold](https://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)— Spécifie le niveau de filtrage que l’utilisateur a spécifié pour le compte.</span><span class="sxs-lookup"><span data-stu-id="a6424-110">[PidTagSpamThreshold](https://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)—Specifies the level of spam-filtering that the user has specified for the account.</span></span> <span data-ttu-id="a6424-111">Le tableau suivant présente les valeurs prises en charge.</span><span class="sxs-lookup"><span data-stu-id="a6424-111">The following table shows the supported values.</span></span>
    
|<span data-ttu-id="a6424-112">Valeur prise en charge</span><span class="sxs-lookup"><span data-stu-id="a6424-112">Supported value</span></span> |<span data-ttu-id="a6424-113">Définition</span><span class="sxs-lookup"><span data-stu-id="a6424-113">Definition</span></span> |
|:-----|:-----|
|<span data-ttu-id="a6424-114">Aucune</span><span class="sxs-lookup"><span data-stu-id="a6424-114">None</span></span>  <br/> |<span data-ttu-id="a6424-115">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="a6424-115">0xFFFFFFFF</span></span>  <br/> |
|<span data-ttu-id="a6424-116">Low</span><span class="sxs-lookup"><span data-stu-id="a6424-116">Low</span></span>  <br/> |<span data-ttu-id="a6424-117">0 x 00000006</span><span class="sxs-lookup"><span data-stu-id="a6424-117">0x00000006</span></span>  <br/> |
|<span data-ttu-id="a6424-118">Moyenne</span><span class="sxs-lookup"><span data-stu-id="a6424-118">Medium</span></span>  <br/> |<span data-ttu-id="a6424-119">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="a6424-119">0x00000005</span></span>  <br/> |
|<span data-ttu-id="a6424-120">High</span><span class="sxs-lookup"><span data-stu-id="a6424-120">High</span></span>  <br/> |<span data-ttu-id="a6424-121">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="a6424-121">0x00000003</span></span>  <br/> |
   
- <span data-ttu-id="a6424-122">[PidTagSpamTrustedRecipients](https://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)— spécifie une liste délimitée par des points-virgules d’adresses de messagerie et les domaines qui l’utilisateur a spécifié comme destinataires approuvés pour le compte.</span><span class="sxs-lookup"><span data-stu-id="a6424-122">[PidTagSpamTrustedRecipients](https://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as trusted recipients for the account.</span></span>
    
- <span data-ttu-id="a6424-123">[PidTagSpamTrustedSenders](https://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)— spécifie une liste délimitée par des points-virgules d’adresses de messagerie et les domaines qui l’utilisateur a spécifié comme des expéditeurs approuvés pour le compte.</span><span class="sxs-lookup"><span data-stu-id="a6424-123">[PidTagSpamTrustedSenders](https://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as trusted senders for the account.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a6424-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6424-124">See also</span></span>

- [<span data-ttu-id="a6424-125">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="a6424-125">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="a6424-126">Ajouter des noms aux listes de filtre de courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="a6424-126">Add names to the Junk Email Filter lists</span></span>](https://office.microsoft.com/en-us/outlook-help/add-names-to-the-junk-email-filter-lists-HA010355043.aspx?CTT=1)

