---
title: Réception de messages à l'aide du traitement de pièces jointes personnalisé TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb5082fa-8fe3-46fe-b2de-b6dd1af79ea7
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: 046b537d41b318fa857ef77f1906edcf2c3aa2bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429319"
---
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a><span data-ttu-id="46961-103">Réception de messages à l'aide du traitement de pièces jointes personnalisé TNEF</span><span class="sxs-lookup"><span data-stu-id="46961-103">Receiving Messages by Using TNEF Custom Attachment Processing</span></span>

 
  
<span data-ttu-id="46961-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46961-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46961-105">Pour recevoir un message TNEF avec traitement des pièces jointes personnalisées:</span><span class="sxs-lookup"><span data-stu-id="46961-105">To receive a TNEF message with customized attachment processing:</span></span>
  
1. <span data-ttu-id="46961-106">ImPortez toutes les propriétés transmissibles, telles que prises en charge par le système de messagerie, du message entrant dans un nouveau message MAPI.</span><span class="sxs-lookup"><span data-stu-id="46961-106">Import all the transmittable properties — those that the messaging system supports — from the incoming message into a new MAPI message.</span></span> <span data-ttu-id="46961-107">Cela inclut le texte du message, qui contient le flux de données TNEF.</span><span class="sxs-lookup"><span data-stu-id="46961-107">This includes the message text, which contains the TNEF data stream.</span></span>
    
2. <span data-ttu-id="46961-108">Identifiez et décodez la pièce jointe spéciale qui contient le flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="46961-108">Identify and decode the special attachment that contains the TNEF stream.</span></span>
    
3. <span data-ttu-id="46961-109">Extraire toutes les pièces jointes du message entrant en pièces jointes MAPI dans le nouveau message MAPI.</span><span class="sxs-lookup"><span data-stu-id="46961-109">Extract all the attachments from the incoming message into MAPI attachments on the new MAPI message.</span></span> <span data-ttu-id="46961-110">Les noms de fichier récupérés ou d'autres marqueurs d'identification des pièces jointes doivent être placés dans la propriété **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) des nouvelles pièces jointes afin que la méthode [ITnef:: ExtractProps](itnef-extractprops.md) peut ensuite associer la pièce jointe correcte aux balises de pièces jointes codées dans le texte du message.</span><span class="sxs-lookup"><span data-stu-id="46961-110">The recovered filenames, or other identifying markers on the attachments, should be placed into the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property of the new attachments so that the [ITnef::ExtractProps](itnef-extractprops.md) method can later associate the correct attachment with the attachment tags encoded in the message text.</span></span> 
    
4. <span data-ttu-id="46961-111">Créez une interface OLE **IStream** pour encapsuler le flux TNEF décodé et utilisez cet objet avec le nouveau message MAPI dans un appel à la fonction [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="46961-111">Create an OLE **IStream** interface to wrap around the decoded TNEF stream and use that object along with the new MAPI message in a call to the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
5. <span data-ttu-id="46961-112">Appelez la méthode **ITnef:: ExtractProps** pour récupérer les propriétés non transmissibles du message à partir du flux de données TNEF.</span><span class="sxs-lookup"><span data-stu-id="46961-112">Call the **ITnef::ExtractProps** method to recover the nontransmittable properties on the message from the TNEF data stream.</span></span> 
    
6. <span data-ttu-id="46961-113">Appelez la méthode [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) avec les indicateurs MAPI_CREATE et MAPI_MODIFY définis.</span><span class="sxs-lookup"><span data-stu-id="46961-113">Call the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method with the MAPI_CREATE and MAPI_MODIFY flags set.</span></span> <span data-ttu-id="46961-114">Cet appel supprime les balises de pièce jointe du texte du message et les convertit en informations de position des pièces jointes dans le message MAPI.</span><span class="sxs-lookup"><span data-stu-id="46961-114">This call removes the attachment tags from the message text and converts them into attachment position information in the MAPI message.</span></span> 
    
7. <span data-ttu-id="46961-115">Remise du message via le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="46961-115">Deliver the message through the MAPI spooler.</span></span>
    

