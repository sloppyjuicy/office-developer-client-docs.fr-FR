---
title: Affichage de la boîte de dialogue d’adresse courante
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 276f9fa8-c333-4381-b20f-22fe9d2f27cd
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 00d1063310aaf1a8948e04d725d7e11418cf986c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592422"
---
# <a name="displaying-the-common-address-dialog-box"></a><span data-ttu-id="5029a-103">Affichage de la boîte de dialogue d’adresse courante</span><span class="sxs-lookup"><span data-stu-id="5029a-103">Displaying the Common Address Dialog Box</span></span>

  
  
<span data-ttu-id="5029a-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5029a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5029a-105">La boîte de dialogue adresse MAPI courantes pouvant servir à diverses tâches adressage telles que la création d’une liste de destinataires.</span><span class="sxs-lookup"><span data-stu-id="5029a-105">The MAPI common address dialog box can be used for a variety of addressing tasks such as constructing a recipient list.</span></span> <span data-ttu-id="5029a-106">Pour afficher cette boîte de dialogue, appelez **IAddrBook::Address**.</span><span class="sxs-lookup"><span data-stu-id="5029a-106">To display this dialog box, call **IAddrBook::Address**.</span></span> <span data-ttu-id="5029a-107">Selon parmi les nombreux paramètres que vous définissez et la façon dont vous les définissez, vous pouvez limiter l’affichage aux entrées d’un type particulier à partir d’un conteneur spécifique.</span><span class="sxs-lookup"><span data-stu-id="5029a-107">Depending on which of the many parameters you set and how you set them, you can limit your display to entries of a particular type from a particular container.</span></span>
  
 <span data-ttu-id="5029a-108">**Pour limiter la boîte de dialogue adresse à l’affichage des entrées de carnet d’adresses personnel uniquement**</span><span class="sxs-lookup"><span data-stu-id="5029a-108">**To limit the address dialog box to displaying personal address book (PAB) entries only**</span></span>
  
1. <span data-ttu-id="5029a-109">Appelez [IAddrBook::GetPAB](iaddrbook-getpab.md) pour récupérer l’identificateur d’entrée du carnet d’adresses personnel.</span><span class="sxs-lookup"><span data-stu-id="5029a-109">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> 
    
2. <span data-ttu-id="5029a-110">Créer une restriction de propriété qui utilise RELOP_EQ pour le membre de la structure [SPropertyRestriction](spropertyrestriction.md) et **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) ou **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) **relop** en tant que le membre **ulPropTag** .</span><span class="sxs-lookup"><span data-stu-id="5029a-110">Create a property restriction that uses RELOP_EQ for the **relop** member of the [SPropertyRestriction](spropertyrestriction.md) structure and either **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) or **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) as the **ulPropTag** member.</span></span> <span data-ttu-id="5029a-111">Si vous utilisez **PR_ENTRYID**, transmettez l’identificateur d’entrée est recherché dans **GetPAB**.</span><span class="sxs-lookup"><span data-stu-id="5029a-111">If you use **PR_ENTRYID**, pass the entry identifier retrieved from **GetPAB**.</span></span> <span data-ttu-id="5029a-112">Si vous utilisez **PR_AB_PROVIDER_ID**, passez la valeur incluse dans le MSPAB. Fichier d’en-tête H.</span><span class="sxs-lookup"><span data-stu-id="5029a-112">If you use **PR_AB_PROVIDER_ID**, pass the value included in the MSPAB.H header file.</span></span> <span data-ttu-id="5029a-113">**PR_AB_PROVIDER_ID** est l’identificateur unique pour le carnet d’adresses personnel conçu par MAPI.</span><span class="sxs-lookup"><span data-stu-id="5029a-113">**PR_AB_PROVIDER_ID** is the unique identifier for the PAB designed by MAPI.</span></span> 
    
3. <span data-ttu-id="5029a-114">Appelez [IAddrBook::Address](iaddrbook-address.md) avec le paramètre _lpHierRestriction_ en pointant sur la restriction de propriété.</span><span class="sxs-lookup"><span data-stu-id="5029a-114">Call [IAddrBook::Address](iaddrbook-address.md) with the  _lpHierRestriction_ parameter pointing to the property restriction.</span></span> 
    

