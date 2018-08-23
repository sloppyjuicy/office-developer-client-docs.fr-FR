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
ms.openlocfilehash: a32552343fa90dfbbb3571f50846976a5f5f5edd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595362"
---
# <a name="accessing-the-members-of-a-distribution-list"></a><span data-ttu-id="4d2b4-103">Accès aux membres d’une liste de distribution</span><span class="sxs-lookup"><span data-stu-id="4d2b4-103">Accessing the Members of a Distribution List</span></span>

  
  
<span data-ttu-id="4d2b4-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d2b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="4d2b4-105">**Pour obtenir les membres d’une liste de distribution**</span><span class="sxs-lookup"><span data-stu-id="4d2b4-105">**To get the members of a distribution list**</span></span>
  
1. <span data-ttu-id="4d2b4-106">Créer un tableau de balise de propriété ajustés avec les propriétés des membres que vous souhaitez récupérer, comme **PR_DISPLAY_TYPE** ([ , **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) et **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4d2b4-106">Create a sized property tag array with the properties of the members you would like to retrieve, such as **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), and **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="4d2b4-107">Appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md) pour ouvrir la liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="4d2b4-107">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the distribution list.</span></span> 
    
3. <span data-ttu-id="4d2b4-108">Appelez la méthode **IABContainer::GetContentsTable** de la liste de distribution pour accéder à sa table des matières.</span><span class="sxs-lookup"><span data-stu-id="4d2b4-108">Call the distribution list's **IABContainer::GetContentsTable** method to access its contents table.</span></span> 
    
4. <span data-ttu-id="4d2b4-109">Appelez [HrQueryAllRows](hrqueryallrows.md) pour récupérer toutes les lignes de la table qui représente les membres de la liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="4d2b4-109">Call [HrQueryAllRows](hrqueryallrows.md) to retrieve all of the table's rows representing the members of the distribution list.</span></span> 
    

