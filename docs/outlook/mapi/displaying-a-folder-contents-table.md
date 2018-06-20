---
title: Affichage d’une table de contenu de dossier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 14a4c123-776d-4a32-9688-8a4402dd1f53
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 30099e9fe645f810e08ba331717cff975f69b313
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783190"
---
# <a name="displaying-a-folder-contents-table"></a><span data-ttu-id="d0b56-103">Affichage d’une table de contenu de dossier</span><span class="sxs-lookup"><span data-stu-id="d0b56-103">Displaying a folder contents table</span></span>

<span data-ttu-id="d0b56-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d0b56-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d0b56-105">La table des matières d’un dossier contient des informations récapitulatives sur tous ses messages.</span><span class="sxs-lookup"><span data-stu-id="d0b56-105">The contents table of a folder contains summary information about all of its messages.</span></span> <span data-ttu-id="d0b56-106">Informations récapitulatives concernant les nouveaux messages entrants s’affiche dans le tableau contenu du dossier de réception pour la classe de message.</span><span class="sxs-lookup"><span data-stu-id="d0b56-106">Summary information about new incoming messages appears in the contents table of the receive folder for the message class.</span></span> <span data-ttu-id="d0b56-107">Pour rendre ces informations disponibles aux utilisateurs, extraire la table et afficher les colonnes et lignes comme il convient.</span><span class="sxs-lookup"><span data-stu-id="d0b56-107">To make this information available to users, retrieve the table and display the columns and rows as appropriate.</span></span>
  
<span data-ttu-id="d0b56-108">**Pour afficher un tableau contenu de dossier**</span><span class="sxs-lookup"><span data-stu-id="d0b56-108">**To display a folder contents table**</span></span>
  
1. <span data-ttu-id="d0b56-109">Appelez [IMsgStore::OpenEntry](imsgstore-openentry.md), en passant l’identificateur d’entrée du dossier contenant la table.</span><span class="sxs-lookup"><span data-stu-id="d0b56-109">Call [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the entry identifier of the folder containing the table.</span></span>
    
2. <span data-ttu-id="d0b56-110">Appelez du dossier [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) pour ouvrir la table des matières.</span><span class="sxs-lookup"><span data-stu-id="d0b56-110">Call the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to open its contents table.</span></span> 
    
3. <span data-ttu-id="d0b56-111">Limiter l’affichage de la table des matières si vous le souhaitez en appelant la méthode [IMAPITable::SetColumns](imapitable-setcolumns.md) de la table pour spécifier les colonnes particuliers.</span><span class="sxs-lookup"><span data-stu-id="d0b56-111">Limit your view of the contents table if desired by calling the table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to specify particular columns.</span></span> 
    
4. <span data-ttu-id="d0b56-112">Limiter l’affichage de la table des matières si vous le souhaitez en appelant la méthode la table [IMAPITable](imapitable-restrict.md) pour filtrer les lignes particuliers.</span><span class="sxs-lookup"><span data-stu-id="d0b56-112">Limit your view of the contents table if desired by calling the table's [IMAPITable::Restrict](imapitable-restrict.md) method to filter particular rows.</span></span> <span data-ttu-id="d0b56-113">Si, par exemple, vous souhaitez afficher uniquement les messages avec une classe de message spécifique qui n’ont pas encore être lues :</span><span class="sxs-lookup"><span data-stu-id="d0b56-113">If, for example, you want to show only messages with a specific message class that have yet to be read:</span></span> 
    
    1. <span data-ttu-id="d0b56-114">Créez une restriction de propriété dans une structure [SPropertyRestriction](spropertyrestriction.md) qui correspond à la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) avec la classe de message de votre choix.</span><span class="sxs-lookup"><span data-stu-id="d0b56-114">Create a property restriction in an [SPropertyRestriction](spropertyrestriction.md) structure that matches the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property with the desired message class.</span></span> 
        
    2. <span data-ttu-id="d0b56-115">Créez une restriction de masque de bits dans une structure [SBitMaskRestriction](sbitmaskrestriction.md) qui utilise **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) en tant que la balise de propriété et la valeur MSGFLAG_UNREAD comme masque.</span><span class="sxs-lookup"><span data-stu-id="d0b56-115">Create a bitmask restriction in an [SBitMaskRestriction](sbitmaskrestriction.md) structure that uses **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) as the property tag and the MSGFLAG_UNREAD value as the mask.</span></span>
        
    3. <span data-ttu-id="d0b56-116">Créez une restriction dans une structure [SAndRestriction](sandrestriction.md) qui associe les restrictions de propriété et masque de bits.</span><span class="sxs-lookup"><span data-stu-id="d0b56-116">Create a restriction in an [SAndRestriction](sandrestriction.md) structure that joins the property and bitmask restrictions.</span></span> 
    
5. <span data-ttu-id="d0b56-117">Trier le tableau contenu si vous le souhaitez en appelant la méthode [IMAPITable::SortTable](imapitable-sorttable.md) de la table.</span><span class="sxs-lookup"><span data-stu-id="d0b56-117">Sort the contents table if desired by calling the table's [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
    
6. <span data-ttu-id="d0b56-118">[IMAPITable::QueryRows](imapitable-queryrows.md) pour extraire toutes les lignes de la table de contenu pour le traitement des appels.</span><span class="sxs-lookup"><span data-stu-id="d0b56-118">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows from the contents table for processing.</span></span> 
    

