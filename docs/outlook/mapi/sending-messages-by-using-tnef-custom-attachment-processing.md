---
title: Envoi de messages à l’aide du traitement des pièces jointes personnalisé TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da318b6f-128a-44b5-8357-a130022030a1
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: f9d154b26319f5ed72b1abd6aeef307d07a63bda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339696"
---
# <a name="sending-messages-by-using-tnef-custom-attachment-processing"></a><span data-ttu-id="fc33f-103">Envoi de messages à l’aide du traitement des pièces jointes personnalisé TNEF</span><span class="sxs-lookup"><span data-stu-id="fc33f-103">Sending Messages by Using TNEF Custom Attachment Processing</span></span>

 
  
<span data-ttu-id="fc33f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc33f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc33f-105">Pour personnaliser le traitement des pièces jointes lors de l’envoi d’un message :</span><span class="sxs-lookup"><span data-stu-id="fc33f-105">To customize attachment processing when sending a message:</span></span>
  
1. <span data-ttu-id="fc33f-106">Obtenez un objet TNEF en passant une interface **IStream** et un message dans la [fonction OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="fc33f-106">Obtain a TNEF object by passing an **IStream** interface and a message into the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
2. <span data-ttu-id="fc33f-107">Obtenez la liste de toutes les propriétés définies pour le message en appelant la [méthode IMAPIProp::GetPropList.](imapiprop-getproplist.md)</span><span class="sxs-lookup"><span data-stu-id="fc33f-107">Get a list of all defined properties for the message by calling the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
    
3. <span data-ttu-id="fc33f-108">Utilisez [les méthodes IMAPIProp](imapipropiunknown.md) pour exclure toutes les propriétés pris en charge par le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="fc33f-108">Use [IMAPIProp](imapipropiunknown.md) methods to exclude all properties supported by the messaging system.</span></span> <span data-ttu-id="fc33f-109">Au moment approprié, écrivez ces propriétés dans le système de messagerie au format requis par le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="fc33f-109">At an appropriate time write those properties to the messaging system in the format required by the messaging system.</span></span> 
    
4. <span data-ttu-id="fc33f-110">Appelez la méthode [ITnef::AddProps](itnef-addprops.md) pour ajouter uniquement les propriétés du message , c’est-à-dire, aucune des propriétés sur les pièces jointes, en TNEF_PROP_MESSAGE_ONLY indicateur.</span><span class="sxs-lookup"><span data-stu-id="fc33f-110">Call the [ITnef::AddProps](itnef-addprops.md) method to add only the properties on the message — that is, none of the properties on the attachments — by setting the TNEF_PROP_MESSAGE_ONLY flag.</span></span> 
    
5. <span data-ttu-id="fc33f-111">Appelez [ITnef::AddProps](itnef-addprops.md) avec ces éléments : l’indicateur TNEF_PROP_EXCLUDE, un tableau de balises de propriétés qui contient la propriété **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) ou **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) et un identificateur de pièce jointe qui spécifie la pièce jointe à traiter.</span><span class="sxs-lookup"><span data-stu-id="fc33f-111">Call [ITnef::AddProps](itnef-addprops.md) with these items: the TNEF_PROP_EXCLUDE flag, a property tag array that contains the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) or **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property, and an attachment identifier that specifies the attachment to be processed.</span></span>
    
