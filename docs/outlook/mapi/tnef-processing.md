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
ms.openlocfilehash: 066ad3dfb64161e326b92fef7774d5b3b9461d8a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339598"
---
# <a name="tnef-processing"></a><span data-ttu-id="6de5e-103">Traitement TNEF</span><span class="sxs-lookup"><span data-stu-id="6de5e-103">TNEF Processing</span></span>

  
  
<span data-ttu-id="6de5e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6de5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6de5e-105">La série d’actions suivante décrit comment les transports utilisent les méthodes TNEF pour traiter les messages sortants et entrants.</span><span class="sxs-lookup"><span data-stu-id="6de5e-105">The following series of actions describe how transports use TNEF methods to process outgoing and incoming messages.</span></span>
  
 <span data-ttu-id="6de5e-106">**Pour envoyer un message qui inclut un flux TNEF**</span><span class="sxs-lookup"><span data-stu-id="6de5e-106">**To send a message that includes a TNEF stream**</span></span>
  
1. <span data-ttu-id="6de5e-107">Traiter les propriétés de message qui sont pris en charge par le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="6de5e-107">Process the message properties that are supported by the messaging system.</span></span>
    
2. <span data-ttu-id="6de5e-108">Marquez le message d’une manière spécifique à l’implémentation afin que le fournisseur de transport de réception puisse déterminer que le message nécessite un traitement TNEF.</span><span class="sxs-lookup"><span data-stu-id="6de5e-108">Mark the message in an implementation specific way so that the receiving transport provider can determine that the message requires TNEF processing.</span></span> <span data-ttu-id="6de5e-109">Par exemple, un fournisseur de transport TNEF envoyant un message à un système de messagerie SMTP peut ajouter un champ d’en-tête personnalisé tel que « X-CONTAINS-TNEF » pour indiquer que le message contient des données TNEF.</span><span class="sxs-lookup"><span data-stu-id="6de5e-109">For example, a TNEF transport provider sending to an SMTP messaging system might add a custom header field like "X-CONTAINS-TNEF" to indicate that the message contains TNEF data.</span></span>
    
3. <span data-ttu-id="6de5e-110">Obtenez un objet TNEF et utilisez-le pour encapsuler les propriétés de message non pris en charge par le système de messagerie dans un flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="6de5e-110">Obtain a TNEF object and use it to encapsulate the message properties not supported by the messaging system into a TNEF stream.</span></span>
    
4. <span data-ttu-id="6de5e-111">Encodez le flux TNEF à l’aide du modèle de pièce jointe du système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="6de5e-111">Encode the TNEF stream using the messaging system's attachment model.</span></span> <span data-ttu-id="6de5e-112">Par exemple, si le modèle de pièce jointe sous-jacent consiste à uuencoder les pièces jointes et les ajoute au texte du message, le fournisseur de transport doit uuencoder le flux TNEF dans une autre pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="6de5e-112">For example, if the underlying attachment model is to uuencode attachments and append them to the message text, then the transport provider must uuencode the TNEF stream into another attachment.</span></span> <span data-ttu-id="6de5e-113">Le fournisseur de transport doit également implémenter une méthode pour reconnaître quelle pièce jointe contient le flux TNEF codé lorsqu’il reçoit un message.</span><span class="sxs-lookup"><span data-stu-id="6de5e-113">The transport provider must also implement a method for recognizing which attachment contains the encoded TNEF stream when it receives a message.</span></span> <span data-ttu-id="6de5e-114">La manière standard de marquer cette pièce jointe consiste à lui donner le nom de fichier de pièce jointe « WINMAIL ». DAT ».</span><span class="sxs-lookup"><span data-stu-id="6de5e-114">The standard way to mark this attachment is to give it an attachment filename of "WINMAIL.DAT".</span></span> <span data-ttu-id="6de5e-115">Si votre fournisseur de transport le fait, tous les autres fournisseurs de transport activés pour le TNEF qui suivent cette convention pourront interopérer avec elle.</span><span class="sxs-lookup"><span data-stu-id="6de5e-115">If your transport provider does this, any other TNEF-enabled transport providers that follow this convention will be able to interoperate with it.</span></span>
    
5. <span data-ttu-id="6de5e-116">Utilisez [les méthodes d’interface ITnef : IUnknown](itnefiunknown.md) pour insérer des balises décrivant les positions des pièces jointes du message dans le texte du message.</span><span class="sxs-lookup"><span data-stu-id="6de5e-116">Use [ITnef : IUnknown](itnefiunknown.md) interface methods to insert tags describing the positions of message attachments in the message text.</span></span> 
    
6. <span data-ttu-id="6de5e-117">Accédez au texte du message balisé via [les méthodes IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) et envoyez-le au système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="6de5e-117">Access the tagged message text through [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) methods, and send it to the messaging system.</span></span> 
    
 <span data-ttu-id="6de5e-118">**Pour récupérer des propriétés encapsulées**</span><span class="sxs-lookup"><span data-stu-id="6de5e-118">**To retrieve encapsulated properties**</span></span>
  
1. <span data-ttu-id="6de5e-119">Écrivez les propriétés prise en charge par le système de messagerie dans un nouveau message, y compris le texte de message balisé qui contient les propriétés encapsulées.</span><span class="sxs-lookup"><span data-stu-id="6de5e-119">Write the properties supported by the messaging system into a new message, including the tagged message text that contains the encapsulated properties.</span></span>
    
2. <span data-ttu-id="6de5e-120">Décodez le flux TNEF à partir de la pièce jointe appropriée.</span><span class="sxs-lookup"><span data-stu-id="6de5e-120">Decode the TNEF stream from the proper attachment.</span></span>
    
3. <span data-ttu-id="6de5e-121">Décodez les autres pièces jointes et écrivez-les dans les nouvelles pièces jointes MAPI d’un message.</span><span class="sxs-lookup"><span data-stu-id="6de5e-121">Decode any other attachments and write them to new MAPI attachments on a message.</span></span>
    
4. <span data-ttu-id="6de5e-122">Ouvrez le flux TNEF pour le décodage à l’aide de la [fonction OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="6de5e-122">Open the TNEF stream for decoding using the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
5. <span data-ttu-id="6de5e-123">Utilisez la [méthode ITnef::ExtractProps](itnef-extractprops.md) pour décoder le flux TNEF et écrire les propriétés encapsulées dans le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="6de5e-123">Use the [ITnef::ExtractProps](itnef-extractprops.md) method to decode the TNEF stream and write the encapsulated properties into the new message.</span></span> <span data-ttu-id="6de5e-124">Toutes les propriétés codées qui sont des doublons de propriétés non codées ont la valeur overwrite les propriétés non codées lorsque les propriétés codées sont décodées.</span><span class="sxs-lookup"><span data-stu-id="6de5e-124">Any encoded properties that are duplicates of nonencoded properties will overwrite the nonencoded properties when the encoded properties are decoded.</span></span> 
    
6. <span data-ttu-id="6de5e-125">Utilisez la [méthode ITnef::OpenTaggedBody](itnef-opentaggedbody.md) pour lire le texte du message afin de récupérer les positions des pièces jointes à partir des balises du texte du message.</span><span class="sxs-lookup"><span data-stu-id="6de5e-125">Use the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to parse the message text to recover attachment positions from the tags in the message text.</span></span> 
    

