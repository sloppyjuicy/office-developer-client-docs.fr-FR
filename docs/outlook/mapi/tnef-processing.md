---
title: Traitement TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d324fb3-d917-4502-b3a4-179c479deb79
description: 'Derni�re modification�: jeudi 5 juillet 2012'
ms.openlocfilehash: bd9cc49f5d1d865d5d6b222677df0dd62ec36fd6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787355"
---
# <a name="tnef-processing"></a><span data-ttu-id="763c9-103">Traitement TNEF</span><span class="sxs-lookup"><span data-stu-id="763c9-103">TNEF Processing</span></span>

  
  
<span data-ttu-id="763c9-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="763c9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="763c9-105">La série d’actions suivante décrire comment des transports utilisent les méthodes TNEF pour traiter les messages entrants et sortants.</span><span class="sxs-lookup"><span data-stu-id="763c9-105">The following series of actions describe how transports use TNEF methods to process outgoing and incoming messages.</span></span>
  
 <span data-ttu-id="763c9-106">**Pour envoyer un message qui inclut un flux de données TNEF**</span><span class="sxs-lookup"><span data-stu-id="763c9-106">**To send a message that includes a TNEF stream**</span></span>
  
1. <span data-ttu-id="763c9-107">Traiter les propriétés des messages qui sont pris en charge par le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="763c9-107">Process the message properties that are supported by the messaging system.</span></span>
    
2. <span data-ttu-id="763c9-108">Marquer le message dans une implémentation spécifique façon afin que le fournisseur de transport de réception peut déterminer que le message nécessite de traitement TNEF.</span><span class="sxs-lookup"><span data-stu-id="763c9-108">Mark the message in an implementation specific way so that the receiving transport provider can determine that the message requires TNEF processing.</span></span> <span data-ttu-id="763c9-109">Par exemple, un fournisseur de transport TNEF l’envoi à un serveur SMTP système de messagerie peut ajouter un champ d’en-tête personnalisé comme « X-contient-TNEF » pour indiquer que le message contient des données TNEF.</span><span class="sxs-lookup"><span data-stu-id="763c9-109">For example, a TNEF transport provider sending to an SMTP messaging system might add a custom header field like "X-CONTAINS-TNEF" to indicate that the message contains TNEF data.</span></span>
    
3. <span data-ttu-id="763c9-110">Obtenir un objet TNEF et utilisez-la pour encapsuler les propriétés de message non pris en charge par le système de messagerie dans un objet stream TNEF.</span><span class="sxs-lookup"><span data-stu-id="763c9-110">Obtain a TNEF object and use it to encapsulate the message properties not supported by the messaging system into a TNEF stream.</span></span>
    
4. <span data-ttu-id="763c9-111">Coder le flux TNEF à l’aide du modèle de pièce jointe du système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="763c9-111">Encode the TNEF stream using the messaging system's attachment model.</span></span> <span data-ttu-id="763c9-112">Par exemple, si le modèle de pièce jointe sous-jacent est uuencode des pièces jointes et les ajouter au texte du message, le fournisseur de transport doit uuencode le flux TNEF dans une autre pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="763c9-112">For example, if the underlying attachment model is to uuencode attachments and append them to the message text, then the transport provider must uuencode the TNEF stream into another attachment.</span></span> <span data-ttu-id="763c9-113">Le fournisseur de transport doit également implémenter une méthode pour reconnaître les pièces jointes contient le flux TNEF codé lorsqu’il reçoit un message.</span><span class="sxs-lookup"><span data-stu-id="763c9-113">The transport provider must also implement a method for recognizing which attachment contains the encoded TNEF stream when it receives a message.</span></span> <span data-ttu-id="763c9-114">La méthode standard pour marquer cette pièce jointe est pour lui donner un nom de fichier des pièces jointes de « WINMAIL. DONNÉES ».</span><span class="sxs-lookup"><span data-stu-id="763c9-114">The standard way to mark this attachment is to give it an attachment filename of "WINMAIL.DAT".</span></span> <span data-ttu-id="763c9-115">Si votre fournisseur de transport pour cela, tous les fournisseurs de transport prenant en charge TNEF qui suivent cette convention sera en mesure d’interagir avec lui.</span><span class="sxs-lookup"><span data-stu-id="763c9-115">If your transport provider does this, any other TNEF-enabled transport providers that follow this convention will be able to interoperate with it.</span></span>
    
5. <span data-ttu-id="763c9-116">Utilisez [ITnef : IUnknown](itnefiunknown.md) méthodes pour insérer des balises décrivant les positions des pièces jointes des messages dans le texte du message de l’interface.</span><span class="sxs-lookup"><span data-stu-id="763c9-116">Use [ITnef : IUnknown](itnefiunknown.md) interface methods to insert tags describing the positions of message attachments in the message text.</span></span> 
    
6. <span data-ttu-id="763c9-117">Accès le texte du message avec balise via les méthodes [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) et l’envoyer au système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="763c9-117">Access the tagged message text through [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) methods, and send it to the messaging system.</span></span> 
    
 <span data-ttu-id="763c9-118">**Pour récupérer les propriétés encapsulées**</span><span class="sxs-lookup"><span data-stu-id="763c9-118">**To retrieve encapsulated properties**</span></span>
  
1. <span data-ttu-id="763c9-119">Écrire les propriétés prises en charge par le système de messagerie dans un nouveau message, y compris le texte du message avec balise qui contient les propriétés encapsulées.</span><span class="sxs-lookup"><span data-stu-id="763c9-119">Write the properties supported by the messaging system into a new message, including the tagged message text that contains the encapsulated properties.</span></span>
    
2. <span data-ttu-id="763c9-120">Décoder le flux TNEF à partir de la pièce jointe appropriée.</span><span class="sxs-lookup"><span data-stu-id="763c9-120">Decode the TNEF stream from the proper attachment.</span></span>
    
3. <span data-ttu-id="763c9-121">Décoder toutes les pièces jointes et les écrire dans les nouvelles pièces jointes MAPI d’un message.</span><span class="sxs-lookup"><span data-stu-id="763c9-121">Decode any other attachments and write them to new MAPI attachments on a message.</span></span>
    
4. <span data-ttu-id="763c9-122">Ouvrez le flux TNEF de décodage à l’aide de la fonction [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="763c9-122">Open the TNEF stream for decoding using the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
5. <span data-ttu-id="763c9-123">Utilisez la méthode [ITnef::ExtractProps](itnef-extractprops.md) pour décoder le flux TNEF et écrire les propriétés encapsulées dans le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="763c9-123">Use the [ITnef::ExtractProps](itnef-extractprops.md) method to decode the TNEF stream and write the encapsulated properties into the new message.</span></span> <span data-ttu-id="763c9-124">Les propriétés codées doublons des propriétés nonencoded remplace les propriétés nonencoded les propriétés codées sont décodées.</span><span class="sxs-lookup"><span data-stu-id="763c9-124">Any encoded properties that are duplicates of nonencoded properties will overwrite the nonencoded properties when the encoded properties are decoded.</span></span> 
    
6. <span data-ttu-id="763c9-125">Utilisez la méthode [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) pour analyser le texte du message pour récupérer les positions des pièces jointes dans les balises dans le texte du message.</span><span class="sxs-lookup"><span data-stu-id="763c9-125">Use the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to parse the message text to recover attachment positions from the tags in the message text.</span></span> 
    