6. <span data-ttu-id="fc33f-112">Utilisez la méthode [ITnef::SetProps](itnef-setprops.md) pour ajouter la balise de propriété **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) avec une chaîne unique qui identifie la pièce jointe au système de messagerie si la pièce jointe possède un nom de fichier que le système de messagerie ne peut pas prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="fc33f-112">Use the [ITnef::SetProps](itnef-setprops.md) method to add the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property tag with a unique string that identifies the attachment to the messaging system if the attachment has a filename that the messaging system cannot support.</span></span> <span data-ttu-id="fc33f-113">Par exemple, plusieurs pièces jointes avec le même nom de fichier d’origine ou un nom de fichier qui n’est pas un nom de fichier valide pour le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="fc33f-113">For example, multiple attachments with the same original filename, or a filename that is not a valid filename for the messaging system.</span></span> <span data-ttu-id="fc33f-114">Cette chaîne est utilisée avec un numéro de clé lors de l’écriture des balises de pièce jointe dans le texte du message marqué pour associer une pièce jointe à ses données.</span><span class="sxs-lookup"><span data-stu-id="fc33f-114">This string will be used with a key number when writing the attachment tags in the tagged message text to associate an attachment with its data.</span></span> <span data-ttu-id="fc33f-115">Pour plus d’informations, voir texte de [message balisé TNEF.](tnef-tagged-message-text.md)</span><span class="sxs-lookup"><span data-stu-id="fc33f-115">For more information, see, [TNEF-Tagged Message Text](tnef-tagged-message-text.md).</span></span>
    
7. <span data-ttu-id="fc33f-116">Répétez **les appels AddProps** et **SetProps** pour chaque pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="fc33f-116">Repeat the **AddProps** and **SetProps** calls for each attachment.</span></span> 
    
8. <span data-ttu-id="fc33f-117">Appelez la [méthode ITnef::Finish](itnef-finish.md) pour encoder le message dans le flux TNEF une fois toutes les propriétés demandées ajoutées.</span><span class="sxs-lookup"><span data-stu-id="fc33f-117">Call the [ITnef::Finish](itnef-finish.md) method to encode the message into the TNEF stream after all the requested properties are added.</span></span> 
    
9. <span data-ttu-id="fc33f-118">Obtenez le texte du message marqué en appelant la [méthode ITnef::OpenTaggedBody.](itnef-opentaggedbody.md)</span><span class="sxs-lookup"><span data-stu-id="fc33f-118">Obtain the tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="fc33f-119">Ce texte balisé est lu à l’aide des méthodes de l’interface **IStream,** codé à l’aide du modèle de pièce jointe du système de messagerie et écrit dans le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="fc33f-119">This tagged text is read using methods from the **IStream** interface, encoded using the messaging system's attachment model, and written out to the messaging system.</span></span> 
    
10. <span data-ttu-id="fc33f-120">Appelez [la méthode IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) pour libérer [l’objet ITnef.](itnefiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="fc33f-120">Call the [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to release the [ITnef](itnefiunknown.md) object.</span></span> 
    
11. <span data-ttu-id="fc33f-121">Écrivez les pièces jointes restantes dans le système de messagerie via le modèle de pièces jointes du système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="fc33f-121">Write the remaining attachments to the messaging system through the messaging system's attachment model.</span></span>
    
<span data-ttu-id="fc33f-122">Votre fournisseur de transport doit utiliser la procédure décrite précédemment pour traiter les pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="fc33f-122">Your transport provider should use the previously described procedure to process attachments.</span></span> <span data-ttu-id="fc33f-123">Si ce n’est pas possible, le fournisseur de transport doit suivre les étapes suivantes pour le traitement personnalisé des pièces jointes :</span><span class="sxs-lookup"><span data-stu-id="fc33f-123">If that is not possible, the transport provider should use the following steps for customized attachment processing:</span></span>
  
1. <span data-ttu-id="fc33f-124">Le fournisseur de transport garantit que les **PR_ATTACH_TRANSPORT_NAME** de toutes les pièces jointes contiennent des valeurs uniques qui sont des identificateurs de pièces jointes valides pour le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="fc33f-124">The transport provider ensures that the **PR_ATTACH_TRANSPORT_NAME** properties of all the attachments contain unique values that are valid attachment identifiers for the messaging system.</span></span> 
    
2. <span data-ttu-id="fc33f-125">Le fournisseur de transport utilise ensuite un seul appel à **ITnef::AddProps** pour chaque pièce jointe, en passant l’indicateur TNEF_PROP_CONTAINED.</span><span class="sxs-lookup"><span data-stu-id="fc33f-125">The transport provider then uses a single call to **ITnef::AddProps** for each attachment, passing in the TNEF_PROP_CONTAINED flag.</span></span> 
    

