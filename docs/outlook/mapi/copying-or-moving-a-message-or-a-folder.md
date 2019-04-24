---
title: Copie ou déplacement d’un message ou dossier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: 'Dernière modification: 08 08, 2011'
ms.openlocfilehash: c5e92c44d7078560ed84d72b3477d5cf2e809353
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333039"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a><span data-ttu-id="0fb81-103">Copie ou déplacement d’un message ou dossier</span><span class="sxs-lookup"><span data-stu-id="0fb81-103">Copying or moving a message or a folder</span></span>
  
<span data-ttu-id="0fb81-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0fb81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0fb81-105">Un client peut utiliser l'une des quatre méthodes de copie ou de déplacement d'un message ou d'un dossier:</span><span class="sxs-lookup"><span data-stu-id="0fb81-105">A client can use one of four methods to copy or move a message or a folder:</span></span>
  
- [<span data-ttu-id="0fb81-106">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="0fb81-106">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
- [<span data-ttu-id="0fb81-107">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="0fb81-107">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
- [<span data-ttu-id="0fb81-108">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="0fb81-108">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="0fb81-109">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="0fb81-109">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
<span data-ttu-id="0fb81-110">En définissant les indicateurs et paramètres appropriés, **CopyTo** et **CopyProps** peuvent être configurés pour fonctionner comme **CopyFolder** ou **CopyMessages**.</span><span class="sxs-lookup"><span data-stu-id="0fb81-110">By setting the appropriate flags and parameters, **CopyTo** and **CopyProps** can be made to work just like **CopyFolder** or **CopyMessages**.</span></span> <span data-ttu-id="0fb81-111">Tenez compte des points suivants lors du choix de la méthode à appeler:</span><span class="sxs-lookup"><span data-stu-id="0fb81-111">Consider the following issues when deciding which method to call:</span></span>
  
- <span data-ttu-id="0fb81-112">Est-ce que vous copiez ou déplacez un dossier ou un message?</span><span class="sxs-lookup"><span data-stu-id="0fb81-112">Are you copying or moving a folder or a message?</span></span>
    
- <span data-ttu-id="0fb81-113">Dans quelle mesure le dossier ou le message doit-il être déplacé ou copié?</span><span class="sxs-lookup"><span data-stu-id="0fb81-113">How much do you know about the folder or message to be moved or copied?</span></span>
    
- <span data-ttu-id="0fb81-114">Combien de propriétés du dossier ou du message seront déplacées ou copiées?</span><span class="sxs-lookup"><span data-stu-id="0fb81-114">How many of the folder or message's properties will be moved or copied?</span></span>
    
<span data-ttu-id="0fb81-115">Vous pouvez utiliser les méthodes **IMAPIProp** pour copier ou déplacer un dossier ou un message.</span><span class="sxs-lookup"><span data-stu-id="0fb81-115">You can use the **IMAPIProp** methods to copy or move either a folder or a message.</span></span> <span data-ttu-id="0fb81-116">**IMAPIFolder:: CopyMessages** fonctionne avec les messages uniquement; **IMAPIFolder:: CopyFolder** ne fonctionne qu'avec des dossiers.</span><span class="sxs-lookup"><span data-stu-id="0fb81-116">**IMAPIFolder::CopyMessages** works with messages only; **IMAPIFolder::CopyFolder** works with folders only.</span></span> 
  
<span data-ttu-id="0fb81-117">Que l'utilisation des méthodes **IMAPIFolder** ne nécessite aucune connaissance des propriétés prises en charge par le dossier ou le message à copier ou déplacer, vous devez avoir des connaissances pour utiliser les méthodes **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="0fb81-117">Whereas using the **IMAPIFolder** methods does not require any knowledge of the properties supported by the folder or message to be copied or moved, you must have some knowledge to use the **IMAPIProp** methods.</span></span> <span data-ttu-id="0fb81-118">Avec **IMAPIProp:: CopyProps**, vous devez être en mesure de spécifier explicitement les propriétés du dossier ou du message que vous souhaitez copier ou déplacer.</span><span class="sxs-lookup"><span data-stu-id="0fb81-118">With **IMAPIProp::CopyProps**, you must be able to explicitly specify which of the folder or message properties that you want to copy or move.</span></span> <span data-ttu-id="0fb81-119">Avec **IMAPIProp:: CopyTo**, sauf si vous souhaitez copier ou déplacer toutes les propriétés, vous devez explicitement spécifier celles qui doivent être exclues.</span><span class="sxs-lookup"><span data-stu-id="0fb81-119">With **IMAPIProp::CopyTo**, unless you want to copy or move all of the properties, you must explicitly specify which ones should be excluded.</span></span> <span data-ttu-id="0fb81-120">Pour plus d'informations sur ces méthodes, reportez-vous à la rubrique [copie des propriétés MAPI](copying-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="0fb81-120">For more information about these methods, see [Copying MAPI Properties](copying-mapi-properties.md).</span></span>
  
<span data-ttu-id="0fb81-121">Le nombre de propriétés à copier ou à déplacer peut affecter votre décision quant à la méthode à utiliser.</span><span class="sxs-lookup"><span data-stu-id="0fb81-121">The number of properties to be copied or moved can affect your decision as to which method to use.</span></span> <span data-ttu-id="0fb81-122">Si vous copiez ou déplacez plusieurs messages, appelez **IMAPIFolder:: CopyMessages**.</span><span class="sxs-lookup"><span data-stu-id="0fb81-122">If you are copying or moving multiple messages, call **IMAPIFolder::CopyMessages**.</span></span> <span data-ttu-id="0fb81-123">Une autre option consiste à appeler **IMAPIProp:: CopyProps** pour copier uniquement la propriété **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) du dossier.</span><span class="sxs-lookup"><span data-stu-id="0fb81-123">An alternate choice is to call **IMAPIProp::CopyProps** to copy only the folder's **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span> <span data-ttu-id="0fb81-124">La procédure suivante montre comment utiliser **CopyMessages**.</span><span class="sxs-lookup"><span data-stu-id="0fb81-124">The following procedure shows how to use **CopyMessages**.</span></span> 
  
### <a name="to-copy-or-move-one-or-more-messages"></a><span data-ttu-id="0fb81-125">Pour copier ou déplacer un ou plusieurs messages</span><span class="sxs-lookup"><span data-stu-id="0fb81-125">To copy or move one or more messages</span></span>
  
1. <span data-ttu-id="0fb81-126">Recherchez des identificateurs d'entrée valides pour les dossiers source et de destination.</span><span class="sxs-lookup"><span data-stu-id="0fb81-126">Locate valid entry identifiers for the source and destination folders.</span></span>
    
2. <span data-ttu-id="0fb81-127">Ouvrez ces dossiers en mode lecture/écriture en appelant [IMAPISession:: OpenEntry](imapisession-openentry.md) ou [IMsgStore:: OpenEntry](imsgstore-openentry.md) et en définissant l'indicateur MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="0fb81-127">Open these folders in read/write mode by calling either [IMAPISession::OpenEntry](imapisession-openentry.md) or [IMsgStore::OpenEntry](imsgstore-openentry.md) and setting the MAPI_MODIFY flag.</span></span> 
    
3. <span data-ttu-id="0fb81-128">Vérifiez que le pointeur d'interface renvoyé depuis **OpenEntry** est un pointeur d'interface **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="0fb81-128">Check that the interface pointer returned from **OpenEntry** is an **IMAPIFolder** interface pointer.</span></span> <span data-ttu-id="0fb81-129">Si ce n'est pas le cas, convertissez-le en type LPMAPIFOLDER.</span><span class="sxs-lookup"><span data-stu-id="0fb81-129">If not, cast it to the LPMAPIFOLDER type.</span></span> 
    
4. <span data-ttu-id="0fb81-130">Créez un tableau d'identificateurs d'entrée représentant un ou plusieurs messages à copier ou déplacer.</span><span class="sxs-lookup"><span data-stu-id="0fb81-130">Create an array of entry identifiers representing the one or more messages to be copied or moved.</span></span> 
    
5. <span data-ttu-id="0fb81-131">Appelez **IMAPIFolder:: CopyMessages** avec les indicateurs suivants:</span><span class="sxs-lookup"><span data-stu-id="0fb81-131">Call **IMAPIFolder::CopyMessages** with the following flags set:</span></span> 
    
   - <span data-ttu-id="0fb81-132">MESSAGE_MOVE, si vous voulez effectuer une opération de déplacement.</span><span class="sxs-lookup"><span data-stu-id="0fb81-132">MESSAGE_MOVE, if you want to perform a move operation.</span></span> 
    
   - <span data-ttu-id="0fb81-133">MESSAGE_DIALOG et transmettez un descripteur de fenêtre dans le paramètre _ulUIParam_ , si vous souhaitez que le dossier affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="0fb81-133">MESSAGE_DIALOG and pass a window handle in the  _ulUIParam_ parameter, if you want the folder to show a progress indicator.</span></span> 
    
6. <span data-ttu-id="0fb81-134">Libérez les pointeurs **IMAPIFolder** pour les dossiers source et de destination.</span><span class="sxs-lookup"><span data-stu-id="0fb81-134">Release the **IMAPIFolder** pointers for the source and destination folders.</span></span> 
    
<span data-ttu-id="0fb81-135">Si vous souhaitez copier l'intégralité du contenu d'un dossier dans un autre dossier, appelez la méthode **IMAPIFolder:: CopyFolder** ou **IMAPIProp:: CopyTo** du dossier source.</span><span class="sxs-lookup"><span data-stu-id="0fb81-135">If you want to copy the complete contents of a folder to another folder, call the source folder's **IMAPIFolder::CopyFolder** or **IMAPIProp::CopyTo** method.</span></span> 
  
<span data-ttu-id="0fb81-136">Pour copier quelques-unes des propriétés d'un dossier, appelez sa méthode **IMAPIProp:: CopyProps** .</span><span class="sxs-lookup"><span data-stu-id="0fb81-136">To copy a few of a folder's properties, call its **IMAPIProp::CopyProps** method.</span></span> <span data-ttu-id="0fb81-137">Pour copier la plupart des propriétés d'un dossier, appelez **IMAPIProp:: CopyTo**.</span><span class="sxs-lookup"><span data-stu-id="0fb81-137">To copy most of a folder's properties, call **IMAPIProp::CopyTo**.</span></span> 
  
<span data-ttu-id="0fb81-138">Par exemple, si vous souhaitez copier les propriétés **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) et **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) d'un dossier, vous disposez des options suivantes:</span><span class="sxs-lookup"><span data-stu-id="0fb81-138">For example, if you want to copy a folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) and **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) properties, you have the following options:</span></span>
  
- <span data-ttu-id="0fb81-139">Appelez **IMAPIFolder:: CopyFolder** pour copier toutes les propriétés du dossier, puis supprimez les propriétés indésirables du nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="0fb81-139">Call **IMAPIFolder::CopyFolder** to copy all of the folder properties and then delete the unwanted ones from the new folder.</span></span> 
    
- <span data-ttu-id="0fb81-140">Appelez **CopyTo** et excluez toutes les propriétés du dossier à l'exception de **PR_DISPLAY_NAME** et **PR_COMMENT**.</span><span class="sxs-lookup"><span data-stu-id="0fb81-140">Call **CopyTo** and exclude all of the folder's properties except for **PR_DISPLAY_NAME** and **PR_COMMENT**.</span></span> 
    
- <span data-ttu-id="0fb81-141">Appelez **CopyProps**, en passant **PR_DISPLAY_NAME** et **PR_COMMENT** dans le tableau include.</span><span class="sxs-lookup"><span data-stu-id="0fb81-141">Call **CopyProps**, passing **PR_DISPLAY_NAME** and **PR_COMMENT** in the include array.</span></span> 
    
<span data-ttu-id="0fb81-142">Dans ce cas, **CopyProps** est le meilleur choix car il est destiné à être utilisé pour copier un petit ensemble de propriétés et est l'appel le plus simple à implémenter.</span><span class="sxs-lookup"><span data-stu-id="0fb81-142">In this case, **CopyProps** is the best choice because it is meant to be used to copy a small set of properties and is the easiest call to implement.</span></span> 
  
<span data-ttu-id="0fb81-143">Pour copier ou déplacer uniquement les propriétés de dossier, sans inclure les messages, appelez la méthode **IMAPIProp:: CopyTo** du dossier et excluez les propriétés suivantes:</span><span class="sxs-lookup"><span data-stu-id="0fb81-143">To copy or move only folder properties, without including messages, call the folder's **IMAPIProp::CopyTo** method and exclude the following properties:</span></span> 
  
- <span data-ttu-id="0fb81-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0fb81-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>
    
- <span data-ttu-id="0fb81-145">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0fb81-145">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>
    
<span data-ttu-id="0fb81-146">Les méthodes Copy peuvent renvoyer S_OK, indiquant le total de la réussite, MAPI_W_PARTIAL_COMPLETION, indiquant la réussite partielle ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="0fb81-146">The copy methods can return S_OK, indicating total success, MAPI_W_PARTIAL_COMPLETION, indicating partial success, or an error.</span></span> <span data-ttu-id="0fb81-147">Si MAPI_W_PARTIAL_COMPLETION est renvoyé, utilisez la macro **HR_FAILED** pour accéder à une erreur plus spécifique.</span><span class="sxs-lookup"><span data-stu-id="0fb81-147">If MAPI_W_PARTIAL_COMPLETION is returned, use the **HR_FAILED** macro to access a more specific error.</span></span> <span data-ttu-id="0fb81-148">Pour plus d'informations, consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="0fb81-148">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
  
<span data-ttu-id="0fb81-149">Si vous copiez des messages d'une banque de messages vers une autre et que Unicode n'est pas pris en charge par les deux, sachez que les informations peuvent être perdues en raison de la conversion de la page de codes.</span><span class="sxs-lookup"><span data-stu-id="0fb81-149">If you copy messages from one message store to another and Unicode is not supported by both, be aware that information can be lost due to code page conversion.</span></span> <span data-ttu-id="0fb81-150">En règle générale, vous ne pouvez pas savoir si la Banque de messages prend en charge un ou les deux formats, ce qui empêche de déterminer s'il faut copier les propriétés de texte sous forme de chaînes ASCII ou Unicode.</span><span class="sxs-lookup"><span data-stu-id="0fb81-150">Usually you cannot know if the message stores support one or both formats, making it impossible to determine whether to copy text properties as ASCII strings or as Unicode strings.</span></span> <span data-ttu-id="0fb81-151">Si vous prenez en charge Unicode, essayez d'effectuer une copie Unicode; Si elle échoue avec la valeur d'erreur MAPI_E_BAD_CHARWIDTH, Resort to ASCII.</span><span class="sxs-lookup"><span data-stu-id="0fb81-151">If you support Unicode, try to perform a Unicode copy; if it fails with the error value MAPI_E_BAD_CHARWIDTH, resort to ASCII.</span></span>
  

