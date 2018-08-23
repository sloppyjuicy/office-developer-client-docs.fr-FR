---
title: Codage d’un message avec TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b86d9a9-6876-4885-ae1e-8571b25b85cc
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5043c338f309b5da21ca828a47daf1d8b6abfd5d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577750"
---
# <a name="encoding-a-message-with-tnef"></a><span data-ttu-id="94e41-103">Codage d’un message avec TNEF</span><span class="sxs-lookup"><span data-stu-id="94e41-103">Encoding a message with TNEF</span></span>

<span data-ttu-id="94e41-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94e41-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94e41-105">Lorsqu’un message est envoyé, le fournisseur de transport peut créer un fichier qui est utilisé pour contenir le message lors de la transmission.</span><span class="sxs-lookup"><span data-stu-id="94e41-105">When a message is submitted, the transport provider can create a file that is used to contain the message during transmission.</span></span> <span data-ttu-id="94e41-106">Ensuite, une interface [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) est autour du fichier.</span><span class="sxs-lookup"><span data-stu-id="94e41-106">Next, an [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface is wrapped around the file.</span></span> <span data-ttu-id="94e41-107">Le fournisseur de transport utilise ensuite les méthodes [ITnef](itnefiunknown.md) pour écrire les propriétés de message dans le flux dans un format avec balise qui permet les propriétés à décoder facilement par les fournisseurs de transport de réception.</span><span class="sxs-lookup"><span data-stu-id="94e41-107">The transport provider then uses [ITnef](itnefiunknown.md) methods to write the message properties to the stream in a tagged format that enables the properties to be easily decoded by the receiving transport providers.</span></span> 
  
<span data-ttu-id="94e41-108">**Pour représenter un message dans un seul fichier entier**</span><span class="sxs-lookup"><span data-stu-id="94e41-108">**To represent an entire message in a single file**</span></span>
  
1. <span data-ttu-id="94e41-109">Obtenir un objet TNEF en passant un objet [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) et un message dans la fonction [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="94e41-109">Obtain a TNEF object by passing an [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) object and a message into the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
2. <span data-ttu-id="94e41-110">Pour obtenir une liste de toutes les propriétés définies pour le message en appelant la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) .</span><span class="sxs-lookup"><span data-stu-id="94e41-110">Get a list of all defined properties for the message by calling the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
    
3. <span data-ttu-id="94e41-111">Utilisez les méthodes [IMAPIProp](imapipropiunknown.md) pour exclure toutes les propriétés prises en charge par le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="94e41-111">Use [IMAPIProp](imapipropiunknown.md) methods to exclude all properties supported by the messaging system.</span></span> <span data-ttu-id="94e41-112">À un moment opportun, écrire ces propriétés dans le système de messagerie dans le format requis par le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="94e41-112">At an appropriate time, write those properties to the messaging system in the format required by the messaging system.</span></span> 
    
4. <span data-ttu-id="94e41-113">Appelez [ITnef::AddProps](itnef-addprops.md) pour coder les propriétés restantes, y compris toutes les pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="94e41-113">Call [ITnef::AddProps](itnef-addprops.md) to encode the remaining properties, including all attachments.</span></span> 
    
5. <span data-ttu-id="94e41-114">Appelez la méthode [ITnef::Finish](itnef-finish.md) pour coder le message dans le flux TNEF après avoir ajouté toutes les propriétés demandées.</span><span class="sxs-lookup"><span data-stu-id="94e41-114">Call the [ITnef::Finish](itnef-finish.md) method to encode the message into the TNEF stream after all the requested properties are added.</span></span> 
    
6. <span data-ttu-id="94e41-115">Appelez la méthode [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) pour obtenir le texte du message avec balise.</span><span class="sxs-lookup"><span data-stu-id="94e41-115">Call the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to obtain the tagged message text.</span></span> <span data-ttu-id="94e41-116">Ce texte balisé est écrites dans le système de messagerie à l’aide des méthodes de l’interface OLE [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="94e41-116">This tagged text is written out to the messaging system using methods from the OLE [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
    
7. <span data-ttu-id="94e41-117">Appelez la méthode [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) pour libérer de l’objet **ITnef** .</span><span class="sxs-lookup"><span data-stu-id="94e41-117">Call the [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) method to release the **ITnef** object.</span></span> 
    
<span data-ttu-id="94e41-118">**Pour traiter un message TNEF entrant**</span><span class="sxs-lookup"><span data-stu-id="94e41-118">**To process an inbound TNEF message**</span></span>
  
1. <span data-ttu-id="94e41-119">Obtenir un objet de message MAPI dans le spouleur MAPI et écrire des propriétés d’en-tête de message dans le nouveau message MAPI.</span><span class="sxs-lookup"><span data-stu-id="94e41-119">Get a MAPI message object from the MAPI spooler and write message header properties into the new MAPI message.</span></span>
    
2. <span data-ttu-id="94e41-120">Créer et initialiser un objet [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) pour contenir les données TNEF à partir du message entrant.</span><span class="sxs-lookup"><span data-stu-id="94e41-120">Create and initialize an [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) object to contain the TNEF data from the inbound message.</span></span> 
    
3. <span data-ttu-id="94e41-121">Transmettre le message MAPI et l’objet [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) à la fonction [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="94e41-121">Pass the MAPI message and the [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) object to the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
4. <span data-ttu-id="94e41-122">Décoder les informations contenues dans les données TNEF en appelant la méthode [ITnef::ExtractProps](itnef-extractprops.md) .</span><span class="sxs-lookup"><span data-stu-id="94e41-122">Decode the information in the TNEF data by calling the [ITnef::ExtractProps](itnef-extractprops.md) method.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="94e41-123">Rien décodé par **ExtractProps** remplacera les propriétés décodées à partir de l’enveloppe du message entrant.</span><span class="sxs-lookup"><span data-stu-id="94e41-123">Anything decoded by **ExtractProps** will overwrite properties decoded from the incoming message's envelope.</span></span> <span data-ttu-id="94e41-124">Autrement dit, les propriétés extraites TNEF remplacera les propriétés existantes dans un message.</span><span class="sxs-lookup"><span data-stu-id="94e41-124">That is, extracted TNEF properties will overwrite the existing properties in a message.</span></span> 
  
5. <span data-ttu-id="94e41-125">Traiter le texte du message avec balise en appelant [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) et analysez le texte pour récupérer les positions des pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="94e41-125">Process the tagged message text by calling [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) and parse the text to recover attachment positions.</span></span> 
    
6. <span data-ttu-id="94e41-126">Enregistrez le message en appelant [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="94e41-126">Save the message by calling [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
7. <span data-ttu-id="94e41-127">Version de l’objet TNEF en appelant la méthode [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="94e41-127">Release the TNEF object by calling the [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) method.</span></span> 
    

