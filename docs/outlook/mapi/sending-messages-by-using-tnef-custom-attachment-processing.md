---
title: Envoi de messages via le traitement de pièce jointe personnalisé TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da318b6f-128a-44b5-8357-a130022030a1
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: f9d154b26319f5ed72b1abd6aeef307d07a63bda
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388566"
---
# <a name="sending-messages-by-using-tnef-custom-attachment-processing"></a><span data-ttu-id="a3522-103">Envoi de messages via le traitement de pièce jointe personnalisé TNEF</span><span class="sxs-lookup"><span data-stu-id="a3522-103">Sending Messages by Using TNEF Custom Attachment Processing</span></span>

 
  
<span data-ttu-id="a3522-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3522-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3522-105">Pour personnaliser le traitement des pièces jointes lors de l’envoi d’un message :</span><span class="sxs-lookup"><span data-stu-id="a3522-105">To customize attachment processing when sending a message:</span></span>
  
1. <span data-ttu-id="a3522-106">Obtenir un objet TNEF en passant une interface **IStream** et un message dans la fonction [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="a3522-106">Obtain a TNEF object by passing an **IStream** interface and a message into the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
2. <span data-ttu-id="a3522-107">Pour obtenir une liste de toutes les propriétés définies pour le message en appelant la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) .</span><span class="sxs-lookup"><span data-stu-id="a3522-107">Get a list of all defined properties for the message by calling the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
    
3. <span data-ttu-id="a3522-108">Utilisez les méthodes [IMAPIProp](imapipropiunknown.md) pour exclure toutes les propriétés prises en charge par le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="a3522-108">Use [IMAPIProp](imapipropiunknown.md) methods to exclude all properties supported by the messaging system.</span></span> <span data-ttu-id="a3522-109">À un moment opportun écrire ces propriétés dans le système de messagerie dans le format requis par le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="a3522-109">At an appropriate time write those properties to the messaging system in the format required by the messaging system.</span></span> 
    
4. <span data-ttu-id="a3522-110">Appelez la méthode [ITnef::AddProps](itnef-addprops.md) pour ajouter uniquement les propriétés sur le message — autrement dit, aucune des propriétés sur les pièces jointes, en définissant l’indicateur TNEF_PROP_MESSAGE_ONLY.</span><span class="sxs-lookup"><span data-stu-id="a3522-110">Call the [ITnef::AddProps](itnef-addprops.md) method to add only the properties on the message — that is, none of the properties on the attachments — by setting the TNEF_PROP_MESSAGE_ONLY flag.</span></span> 
    
5. <span data-ttu-id="a3522-111">Appelez [ITnef::AddProps](itnef-addprops.md) avec ces éléments : l’indicateur TNEF_PROP_EXCLUDE, un tableau de balise de propriété qui contient le **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) ou **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) propriété et un identificateur de pièce jointe qui spécifie la pièce jointe à traiter.</span><span class="sxs-lookup"><span data-stu-id="a3522-111">Call [ITnef::AddProps](itnef-addprops.md) with these items: the TNEF_PROP_EXCLUDE flag, a property tag array that contains the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) or **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property, and an attachment identifier that specifies the attachment to be processed.</span></span>
    
