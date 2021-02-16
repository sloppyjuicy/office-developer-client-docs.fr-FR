---
title: Affichage des icônes de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c93912d19f0ad3c3231092c82f27cec9e3f15b3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438630"
---
# <a name="displaying-form-icons"></a><span data-ttu-id="ef06f-103">Affichage des icônes de formulaire</span><span class="sxs-lookup"><span data-stu-id="ef06f-103">Displaying Form Icons</span></span>

  
  
<span data-ttu-id="ef06f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef06f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef06f-105">Lors de l’affichage d’une liste de messages dans un dossier, il est utile pour vos utilisateurs si vous distinguez les messages avec des classes de messages personnalisées de l’IPM standard. Messages de note.</span><span class="sxs-lookup"><span data-stu-id="ef06f-105">When displaying a list of messages in a folder, it is helpful to your users if you distinguish messages with custom message classes from the standard IPM.Note messages.</span></span> <span data-ttu-id="ef06f-106">Les classes de message personnalisées correspondent aux serveurs de formulaires et les serveurs de formulaire fournissent des icônes pour se représenter eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="ef06f-106">Custom message classes correspond to form servers, and form servers provide icons to represent themselves.</span></span> <span data-ttu-id="ef06f-107">Vous pouvez afficher ces icônes dans la liste des messages pour alerter les utilisateurs de la classe de message de chaque message avant que l’utilisateur n’ouvre les messages.</span><span class="sxs-lookup"><span data-stu-id="ef06f-107">You can display these icons in the list of messages to alert users to each message's message class before the user opens the messages.</span></span> <span data-ttu-id="ef06f-108">En règle générale, l’icône de la propriété **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) du formulaire est celle qui doit être affichée dans la liste des messages.</span><span class="sxs-lookup"><span data-stu-id="ef06f-108">Typically, the icon in the form's **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property is the one that should be displayed in the list of messages.</span></span> <span data-ttu-id="ef06f-109">Les formulaires ont **également une PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) qui peut être affichée lorsque le formulaire est réduit dans une feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="ef06f-109">Forms also have a **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) property that can be displayed when the form is minimized in a property sheet.</span></span>
  
 <span data-ttu-id="ef06f-110">**Pour obtenir une icône pour une classe de message sans activer le serveur de formulaires pour cette classe de message**</span><span class="sxs-lookup"><span data-stu-id="ef06f-110">**To get an icon for a message class without activating the form server for that message class**</span></span>
  
1. <span data-ttu-id="ef06f-111">Appelez [la méthode IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) pour obtenir un pointeur vers une interface [IMAPIFormContainer : IUnknown.](imapiformcontaineriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="ef06f-111">Call the [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method to get a pointer to an [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
2. <span data-ttu-id="ef06f-112">Appelez [la méthode IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) pour obtenir un pointeur vers une interface [IMAPIFormInfo : IMAPIProp.](imapiforminfoimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="ef06f-112">Call the [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) method to get a pointer to an [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
3. <span data-ttu-id="ef06f-113">Appelez [la méthode IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) pour obtenir un handle d’icône.</span><span class="sxs-lookup"><span data-stu-id="ef06f-113">Call the [IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) method to get an icon handle.</span></span> 
    
<span data-ttu-id="ef06f-114">L’icône peut ensuite être affichée à l’aide des API Win32 standard.</span><span class="sxs-lookup"><span data-stu-id="ef06f-114">The icon can then be displayed using standard Win32 APIs.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="ef06f-115">Une fois que vous avez l’icône d’une classe de message, veillez à mettre en cache cette icône.</span><span class="sxs-lookup"><span data-stu-id="ef06f-115">Once you have the icon for a message class, make every effort to cache that icon.</span></span> <span data-ttu-id="ef06f-116">Le fait de ne pas mettre en cache les icônes affecte gravement les performances des applications clientes.</span><span class="sxs-lookup"><span data-stu-id="ef06f-116">Not caching icons severely affects the performance of client applications.</span></span> <span data-ttu-id="ef06f-117">Lors de la mise en cache des icônes, faites attention aux relations entre les classes de message et leurs sous-classes.</span><span class="sxs-lookup"><span data-stu-id="ef06f-117">When caching icons, be careful of the relationships between message classes and their subclasses.</span></span> <span data-ttu-id="ef06f-118">Par exemple, si le IPM. Note.Meeting.Cancel message class happens to resolve back to IPM. Notez que ne supposez pas que toutes les sous-classes d’IPM. Notez que vous devez utiliser l’icône pour IPM. Remarque.</span><span class="sxs-lookup"><span data-stu-id="ef06f-118">For example, if the IPM.Note.Meeting.Cancel message class happens to resolve back to IPM.Note, do not assume that all subclasses of IPM.Note should use the icon for IPM.Note.</span></span> 
  

