---
title: Afficher les icônes de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: b2e79e5568de38bee9a97c9df2598b30f1ba1bdf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783186"
---
# <a name="displaying-form-icons"></a><span data-ttu-id="1fbab-103">Afficher les icônes de formulaire</span><span class="sxs-lookup"><span data-stu-id="1fbab-103">Displaying Form Icons</span></span>

  
  
<span data-ttu-id="1fbab-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1fbab-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1fbab-105">Lorsque vous affichez une liste des messages dans un dossier, il est utile pour les utilisateurs si vous distinguer les messages avec les classes de message personnalisées à partir de l’IPM standard. Notez les messages.</span><span class="sxs-lookup"><span data-stu-id="1fbab-105">When displaying a list of messages in a folder, it is helpful to your users if you distinguish messages with custom message classes from the standard IPM.Note messages.</span></span> <span data-ttu-id="1fbab-106">Classes de message personnalisées correspondent aux serveurs de formulaire et les serveurs de formulaire permettent d’icônes pour représenter elle-même.</span><span class="sxs-lookup"><span data-stu-id="1fbab-106">Custom message classes correspond to form servers, and form servers provide icons to represent themselves.</span></span> <span data-ttu-id="1fbab-107">Vous pouvez afficher ces icônes dans la liste des messages pour avertir les utilisateurs de la classe de message de chaque message avant que l’utilisateur ouvre les messages.</span><span class="sxs-lookup"><span data-stu-id="1fbab-107">You can display these icons in the list of messages to alert users to each message's message class before the user opens the messages.</span></span> <span data-ttu-id="1fbab-108">En règle générale, l’icône de la propriété du formulaire **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) est celui qui doit être affiché dans la liste des messages.</span><span class="sxs-lookup"><span data-stu-id="1fbab-108">Typically, the icon in the form's **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property is the one that should be displayed in the list of messages.</span></span> <span data-ttu-id="1fbab-109">Formulaires ont également une propriété **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) qui peut être affichée lorsque le formulaire est réduit dans une feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="1fbab-109">Forms also have a **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) property that can be displayed when the form is minimized in a property sheet.</span></span>
  
 <span data-ttu-id="1fbab-110">**Pour obtenir une icône pour une classe de message sans activer le serveur de formulaire pour cette classe de message**</span><span class="sxs-lookup"><span data-stu-id="1fbab-110">**To get an icon for a message class without activating the form server for that message class**</span></span>
  
1. <span data-ttu-id="1fbab-111">Appelez la méthode [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) pour obtenir un pointeur vers une [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span><span class="sxs-lookup"><span data-stu-id="1fbab-111">Call the [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method to get a pointer to an [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
2. <span data-ttu-id="1fbab-112">Appelez la méthode [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) pour obtenir un pointeur vers une [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span><span class="sxs-lookup"><span data-stu-id="1fbab-112">Call the [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) method to get a pointer to an [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
3. <span data-ttu-id="1fbab-113">Appelez la méthode [IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) pour obtenir un handle d’icône.</span><span class="sxs-lookup"><span data-stu-id="1fbab-113">Call the [IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) method to get an icon handle.</span></span> 
    
<span data-ttu-id="1fbab-114">L’icône peut ensuite être affichée à l’aide des API Win32 standard.</span><span class="sxs-lookup"><span data-stu-id="1fbab-114">The icon can then be displayed using standard Win32 APIs.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="1fbab-115">Une fois que l’icône d’une classe de message, vérifiez tous leurs efforts pour mettre en cache cette icône.</span><span class="sxs-lookup"><span data-stu-id="1fbab-115">Once you have the icon for a message class, make every effort to cache that icon.</span></span> <span data-ttu-id="1fbab-116">Ne pas de mise en cache des icônes sérieusement affecte les performances des applications clientes.</span><span class="sxs-lookup"><span data-stu-id="1fbab-116">Not caching icons severely affects the performance of client applications.</span></span> <span data-ttu-id="1fbab-117">Lors de la mise en cache des icônes, veillez aux relations entre les classes de messages et leurs sous-classes.</span><span class="sxs-lookup"><span data-stu-id="1fbab-117">When caching icons, be careful of the relationships between message classes and their subclasses.</span></span> <span data-ttu-id="1fbab-118">Par exemple, si le formulaire IPM. Classe de message Note.Meeting.Cancel se répercuter dans IPM. Remarque, ne supposent que toutes les sous-classes de IPM. Remarque doit utiliser l’icône pour IPM. Note.</span><span class="sxs-lookup"><span data-stu-id="1fbab-118">For example, if the IPM.Note.Meeting.Cancel message class happens to resolve back to IPM.Note, do not assume that all subclasses of IPM.Note should use the icon for IPM.Note.</span></span> 
  