6. <span data-ttu-id="a3522-112">Utilisez la méthode [ITnef::SetProps](itnef-setprops.md) pour ajouter la balise de propriété **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) avec une chaîne unique qui identifie le système de messagerie de la pièce jointe si la pièce jointe comporte un nom de fichier que le système de messagerie ne peut pas prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="a3522-112">Use the [ITnef::SetProps](itnef-setprops.md) method to add the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property tag with a unique string that identifies the attachment to the messaging system if the attachment has a filename that the messaging system cannot support.</span></span> <span data-ttu-id="a3522-113">Par exemple, plusieurs pièces jointes avec le même nom de fichier d’origine, ou un nom de fichier qui n’est pas un nom de fichier valide pour le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="a3522-113">For example, multiple attachments with the same original filename, or a filename that is not a valid filename for the messaging system.</span></span> <span data-ttu-id="a3522-114">Cette chaîne est utilisée avec un numéro de clé lorsque vous écrivez les balises de pièce jointe dans le texte du message avec balise pour associer une pièce jointe à ses données.</span><span class="sxs-lookup"><span data-stu-id="a3522-114">This string will be used with a key number when writing the attachment tags in the tagged message text to associate an attachment with its data.</span></span> <span data-ttu-id="a3522-115">Pour plus d’informations, voir [TNEF-Tagged le texte du Message](tnef-tagged-message-text.md).</span><span class="sxs-lookup"><span data-stu-id="a3522-115">For more information, see, [TNEF-Tagged Message Text](tnef-tagged-message-text.md).</span></span>
    
7. <span data-ttu-id="a3522-116">Répétez les appels **AddProps** et **SetProps** pour chaque pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="a3522-116">Repeat the **AddProps** and **SetProps** calls for each attachment.</span></span> 
    
8. <span data-ttu-id="a3522-117">Appelez la méthode [ITnef::Finish](itnef-finish.md) pour coder le message dans le flux TNEF après avoir ajouté toutes les propriétés demandées.</span><span class="sxs-lookup"><span data-stu-id="a3522-117">Call the [ITnef::Finish](itnef-finish.md) method to encode the message into the TNEF stream after all the requested properties are added.</span></span> 
    
9. <span data-ttu-id="a3522-118">Obtenir le texte du message avec balise en appelant la méthode [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) .</span><span class="sxs-lookup"><span data-stu-id="a3522-118">Obtain the tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="a3522-119">Ce texte référencé est en lecture à l’aide des méthodes de l’interface **IStream** , codé à l’aide du modèle de pièce jointe du système de messagerie et écrites dans le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="a3522-119">This tagged text is read using methods from the **IStream** interface, encoded using the messaging system's attachment model, and written out to the messaging system.</span></span> 
    
10. <span data-ttu-id="a3522-120">Appelez la méthode [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) pour libérer de l’objet [ITnef](itnefiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="a3522-120">Call the [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to release the [ITnef](itnefiunknown.md) object.</span></span> 
    
11. <span data-ttu-id="a3522-121">Écrire des pièces jointes restants sur le système de messagerie via le modèle de pièce jointe du système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="a3522-121">Write the remaining attachments to the messaging system through the messaging system's attachment model.</span></span>
    
<span data-ttu-id="a3522-122">Votre fournisseur de transport doit utiliser la procédure décrite précédemment aux pièces jointes des processus.</span><span class="sxs-lookup"><span data-stu-id="a3522-122">Your transport provider should use the previously described procedure to process attachments.</span></span> <span data-ttu-id="a3522-123">Si ce n’est pas possible, le fournisseur de transport doit utiliser les étapes suivantes pour le traitement personnalisé des pièces jointes :</span><span class="sxs-lookup"><span data-stu-id="a3522-123">If that is not possible, the transport provider should use the following steps for customized attachment processing:</span></span>
  
1. <span data-ttu-id="a3522-124">Le fournisseur de transport garantit que les propriétés **PR_ATTACH_TRANSPORT_NAME** de toutes les pièces jointes contiennent des valeurs uniques sont des identificateurs de pièce jointe valide pour le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="a3522-124">The transport provider ensures that the **PR_ATTACH_TRANSPORT_NAME** properties of all the attachments contain unique values that are valid attachment identifiers for the messaging system.</span></span> 
    
2. <span data-ttu-id="a3522-125">Le fournisseur de transport utilise un seul appel à **ITnef::AddProps** pour chaque pièce jointe, en passant l’indicateur TNEF_PROP_CONTAINED.</span><span class="sxs-lookup"><span data-stu-id="a3522-125">The transport provider then uses a single call to **ITnef::AddProps** for each attachment, passing in the TNEF_PROP_CONTAINED flag.</span></span> 
    

