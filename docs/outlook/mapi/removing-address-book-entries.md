---
title: Suppression d’entrées du carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 107ebcd7-b612-4139-b676-c3851f15bc74
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1d5ae33b08c85c9ee93764d762c2ec251fddd265
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328349"
---
# <a name="removing-address-book-entries"></a><span data-ttu-id="b609a-103">Suppression d’entrées du carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="b609a-103">Removing address book entries</span></span>
  
<span data-ttu-id="b609a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b609a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b609a-105">IABContainer de votre conteneur: la méthode [eleteentries:D](iabcontainer-deleteentries.md) est appelée pour supprimer un ou plusieurs destinataires.</span><span class="sxs-lookup"><span data-stu-id="b609a-105">Your container's [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method is called to remove one or more recipients.</span></span> <span data-ttu-id="b609a-106">**DeleteEntries** comporte deux paramètres: un tableau d'identificateurs d'entrée représentant les destinataires à supprimer et une valeur d'indicateurs réservée.</span><span class="sxs-lookup"><span data-stu-id="b609a-106">**DeleteEntries** has two parameters: an array of entry identifiers representing the recipients to be deleted and a reserved flags value.</span></span> <span data-ttu-id="b609a-107">La suppression d'un destinataire affecte la table des matières de votre conteneur; en plus de supprimer le destinataire, votre conteneur doit supprimer la ligne de la table de contenu qui représente le destinataire.</span><span class="sxs-lookup"><span data-stu-id="b609a-107">Deleting a recipient affects the contents table of your container; in addition to deleting the recipient, your container must delete the contents table row that represents the recipient.</span></span> <span data-ttu-id="b609a-108">Lorsque la ligne a été supprimée de la table, votre conteneur doit émettre une notification de table pour chaque client inscrit.</span><span class="sxs-lookup"><span data-stu-id="b609a-108">When the row has been removed from the table, your container must issue a table notification to each registered client.</span></span> 
  
### <a name="to-implement-iabcontainerdeleteentries"></a><span data-ttu-id="b609a-109">Pour implémenter IABContainer, procédez comme suit::D eleteEntries</span><span class="sxs-lookup"><span data-stu-id="b609a-109">To implement IABContainer::DeleteEntries</span></span>
  
1. <span data-ttu-id="b609a-110">Supprimez tous les destinataires représentés par l'identificateur d'entrée de votre conteneur.</span><span class="sxs-lookup"><span data-stu-id="b609a-110">Delete each recipient represented by the entry identifier from your container.</span></span>
    
2. <span data-ttu-id="b609a-111">Si la table des matières de votre conteneur est ouverte:</span><span class="sxs-lookup"><span data-stu-id="b609a-111">If your container's contents table is open:</span></span>
    
   - <span data-ttu-id="b609a-112">Envoyez une notification _fnevTableModified_ avec le membre **ULTABLEEVENT** défini sur TABLE_ROW_DELETED aux clients inscrits pour chaque ligne de tableau de contenu supprimé.</span><span class="sxs-lookup"><span data-stu-id="b609a-112">Send an  _fnevTableModified_ notification with the **ulTableEvent** member set to TABLE_ROW_DELETED to registered clients for each deleted contents table row.</span></span> <span data-ttu-id="b609a-113">Si votre fournisseur utilise l'utilitaire de notification, appelez [IMAPISupport:: Notify](imapisupport-notify.md) pour envoyer ces notifications.</span><span class="sxs-lookup"><span data-stu-id="b609a-113">If your provider uses the notification utility, call [IMAPISupport::Notify](imapisupport-notify.md) to send these notifications.</span></span> 
    
   - <span data-ttu-id="b609a-114">Si votre fournisseur prend en charge les notifications d'objet, envoyez également une notification _fnevObjectDeleted_ .</span><span class="sxs-lookup"><span data-stu-id="b609a-114">If your provider supports object notifications, also send an  _fnevObjectDeleted_ notification.</span></span> 
    

