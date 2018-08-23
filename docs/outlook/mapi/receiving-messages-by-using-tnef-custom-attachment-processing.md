---
title: Réception de messages via le traitement de pièce jointe personnalisé TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb5082fa-8fe3-46fe-b2de-b6dd1af79ea7
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: 67c202e5130bd35e1277c5260bc1702043eadd95
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588026"
---
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a><span data-ttu-id="449d6-103">Réception de messages via le traitement de pièce jointe personnalisé TNEF</span><span class="sxs-lookup"><span data-stu-id="449d6-103">Receiving Messages by Using TNEF Custom Attachment Processing</span></span>

 
  
<span data-ttu-id="449d6-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="449d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="449d6-105">Pour recevoir un message TNEF avec traitement personnalisé des pièces jointes :</span><span class="sxs-lookup"><span data-stu-id="449d6-105">To receive a TNEF message with customized attachment processing:</span></span>
  
1. <span data-ttu-id="449d6-106">Importer toutes les propriétés transmissible — ceux qui prend en charge par le système de messagerie, à partir du message entrant dans un nouveau message MAPI.</span><span class="sxs-lookup"><span data-stu-id="449d6-106">Import all the transmittable properties — those that the messaging system supports — from the incoming message into a new MAPI message.</span></span> <span data-ttu-id="449d6-107">Cela inclut le texte du message, qui contient le flux de données TNEF.</span><span class="sxs-lookup"><span data-stu-id="449d6-107">This includes the message text, which contains the TNEF data stream.</span></span>
    
2. <span data-ttu-id="449d6-108">Identifier et décoder la pièce jointe spéciale qui contient le flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="449d6-108">Identify and decode the special attachment that contains the TNEF stream.</span></span>
    
3. <span data-ttu-id="449d6-109">Extraire toutes les pièces jointes à partir du message entrant dans les pièces jointes MAPI sur le nouveau message MAPI.</span><span class="sxs-lookup"><span data-stu-id="449d6-109">Extract all the attachments from the incoming message into MAPI attachments on the new MAPI message.</span></span> <span data-ttu-id="449d6-110">Les noms de fichiers récupérée ou autres marques d’identification sur les pièces jointes, doivent être placés dans la propriété **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) des nouvelles pièces jointes ainsi que la méthode [ITnef::ExtractProps](itnef-extractprops.md) pouvez l’associer ultérieurement la pièce jointe correcte avec les balises de pièce jointe codés dans le texte du message.</span><span class="sxs-lookup"><span data-stu-id="449d6-110">The recovered filenames, or other identifying markers on the attachments, should be placed into the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property of the new attachments so that the [ITnef::ExtractProps](itnef-extractprops.md) method can later associate the correct attachment with the attachment tags encoded in the message text.</span></span> 
    
4. <span data-ttu-id="449d6-111">Créer une interface OLE **IStream** habiller le flux TNEF décodé et d’utiliser cet objet ainsi que le nouveau message MAPI dans un appel à la fonction [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="449d6-111">Create an OLE **IStream** interface to wrap around the decoded TNEF stream and use that object along with the new MAPI message in a call to the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
5. <span data-ttu-id="449d6-112">Appelez la méthode **ITnef::ExtractProps** pour récupérer les propriétés nontransmittable sur le message à partir du flux de données TNEF.</span><span class="sxs-lookup"><span data-stu-id="449d6-112">Call the **ITnef::ExtractProps** method to recover the nontransmittable properties on the message from the TNEF data stream.</span></span> 
    
6. <span data-ttu-id="449d6-113">Appelez la méthode [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) avec l’ensemble d’indicateurs MAPI_CREATE et ne.</span><span class="sxs-lookup"><span data-stu-id="449d6-113">Call the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method with the MAPI_CREATE and MAPI_MODIFY flags set.</span></span> <span data-ttu-id="449d6-114">Cet appel supprime les balises de pièce jointe dans le texte du message et les convertit les informations de position des pièces jointes dans le message MAPI.</span><span class="sxs-lookup"><span data-stu-id="449d6-114">This call removes the attachment tags from the message text and converts them into attachment position information in the MAPI message.</span></span> 
    
7. <span data-ttu-id="449d6-115">Remettre le message via le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="449d6-115">Deliver the message through the MAPI spooler.</span></span>
    

