---
title: Accès aux membres d’une liste de distribution
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f724cac8-2d5d-42bc-a15e-99f77a99ce21
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2944a53d27bc916ccafcfa649d79e3c00afaf622
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412386"
---
# <a name="accessing-the-members-of-a-distribution-list"></a><span data-ttu-id="107fe-103">Accès aux membres d’une liste de distribution</span><span class="sxs-lookup"><span data-stu-id="107fe-103">Accessing the Members of a Distribution List</span></span>

  
  
<span data-ttu-id="107fe-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="107fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="107fe-105">**Pour obtenir les membres d’une liste de distribution**</span><span class="sxs-lookup"><span data-stu-id="107fe-105">**To get the members of a distribution list**</span></span>
  
1. <span data-ttu-id="107fe-106">Créez un tableau de balises de propriétés de taille moyenne avec les propriétés des membres que vous souhaitez récupérer, tels que **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) et **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="107fe-106">Create a sized property tag array with the properties of the members you would like to retrieve, such as **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), and **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="107fe-107">Appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md) pour ouvrir la liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="107fe-107">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the distribution list.</span></span> 
    
3. <span data-ttu-id="107fe-108">Appelez la méthode **IABContainer::GetContentsTable** de la liste de distribution pour accéder à sa table des matières.</span><span class="sxs-lookup"><span data-stu-id="107fe-108">Call the distribution list's **IABContainer::GetContentsTable** method to access its contents table.</span></span> 
    
4. <span data-ttu-id="107fe-109">Appelez [HrQueryAllRows](hrqueryallrows.md) pour récupérer toutes les lignes du tableau représentant les membres de la liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="107fe-109">Call [HrQueryAllRows](hrqueryallrows.md) to retrieve all of the table's rows representing the members of the distribution list.</span></span> 
    

