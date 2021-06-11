---
title: Indicateurs de progression MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 73a99e52-97fe-40f5-af90-52cfd858ab22
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: cdfb6898146583b7da9b043eadd3acc09edbf292
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410706"
---
# <a name="mapi-progress-indicators"></a><span data-ttu-id="653a1-103">Indicateurs de progression MAPI</span><span class="sxs-lookup"><span data-stu-id="653a1-103">MAPI Progress Indicators</span></span>

  
  
<span data-ttu-id="653a1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="653a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="653a1-105">La plupart des opérations que vous effectuez pour les clients peuvent prendre beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="653a1-105">Many of the operations that you perform for clients can take a long time to complete.</span></span> <span data-ttu-id="653a1-106">Pour informer les clients de la progression d’une opération longue, vous pouvez afficher un indicateur qui affiche graphiquement la partie terminée d’une opération à un moment donné depuis le début de l’opération jusqu’à son achèvement.</span><span class="sxs-lookup"><span data-stu-id="653a1-106">To inform clients of the progress of a lengthy operation, you can show an indicator that displays graphically the finished portion of an operation at any given point from the start of the operation to its completion.</span></span> <span data-ttu-id="653a1-107">L’indicateur de progression indique un pourcentage de l’opération totale à terminer.</span><span class="sxs-lookup"><span data-stu-id="653a1-107">The progress indicator shows a percentage of the total operation to be completed.</span></span>
  
<span data-ttu-id="653a1-108">Les méthodes suivantes supportent des opérations longues et l’affichage d’un indicateur de progression :</span><span class="sxs-lookup"><span data-stu-id="653a1-108">The following methods support lengthy operations and the display of a progress indicator:</span></span>
  
- <span data-ttu-id="653a1-109">[IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::D eleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::D eleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md)et [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span><span class="sxs-lookup"><span data-stu-id="653a1-109">[IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md), and [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span></span>
    
- <span data-ttu-id="653a1-110">[IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md).</span><span class="sxs-lookup"><span data-stu-id="653a1-110">[IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md).</span></span>
    
- <span data-ttu-id="653a1-111">[IMAPISupport::D oCopyProps](imapisupport-docopyprops.md), [IMAPISupport::D oCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md)et [IMAPISupport::CopyMessages](imapisupport-copymessages.md).</span><span class="sxs-lookup"><span data-stu-id="653a1-111">[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md), [IMAPISupport::DoCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md), and [IMAPISupport::CopyMessages](imapisupport-copymessages.md).</span></span>
    
- <span data-ttu-id="653a1-112">[IMessage::D eleteAttach](imessage-deleteattach.md).</span><span class="sxs-lookup"><span data-stu-id="653a1-112">[IMessage::DeleteAttach](imessage-deleteattach.md).</span></span>
    
- <span data-ttu-id="653a1-113">[IABContainer::CopyEntries](iabcontainer-copyentries.md).</span><span class="sxs-lookup"><span data-stu-id="653a1-113">[IABContainer::CopyEntries](iabcontainer-copyentries.md).</span></span>
    
<span data-ttu-id="653a1-114">Pour afficher un indicateur de progression, MAPI définit un objet de progression.</span><span class="sxs-lookup"><span data-stu-id="653a1-114">To display a progress indicator, MAPI defines a progress object.</span></span> <span data-ttu-id="653a1-115">Les objets de progression implémentent l’interface [IMAPIProgress : IUnknown,](imapiprogressiunknown.md) une interface qui inclut des méthodes pour établir la plage de l’indicateur et créer l’affichage.</span><span class="sxs-lookup"><span data-stu-id="653a1-115">Progress objects implement the [IMAPIProgress : IUnknown](imapiprogressiunknown.md) interface, an interface that includes methods for establishing the range of the indicator and creating the display.</span></span> <span data-ttu-id="653a1-116">MAPI fournit une implémentation d’objet de progression, tout comme certains clients.</span><span class="sxs-lookup"><span data-stu-id="653a1-116">MAPI provides a progress object implementation as do some clients.</span></span> <span data-ttu-id="653a1-117">Vous devez utiliser l’implémentation d’un client, si elle est fournie, comme paramètre d’entrée pour la méthode qui exécute l’opération.</span><span class="sxs-lookup"><span data-stu-id="653a1-117">You should use a client's implementation, if one is supplied, as an input parameter to the method performing the operation.</span></span> <span data-ttu-id="653a1-118">Si le client transmet la valeur NULL au lieu d’un pointeur vers un objet de progression, utilisez l’implémentation de MAPI en appelant la méthode [IMAPISupport::D oProgressDialog.](imapisupport-doprogressdialog.md)</span><span class="sxs-lookup"><span data-stu-id="653a1-118">If the client passes NULL instead of a pointer to a progress object, use MAPI's implementation by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="653a1-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="653a1-119">See also</span></span>



[<span data-ttu-id="653a1-120">Fournisseurs de services MAPI</span><span class="sxs-lookup"><span data-stu-id="653a1-120">MAPI Service Providers</span></span>](mapi-service-providers.md)

