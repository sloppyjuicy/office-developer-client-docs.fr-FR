---
title: Suppression des entrées de carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 107ebcd7-b612-4139-b676-c3851f15bc74
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 1fb7224e110bbee6844cf2820782aac8be213ba3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786979"
---
# <a name="removing-address-book-entries"></a><span data-ttu-id="b5676-103">Suppression des entrées de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="b5676-103">Removing address book entries</span></span>
  
<span data-ttu-id="b5676-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b5676-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b5676-105">Méthode de [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) de votre conteneur est appelée pour supprimer un ou plusieurs destinataires.</span><span class="sxs-lookup"><span data-stu-id="b5676-105">Your container's [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method is called to remove one or more recipients.</span></span> <span data-ttu-id="b5676-106">**DeleteEntries** possède deux paramètres : un tableau d’identificateurs d’entrée représentant les destinataires à supprimer et une valeur pour les indicateurs réservés.</span><span class="sxs-lookup"><span data-stu-id="b5676-106">**DeleteEntries** has two parameters: an array of entry identifiers representing the recipients to be deleted and a reserved flags value.</span></span> <span data-ttu-id="b5676-107">Suppression d’un destinataire affecte la table des matières de votre conteneur ; en plus de supprimer le destinataire, le conteneur doit supprimer la ligne du tableau contenu qui représente le destinataire.</span><span class="sxs-lookup"><span data-stu-id="b5676-107">Deleting a recipient affects the contents table of your container; in addition to deleting the recipient, your container must delete the contents table row that represents the recipient.</span></span> <span data-ttu-id="b5676-108">Lorsque la ligne a été supprimée de la table, votre conteneur doit émettre une notification de la table pour chaque client enregistré.</span><span class="sxs-lookup"><span data-stu-id="b5676-108">When the row has been removed from the table, your container must issue a table notification to each registered client.</span></span> 
  
### <a name="to-implement-iabcontainerdeleteentries"></a><span data-ttu-id="b5676-109">Pour mettre en œuvre IABContainer::DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="b5676-109">To implement IABContainer::DeleteEntries</span></span>
  
1. <span data-ttu-id="b5676-110">Supprimez chaque destinataire représentée par l’identificateur d’entrée à partir de votre conteneur.</span><span class="sxs-lookup"><span data-stu-id="b5676-110">Delete each recipient represented by the entry identifier from your container.</span></span>
    
2. <span data-ttu-id="b5676-111">Si la table des matières de votre conteneur est ouvert :</span><span class="sxs-lookup"><span data-stu-id="b5676-111">If your container's contents table is open:</span></span>
    
   - <span data-ttu-id="b5676-112">Envoyer une notification _fnevTableModified_ avec le membre **ulTableEvent** défini sur TABLE_ROW_DELETED aux clients enregistrés pour chaque ligne du tableau contenu supprimé.</span><span class="sxs-lookup"><span data-stu-id="b5676-112">Send an  _fnevTableModified_ notification with the **ulTableEvent** member set to TABLE_ROW_DELETED to registered clients for each deleted contents table row.</span></span> <span data-ttu-id="b5676-113">Si votre fournisseur utilise l’utilitaire de notification, appelez [IMAPISupport::Notify](imapisupport-notify.md) pour envoyer ces notifications.</span><span class="sxs-lookup"><span data-stu-id="b5676-113">If your provider uses the notification utility, call [IMAPISupport::Notify](imapisupport-notify.md) to send these notifications.</span></span> 
    
   - <span data-ttu-id="b5676-114">Si votre fournisseur prend en charge les notifications de l’objet, également envoyer une notification _fnevObjectDeleted_ .</span><span class="sxs-lookup"><span data-stu-id="b5676-114">If your provider supports object notifications, also send an  _fnevObjectDeleted_ notification.</span></span> 
    

