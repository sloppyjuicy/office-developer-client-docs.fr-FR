---
title: Indicateurs de progression MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 73a99e52-97fe-40f5-af90-52cfd858ab22
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: d8af2ba3067dabe759056313eb278b9901510980
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784666"
---
# <a name="mapi-progress-indicators"></a><span data-ttu-id="3b198-103">Indicateurs de progression MAPI</span><span class="sxs-lookup"><span data-stu-id="3b198-103">MAPI Progress Indicators</span></span>

  
  
<span data-ttu-id="3b198-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3b198-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3b198-105">De nombreuses opérations que vous effectuez pour les clients peuvent prendre beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="3b198-105">Many of the operations that you perform for clients can take a long time to complete.</span></span> <span data-ttu-id="3b198-106">Pour informer les clients de la progression d’une longue opération, vous pouvez afficher un indicateur qui affiche sous forme graphique la partie d’une opération terminée à un moment donné à partir du début de l’opération à la fin.</span><span class="sxs-lookup"><span data-stu-id="3b198-106">To inform clients of the progress of a lengthy operation, you can show an indicator that displays graphically the finished portion of an operation at any given point from the start of the operation to its completion.</span></span> <span data-ttu-id="3b198-107">L’indicateur de progression indique un pourcentage du total l’opération se termine.</span><span class="sxs-lookup"><span data-stu-id="3b198-107">The progress indicator shows a percentage of the total operation to be completed.</span></span>
  
<span data-ttu-id="3b198-108">Les méthodes suivantes prennent en charge les opérations de longue durée et l’affichage d’un indicateur de progression :</span><span class="sxs-lookup"><span data-stu-id="3b198-108">The following methods support lengthy operations and the display of a progress indicator:</span></span>
  
- <span data-ttu-id="3b198-109">[IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md)et [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span><span class="sxs-lookup"><span data-stu-id="3b198-109">[IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md), and [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span></span>
    
- <span data-ttu-id="3b198-110">[IMAPIProp::CopyProps](imapiprop-copyprops.md) et [IMAPIProp::CopyTo](imapiprop-copyto.md).</span><span class="sxs-lookup"><span data-stu-id="3b198-110">[IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md).</span></span>
    
- <span data-ttu-id="3b198-111">[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md), [IMAPISupport::DoCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md)et [IMAPISupport::CopyMessages](imapisupport-copymessages.md).</span><span class="sxs-lookup"><span data-stu-id="3b198-111">[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md), [IMAPISupport::DoCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md), and [IMAPISupport::CopyMessages](imapisupport-copymessages.md).</span></span>
    
- <span data-ttu-id="3b198-112">[IMessage::DeleteAttach](imessage-deleteattach.md).</span><span class="sxs-lookup"><span data-stu-id="3b198-112">[IMessage::DeleteAttach](imessage-deleteattach.md).</span></span>
    
- <span data-ttu-id="3b198-113">[IABContainer::CopyEntries](iabcontainer-copyentries.md).</span><span class="sxs-lookup"><span data-stu-id="3b198-113">[IABContainer::CopyEntries](iabcontainer-copyentries.md).</span></span>
    
<span data-ttu-id="3b198-114">Pour afficher un indicateur de progression, MAPI définit un objet de progression.</span><span class="sxs-lookup"><span data-stu-id="3b198-114">To display a progress indicator, MAPI defines a progress object.</span></span> <span data-ttu-id="3b198-115">Implémentent des objets de l’avancement du [IMAPIProgress : IUnknown](imapiprogressiunknown.md) interface, une interface qui inclut des méthodes pour l’établissement de la plage de l’indicateur et de création de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="3b198-115">Progress objects implement the [IMAPIProgress : IUnknown](imapiprogressiunknown.md) interface, an interface that includes methods for establishing the range of the indicator and creating the display.</span></span> <span data-ttu-id="3b198-116">MAPI fournit une implémentation d’objet de progression comme certains clients.</span><span class="sxs-lookup"><span data-stu-id="3b198-116">MAPI provides a progress object implementation as do some clients.</span></span> <span data-ttu-id="3b198-117">Vous devez utiliser la mise en œuvre d’un client, le cas échéant, comme paramètre d’entrée à la méthode effectue l’opération.</span><span class="sxs-lookup"><span data-stu-id="3b198-117">You should use a client's implementation, if one is supplied, as an input parameter to the method performing the operation.</span></span> <span data-ttu-id="3b198-118">Si le client transmet NULL au lieu d’un pointeur vers un objet de progression, utilisez la mise en œuvre de MAPI en appelant la méthode [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="3b198-118">If the client passes NULL instead of a pointer to a progress object, use MAPI's implementation by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3b198-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b198-119">See also</span></span>



[<span data-ttu-id="3b198-120">Fournisseurs de services MAPI</span><span class="sxs-lookup"><span data-stu-id="3b198-120">MAPI Service Providers</span></span>](mapi-service-providers.md)

