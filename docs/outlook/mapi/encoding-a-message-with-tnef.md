---
title: Encodage d’un message avec TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b86d9a9-6876-4885-ae1e-8571b25b85cc
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: cdaa03cfbc0bbd0fcf6a320ecf8fae9f372d5781
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336700"
---
# <a name="encoding-a-message-with-tnef"></a><span data-ttu-id="b0dbf-103">Encodage d’un message avec TNEF</span><span class="sxs-lookup"><span data-stu-id="b0dbf-103">Encoding a message with TNEF</span></span>

<span data-ttu-id="b0dbf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0dbf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0dbf-105">Lors de l'envoi d'un message, le fournisseur de transport peut créer un fichier utilisé pour contenir le message pendant la transmission.</span><span class="sxs-lookup"><span data-stu-id="b0dbf-105">When a message is submitted, the transport provider can create a file that is used to contain the message during transmission.</span></span> <span data-ttu-id="b0dbf-106">Ensuite, une interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) est encapsulée autour du fichier.</span><span class="sxs-lookup"><span data-stu-id="b0dbf-106">Next, an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface is wrapped around the file.</span></span> <span data-ttu-id="b0dbf-107">Le fournisseur de transport utilise ensuite les méthodes [ITnef](itnefiunknown.md) pour écrire les propriétés de message dans le flux dans un format balisé qui permet de facilement décoder les propriétés par les fournisseurs de transport de réception.</span><span class="sxs-lookup"><span data-stu-id="b0dbf-107">The transport provider then uses [ITnef](itnefiunknown.md) methods to write the message properties to the stream in a tagged format that enables the properties to be easily decoded by the receiving transport providers.</span></span> 
  
<span data-ttu-id="b0dbf-108">**Pour représenter un message entier dans un seul fichier**</span><span class="sxs-lookup"><span data-stu-id="b0dbf-108">**To represent an entire message in a single file**</span></span>
  
1. <span data-ttu-id="b0dbf-109">Obtenir un objet TNEF en transmettant un objet [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) et un message dans la fonction [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="b0dbf-109">Obtain a TNEF object by passing an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object and a message into the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
2. <span data-ttu-id="b0dbf-110">Obtenir la liste de toutes les propriétés définies pour le message en appelant la méthode [IMAPIProp:: GetPropList](imapiprop-getproplist.md) .</span><span class="sxs-lookup"><span data-stu-id="b0dbf-110">Get a list of all defined properties for the message by calling the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
    
3. <span data-ttu-id="b0dbf-111">Utilisez les méthodes [IMAPIProp](imapipropiunknown.md) pour exclure toutes les propriétés prises en charge par le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="b0dbf-111">Use [IMAPIProp](imapipropiunknown.md) methods to exclude all properties supported by the messaging system.</span></span> <span data-ttu-id="b0dbf-112">À un moment approprié, écrivez ces propriétés dans le système de messagerie au format requis par le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="b0dbf-112">At an appropriate time, write those properties to the messaging system in the format required by the messaging system.</span></span> 
    
4. <span data-ttu-id="b0dbf-113">Appelez [ITnef:: AddProps](itnef-addprops.md) pour coder les autres propriétés, y compris toutes les pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="b0dbf-113">Call [ITnef::AddProps](itnef-addprops.md) to encode the remaining properties, including all attachments.</span></span> 
    
5. <span data-ttu-id="b0dbf-114">Appelez la méthode [ITnef:: Finish](itnef-finish.md) pour coder le message dans le flux TNEF une fois toutes les propriétés demandées ajoutées.</span><span class="sxs-lookup"><span data-stu-id="b0dbf-114">Call the [ITnef::Finish](itnef-finish.md) method to encode the message into the TNEF stream after all the requested properties are added.</span></span> 
    
6. <span data-ttu-id="b0dbf-115">Appelez la méthode [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) pour obtenir le texte du message balisé.</span><span class="sxs-lookup"><span data-stu-id="b0dbf-115">Call the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to obtain the tagged message text.</span></span> <span data-ttu-id="b0dbf-116">Ce texte balisé est écrit dans le système de messagerie à l'aide de méthodes de l'interface OLE [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b0dbf-116">This tagged text is written out to the messaging system using methods from the OLE [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
    
7. <span data-ttu-id="b0dbf-117">Appelez la méthode [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) pour libérer l'objet **ITnef** .</span><span class="sxs-lookup"><span data-stu-id="b0dbf-117">Call the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) method to release the **ITnef** object.</span></span> 
    
<span data-ttu-id="b0dbf-118">**Pour traiter un message TNEF entrant**</span><span class="sxs-lookup"><span data-stu-id="b0dbf-118">**To process an inbound TNEF message**</span></span>
  
1. <span data-ttu-id="b0dbf-119">Obtenir un objet de message MAPI à partir du spouleur MAPI et écrire les propriétés d'en-tête de message dans le nouveau message MAPI.</span><span class="sxs-lookup"><span data-stu-id="b0dbf-119">Get a MAPI message object from the MAPI spooler and write message header properties into the new MAPI message.</span></span>
    
2. <span data-ttu-id="b0dbf-120">Créer et initialiser un objet [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) pour contenir les données TNEF à partir du message entrant.</span><span class="sxs-lookup"><span data-stu-id="b0dbf-120">Create and initialize an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object to contain the TNEF data from the inbound message.</span></span> 
    
3. <span data-ttu-id="b0dbf-121">TransMettez le message MAPI et l'objet [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) à la fonction [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="b0dbf-121">Pass the MAPI message and the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object to the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
4. <span data-ttu-id="b0dbf-122">Décodez les informations contenues dans les données TNEF en appelant la méthode [ITnef:: ExtractProps](itnef-extractprops.md) .</span><span class="sxs-lookup"><span data-stu-id="b0dbf-122">Decode the information in the TNEF data by calling the [ITnef::ExtractProps](itnef-extractprops.md) method.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="b0dbf-123">Tout ce qui est décodé par **ExtractProps** remplace les propriétés décodées de l'enveloppe du message entrant.</span><span class="sxs-lookup"><span data-stu-id="b0dbf-123">Anything decoded by **ExtractProps** will overwrite properties decoded from the incoming message's envelope.</span></span> <span data-ttu-id="b0dbf-124">Autrement dit, les propriétés TNEF extraites remplacent les propriétés existantes dans un message.</span><span class="sxs-lookup"><span data-stu-id="b0dbf-124">That is, extracted TNEF properties will overwrite the existing properties in a message.</span></span> 
  
5. <span data-ttu-id="b0dbf-125">Traitez le texte du message balisé en appelant [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) et analysez le texte afin de récupérer les positions des pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="b0dbf-125">Process the tagged message text by calling [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) and parse the text to recover attachment positions.</span></span> 
    
6. <span data-ttu-id="b0dbf-126">Enregistrez le message en appelant [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="b0dbf-126">Save the message by calling [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
7. <span data-ttu-id="b0dbf-127">Libérez l'objet TNEF en appelant la méthode [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b0dbf-127">Release the TNEF object by calling the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) method.</span></span> 
    

