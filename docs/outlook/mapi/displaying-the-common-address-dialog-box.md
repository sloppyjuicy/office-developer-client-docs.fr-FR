---
title: Affichage de la boîte de dialogue adresse commune
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 276f9fa8-c333-4381-b20f-22fe9d2f27cd
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 812c850d1fcb6d3712d76b160b56b839b2e1353d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436902"
---
# <a name="displaying-the-common-address-dialog-box"></a><span data-ttu-id="bd722-103">Affichage de la boîte de dialogue adresse commune</span><span class="sxs-lookup"><span data-stu-id="bd722-103">Displaying the Common Address Dialog Box</span></span>

  
  
<span data-ttu-id="bd722-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd722-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd722-105">La boîte de dialogue adresse commune MAPI peut être utilisée pour diverses tâches d'adressage telles que la création d'une liste de destinataires.</span><span class="sxs-lookup"><span data-stu-id="bd722-105">The MAPI common address dialog box can be used for a variety of addressing tasks such as constructing a recipient list.</span></span> <span data-ttu-id="bd722-106">Pour afficher cette boîte de dialogue, appelez **IAddrBook:: Address**.</span><span class="sxs-lookup"><span data-stu-id="bd722-106">To display this dialog box, call **IAddrBook::Address**.</span></span> <span data-ttu-id="bd722-107">Selon le nombre de paramètres que vous définissez et la façon dont vous les définissez, vous pouvez limiter l'affichage aux entrées d'un type particulier à partir d'un conteneur particulier.</span><span class="sxs-lookup"><span data-stu-id="bd722-107">Depending on which of the many parameters you set and how you set them, you can limit your display to entries of a particular type from a particular container.</span></span>
  
 <span data-ttu-id="bd722-108">**Pour limiter la boîte de dialogue d'adresses à l'affichage des entrées du carnet d'adresses personnel uniquement**</span><span class="sxs-lookup"><span data-stu-id="bd722-108">**To limit the address dialog box to displaying personal address book (PAB) entries only**</span></span>
  
1. <span data-ttu-id="bd722-109">Appelez [IAddrBook:: GetPAB](iaddrbook-getpab.md) pour récupérer l'identificateur d'entrée du PAB.</span><span class="sxs-lookup"><span data-stu-id="bd722-109">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> 
    
2. <span data-ttu-id="bd722-110">Créez une restriction de propriété qui utilise RELOP_EQ pour le membre **RELOP** de la structure [SPropertyRestriction](spropertyrestriction.md) et soit **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), soit **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) comme membre **ulPropTag** .</span><span class="sxs-lookup"><span data-stu-id="bd722-110">Create a property restriction that uses RELOP_EQ for the **relop** member of the [SPropertyRestriction](spropertyrestriction.md) structure and either **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) or **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) as the **ulPropTag** member.</span></span> <span data-ttu-id="bd722-111">Si vous utilisez **PR_ENTRYID**, transmettez l'identificateur d'entrée extrait de **GetPAB**.</span><span class="sxs-lookup"><span data-stu-id="bd722-111">If you use **PR_ENTRYID**, pass the entry identifier retrieved from **GetPAB**.</span></span> <span data-ttu-id="bd722-112">Si vous utilisez **PR_AB_PROVIDER_ID**, transmettez la valeur incluse dans le MSPAB. Fichier d'en-tête H.</span><span class="sxs-lookup"><span data-stu-id="bd722-112">If you use **PR_AB_PROVIDER_ID**, pass the value included in the MSPAB.H header file.</span></span> <span data-ttu-id="bd722-113">**PR_AB_PROVIDER_ID** est l'identificateur unique du carnet d'adresse (PAB) conçu par MAPI.</span><span class="sxs-lookup"><span data-stu-id="bd722-113">**PR_AB_PROVIDER_ID** is the unique identifier for the PAB designed by MAPI.</span></span> 
    
3. <span data-ttu-id="bd722-114">Appelez [IAddrBook:: Address](iaddrbook-address.md) avec le paramètre _lpHierRestriction_ pointant vers la restriction de propriété.</span><span class="sxs-lookup"><span data-stu-id="bd722-114">Call [IAddrBook::Address](iaddrbook-address.md) with the  _lpHierRestriction_ parameter pointing to the property restriction.</span></span> 
    

