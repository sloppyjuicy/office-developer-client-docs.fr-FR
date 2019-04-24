---
title: Affichage de la table des matières d’un dossier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 14a4c123-776d-4a32-9688-8a4402dd1f53
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 56847283afaf41c1d45cdb875ddf49eaa5881175
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339934"
---
# <a name="displaying-a-folder-contents-table"></a><span data-ttu-id="25544-103">Affichage de la table des matières d’un dossier</span><span class="sxs-lookup"><span data-stu-id="25544-103">Displaying a folder contents table</span></span>

<span data-ttu-id="25544-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25544-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25544-105">La table de contenu d'un dossier contient des informations récapitulatives sur tous ses messages.</span><span class="sxs-lookup"><span data-stu-id="25544-105">The contents table of a folder contains summary information about all of its messages.</span></span> <span data-ttu-id="25544-106">Des informations récapitulatives sur les nouveaux messages entrants s'affichent dans la table des matières du dossier de réception de la classe de message.</span><span class="sxs-lookup"><span data-stu-id="25544-106">Summary information about new incoming messages appears in the contents table of the receive folder for the message class.</span></span> <span data-ttu-id="25544-107">Pour mettre ces informations à la disposition des utilisateurs, récupérez la table et affichez les colonnes et les lignes, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="25544-107">To make this information available to users, retrieve the table and display the columns and rows as appropriate.</span></span>
  
<span data-ttu-id="25544-108">**Pour afficher un tableau de contenu de dossier**</span><span class="sxs-lookup"><span data-stu-id="25544-108">**To display a folder contents table**</span></span>
  
1. <span data-ttu-id="25544-109">Appelez [IMsgStore:: OpenEntry](imsgstore-openentry.md), en transmettant l'identificateur d'entrée du dossier contenant la table.</span><span class="sxs-lookup"><span data-stu-id="25544-109">Call [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the entry identifier of the folder containing the table.</span></span>
    
2. <span data-ttu-id="25544-110">Appelez la méthode [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md) du dossier pour ouvrir sa table des matières.</span><span class="sxs-lookup"><span data-stu-id="25544-110">Call the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to open its contents table.</span></span> 
    
3. <span data-ttu-id="25544-111">Limitez l'affichage de la table de contenu si vous le souhaitez en appelant la méthode [IMAPITable:: SetColumns](imapitable-setcolumns.md) de la table pour spécifier des colonnes particulières.</span><span class="sxs-lookup"><span data-stu-id="25544-111">Limit your view of the contents table if desired by calling the table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to specify particular columns.</span></span> 
    
4. <span data-ttu-id="25544-112">Limitez l'affichage de la table de contenu si vous le souhaitez en appelant la méthode [IMAPITable:: Restrict](imapitable-restrict.md) pour filtrer des lignes spécifiques.</span><span class="sxs-lookup"><span data-stu-id="25544-112">Limit your view of the contents table if desired by calling the table's [IMAPITable::Restrict](imapitable-restrict.md) method to filter particular rows.</span></span> <span data-ttu-id="25544-113">Par exemple, si vous souhaitez n'afficher que les messages avec une classe de message spécifique qui n'ont pas encore été lues:</span><span class="sxs-lookup"><span data-stu-id="25544-113">If, for example, you want to show only messages with a specific message class that have yet to be read:</span></span> 
    
    1. <span data-ttu-id="25544-114">Créez une restriction de propriété dans une structure [SPropertyRestriction](spropertyrestriction.md) qui correspond à la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) avec la classe de message souhaitée.</span><span class="sxs-lookup"><span data-stu-id="25544-114">Create a property restriction in an [SPropertyRestriction](spropertyrestriction.md) structure that matches the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property with the desired message class.</span></span> 
        
    2. <span data-ttu-id="25544-115">Créez une restriction de masque de masques dans une structure [SBitMaskRestriction](sbitmaskrestriction.md) qui utilise **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) comme balise de propriété et la valeur MSGFLAG_UNREAD comme masque.</span><span class="sxs-lookup"><span data-stu-id="25544-115">Create a bitmask restriction in an [SBitMaskRestriction](sbitmaskrestriction.md) structure that uses **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) as the property tag and the MSGFLAG_UNREAD value as the mask.</span></span>
        
    3. <span data-ttu-id="25544-116">Créer une restriction dans une structure [SAndRestriction](sandrestriction.md) qui joint les restrictions de propriété et de masque de masque.</span><span class="sxs-lookup"><span data-stu-id="25544-116">Create a restriction in an [SAndRestriction](sandrestriction.md) structure that joins the property and bitmask restrictions.</span></span> 
    
5. <span data-ttu-id="25544-117">Triez le tableau de contenu si vous le souhaitez en appelant la méthode [IMAPITable:: SortTable](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="25544-117">Sort the contents table if desired by calling the table's [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
    
6. <span data-ttu-id="25544-118">Appelez [IMAPITable:: QueryRows](imapitable-queryrows.md) pour récupérer toutes les lignes de la table de contenu pour traitement.</span><span class="sxs-lookup"><span data-stu-id="25544-118">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows from the contents table for processing.</span></span> 
    

