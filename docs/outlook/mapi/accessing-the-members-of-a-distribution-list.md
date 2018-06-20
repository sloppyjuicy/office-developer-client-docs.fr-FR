---
title: Accès aux membres d’une liste de Distribution
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f724cac8-2d5d-42bc-a15e-99f77a99ce21
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 21975482c458998cbe158a84d535f911156ac392
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782881"
---
# <a name="accessing-the-members-of-a-distribution-list"></a><span data-ttu-id="1d014-103">Accès aux membres d’une liste de Distribution</span><span class="sxs-lookup"><span data-stu-id="1d014-103">Accessing the Members of a Distribution List</span></span>

  
  
<span data-ttu-id="1d014-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1d014-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="1d014-105">**Pour obtenir les membres d’une liste de distribution**</span><span class="sxs-lookup"><span data-stu-id="1d014-105">**To get the members of a distribution list**</span></span>
  
1. <span data-ttu-id="1d014-106">Créer un tableau de balise de propriété ajustés avec les propriétés des membres que vous souhaitez récupérer, comme **PR_DISPLAY_TYPE** ([ , **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) et **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1d014-106">Create a sized property tag array with the properties of the members you would like to retrieve, such as **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), and **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="1d014-107">Appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md) pour ouvrir la liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="1d014-107">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the distribution list.</span></span> 
    
3. <span data-ttu-id="1d014-108">Appelez la méthode **IABContainer::GetContentsTable** de la liste de distribution pour accéder à sa table des matières.</span><span class="sxs-lookup"><span data-stu-id="1d014-108">Call the distribution list's **IABContainer::GetContentsTable** method to access its contents table.</span></span> 
    
4. <span data-ttu-id="1d014-109">Appelez [HrQueryAllRows](hrqueryallrows.md) pour récupérer toutes les lignes de la table qui représente les membres de la liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="1d014-109">Call [HrQueryAllRows](hrqueryallrows.md) to retrieve all of the table's rows representing the members of the distribution list.</span></span> 
    

