---
title: L’ouverture d’un descripteur d’affichage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1940feb0-9e0f-4d96-9fb9-b9a35a0aa661
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 680d80c0827399f3b7a0ea5819e51be654a05810
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592478"
---
# <a name="opening-a-view-descriptor"></a><span data-ttu-id="704cf-103">L’ouverture d’un descripteur d’affichage</span><span class="sxs-lookup"><span data-stu-id="704cf-103">Opening a view descriptor</span></span>
  
<span data-ttu-id="704cf-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="704cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="704cf-105">Nombre de dossiers peut être ouvert avec n’importe quel nombre de vues personnalisées, une vue par défaut ou un affichage normal.</span><span class="sxs-lookup"><span data-stu-id="704cf-105">Many folders can be opened with a normal view, a default view, or any number of personalized views.</span></span> <span data-ttu-id="704cf-106">Un affichage explique comment afficher le contenu d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="704cf-106">A view describes how to display the contents of a folder.</span></span> <span data-ttu-id="704cf-107">L’affichage normal est utilisé lorsqu’il n’existe aucune autre vue et lorsque vous ouvrez le dossier pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="704cf-107">The normal view is used when there is no alternative view and when you are opening the folder for the first time.</span></span> <span data-ttu-id="704cf-108">Lorsqu’une autre vue n’existe pas, vous devez l’utiliser pour ouvrir le dossier.</span><span class="sxs-lookup"><span data-stu-id="704cf-108">When an alternative view does exist, you must use it to open the folder.</span></span>
  
<span data-ttu-id="704cf-109">Une vue est décrit dans un message appelé descripteur d’un affichage.</span><span class="sxs-lookup"><span data-stu-id="704cf-109">A view is described in a message known as a view descriptor.</span></span> <span data-ttu-id="704cf-110">Affichage descripteurs sont généralement créés en tant que messages associés et susceptibles d’apparaître dans soit les dossiers d’affichage communs ou personnel ou dans n’importe quel dossier IPM.</span><span class="sxs-lookup"><span data-stu-id="704cf-110">View descriptors are typically created as associated messages and can appear in either the common or personal view folders or in any IPM folder.</span></span>
  
### <a name="to-open-a-view-descriptor"></a><span data-ttu-id="704cf-111">Pour ouvrir un descripteur d’affichage</span><span class="sxs-lookup"><span data-stu-id="704cf-111">To open a view descriptor</span></span>
  
1. <span data-ttu-id="704cf-112">Appelez [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) pour récupérer la table des matières associée pour le dossier.</span><span class="sxs-lookup"><span data-stu-id="704cf-112">Call [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) to retrieve the associated contents table for the folder.</span></span> 
    
2. <span data-ttu-id="704cf-113">Créer une restriction qui localise uniquement les messages avec la classe de message réservée pour les descripteurs de vue et appelez [IMAPITable](imapitable-restrict.md) pour limiter la table et [IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer les lignes appropriées, ou...</span><span class="sxs-lookup"><span data-stu-id="704cf-113">Create a restriction that locates only messages with the message class reserved for view descriptors and call [IMAPITable::Restrict](imapitable-restrict.md) to limit the table and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the appropriate rows, or...</span></span>
    
   <span data-ttu-id="704cf-114">Appeler [IMAPIProp::GetProps](imapiprop-getprops.md) méthode du dossier pour récupérer la propriété **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="704cf-114">Call the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="704cf-115">**PR_DEFAULT_VIEW_ENTRYID** contient l’identificateur d’entrée du message contenant le descripteur d’affichage par défaut pour un dossier.</span><span class="sxs-lookup"><span data-stu-id="704cf-115">**PR_DEFAULT_VIEW_ENTRYID** contains the entry identifier for the message containing the default view descriptor for a folder.</span></span> <span data-ttu-id="704cf-116">Cet appel va réussir si le dossier prend en charge l’utilisation de l’indicateur MAPI_ASSOCIATED sur les appels à [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) et [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).</span><span class="sxs-lookup"><span data-stu-id="704cf-116">This call will succeed if the folder supports the use of the MAPI_ASSOCIATED flag on calls to [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) and [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).</span></span>
    
3. <span data-ttu-id="704cf-117">Appelez [IMsgStore::OpenEntry](imsgstore-openentry.md) avec l’identificateur d’entrée du descripteur d’affichage pour l’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="704cf-117">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with the entry identifier of the view descriptor to open it.</span></span> 
    

