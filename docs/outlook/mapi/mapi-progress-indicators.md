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
# <a name="mapi-progress-indicators"></a><span data-ttu-id="b354b-103">Indicateurs de progression MAPI</span><span class="sxs-lookup"><span data-stu-id="b354b-103">MAPI Progress Indicators</span></span>

  
  
<span data-ttu-id="b354b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b354b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b354b-105">La plupart des opérations que vous effectuez pour les clients peuvent prendre beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="b354b-105">Many of the operations that you perform for clients can take a long time to complete.</span></span> <span data-ttu-id="b354b-106">Pour informer les clients de la progression d'une opération longue, vous pouvez afficher un indicateur qui affiche sous forme graphique la partie terminée d'une opération à un moment donné, du début de l'opération à son achèvement.</span><span class="sxs-lookup"><span data-stu-id="b354b-106">To inform clients of the progress of a lengthy operation, you can show an indicator that displays graphically the finished portion of an operation at any given point from the start of the operation to its completion.</span></span> <span data-ttu-id="b354b-107">L'indicateur de progression indique un pourcentage de l'opération totale à effectuer.</span><span class="sxs-lookup"><span data-stu-id="b354b-107">The progress indicator shows a percentage of the total operation to be completed.</span></span>
  
<span data-ttu-id="b354b-108">Les méthodes suivantes prennent en charge les opérations longues et l'affichage d'un indicateur de progression:</span><span class="sxs-lookup"><span data-stu-id="b354b-108">The following methods support lengthy operations and the display of a progress indicator:</span></span>
  
- <span data-ttu-id="b354b-109">[IMAPIFolder:: CopyMessages](imapifolder-copymessages.md), [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::D Eletemessages](imapifolder-deletemessages.md), [IMAPIFolder::D Eletefolder](imapifolder-deletefolder.md), [IMAPIFolder:: EmptyFolder](imapifolder-emptyfolder.md)et [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md).</span><span class="sxs-lookup"><span data-stu-id="b354b-109">[IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md), and [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span></span>
    
- <span data-ttu-id="b354b-110">[IMAPIProp:: CopyProps](imapiprop-copyprops.md) et [IMAPIProp:: CopyTo](imapiprop-copyto.md).</span><span class="sxs-lookup"><span data-stu-id="b354b-110">[IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md).</span></span>
    
- <span data-ttu-id="b354b-111">[IMAPISupport::D ocopyprops](imapisupport-docopyprops.md), [IMAPISupport::D ocopyto](imapisupport-docopyto.md), [IMAPISupport:: CopyFolder](imapisupport-copyfolder.md)et [IMAPISupport:: CopyMessages](imapisupport-copymessages.md).</span><span class="sxs-lookup"><span data-stu-id="b354b-111">[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md), [IMAPISupport::DoCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md), and [IMAPISupport::CopyMessages](imapisupport-copymessages.md).</span></span>
    
- <span data-ttu-id="b354b-112">[IMessage::D eleteattach](imessage-deleteattach.md).</span><span class="sxs-lookup"><span data-stu-id="b354b-112">[IMessage::DeleteAttach](imessage-deleteattach.md).</span></span>
    
- <span data-ttu-id="b354b-113">[IABContainer:: CopyEntries](iabcontainer-copyentries.md).</span><span class="sxs-lookup"><span data-stu-id="b354b-113">[IABContainer::CopyEntries](iabcontainer-copyentries.md).</span></span>
    
<span data-ttu-id="b354b-114">Pour afficher un indicateur de progression, MAPI définit un objet de progression.</span><span class="sxs-lookup"><span data-stu-id="b354b-114">To display a progress indicator, MAPI defines a progress object.</span></span> <span data-ttu-id="b354b-115">Les objets Progress implémentent l'interface [méthode imapiprogress: IUnknown](imapiprogressiunknown.md) , une interface qui inclut des méthodes pour établir la plage de l'indicateur et créer l'affichage.</span><span class="sxs-lookup"><span data-stu-id="b354b-115">Progress objects implement the [IMAPIProgress : IUnknown](imapiprogressiunknown.md) interface, an interface that includes methods for establishing the range of the indicator and creating the display.</span></span> <span data-ttu-id="b354b-116">MAPI fournit une implémentation d'objet de progression sous forme de clients.</span><span class="sxs-lookup"><span data-stu-id="b354b-116">MAPI provides a progress object implementation as do some clients.</span></span> <span data-ttu-id="b354b-117">Vous devez utiliser l'implémentation d'un client, si elle est fournie, en tant que paramètre d'entrée de la méthode qui exécute l'opération.</span><span class="sxs-lookup"><span data-stu-id="b354b-117">You should use a client's implementation, if one is supplied, as an input parameter to the method performing the operation.</span></span> <span data-ttu-id="b354b-118">Si le client transmet NULL au lieu d'un pointeur vers un objet de progression, utilisez l'implémentation MAPI en appelant la méthode [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="b354b-118">If the client passes NULL instead of a pointer to a progress object, use MAPI's implementation by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b354b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b354b-119">See also</span></span>



[<span data-ttu-id="b354b-120">Fournisseurs de services MAPI</span><span class="sxs-lookup"><span data-stu-id="b354b-120">MAPI Service Providers</span></span>](mapi-service-providers.md)

