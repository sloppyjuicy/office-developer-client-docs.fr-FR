---
title: Prise en charge du texte formaté dans les responsabilités du client des messages sortants
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 01d5ae3fd06d570e15336fad9538f01e586cd0f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431602"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a><span data-ttu-id="d2641-103">Prise en charge du texte formaté dans les messages sortants : responsabilités du client</span><span class="sxs-lookup"><span data-stu-id="d2641-103">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="d2641-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2641-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2641-105">Les applications clientes définissent la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou la propriété **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) pour un message sortant.</span><span class="sxs-lookup"><span data-stu-id="d2641-105">Client applications set the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, or the **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) property for an outgoing message.</span></span> <span data-ttu-id="d2641-106">Les clients qui ne supportent que le texte simple définissent uniquement **PR_BODY** propriété.</span><span class="sxs-lookup"><span data-stu-id="d2641-106">Clients that support only plain text set only the **PR_BODY** property.</span></span> <span data-ttu-id="d2641-107">Les clients au format RTF (Rich  Text Format) peuvent définir les propriétés PR_BODY et **PR_RTF_COMPRESSED,** ou uniquement **PR_RTF_COMPRESSED,** en fonction du fournisseur de magasin de messages utilisé.</span><span class="sxs-lookup"><span data-stu-id="d2641-107">Rich Text Format (RTF)-aware clients might set both **PR_BODY** and **PR_RTF_COMPRESSED** properties, or only **PR_RTF_COMPRESSED**, depending on the message store provider being used.</span></span> <span data-ttu-id="d2641-108">Les clients html définissent la **propriété PR_HTML.**</span><span class="sxs-lookup"><span data-stu-id="d2641-108">HTML-aware clients set the **PR_HTML** property.</span></span> 
  
<span data-ttu-id="d2641-109">Il est important pour un client de vérifier la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de sa magasin pour déterminer si la magasin prend en charge RTF.</span><span class="sxs-lookup"><span data-stu-id="d2641-109">It is important for a client to check its message store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to determine whether the store supports RTF.</span></span> <span data-ttu-id="d2641-110">Si la magasin de messages n’est pas sensible au  rtf, un client rtf définit les propriétés PR_BODY et **PR_RTF_COMPRESSED** pour chaque message sortant.</span><span class="sxs-lookup"><span data-stu-id="d2641-110">If the message store is not RTF-aware, an RTF-aware client sets both the **PR_BODY** and **PR_RTF_COMPRESSED** properties for each outgoing message.</span></span> 
  
<span data-ttu-id="d2641-111">Si la magasin de messages est sensible au rtf, seule la **propriété PR_RTF_COMPRESSED** doit être définie.</span><span class="sxs-lookup"><span data-stu-id="d2641-111">If the message store is RTF-aware, only the **PR_RTF_COMPRESSED** property needs to be set.</span></span> 
  
 <span data-ttu-id="d2641-112">**Pour définir PR_RTF_COMPRESSED et vous assurer que le processus de synchronisation se produit si nécessaire, les clients rtF**</span><span class="sxs-lookup"><span data-stu-id="d2641-112">**To set PR_RTF_COMPRESSED and ensure that the synchronization process occurs as necessary, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="d2641-113">Appelez la [méthode IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété **PR_RTF_COMPRESSED,** en MAPI_CREATE et MAPI_MODIFY indicateurs.</span><span class="sxs-lookup"><span data-stu-id="d2641-113">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, setting both the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="d2641-114">MAPI_CREATE s’assure que toutes les nouvelles données remplacent les anciennes données et MAPI_MODIFY vous permet d’effectuer ces remplacements.</span><span class="sxs-lookup"><span data-stu-id="d2641-114">MAPI_CREATE ensures that any new data replaces any old data and MAPI_MODIFY enables you to make those replacements.</span></span> 
    
2. <span data-ttu-id="d2641-115">Appelez la fonction [WrapCompressedRTFStream,](wrapcompressedrtfstream.md) en passant STORE_UNCOMPRESSED_RTF si la boutique de messages définit le bit STORE_UNCOMPRESSED_RTF dans sa propriété **PR_STORE_SUPPORT_MASK,** pour obtenir une version non compressée du flux **PR_RTF_COMPRESSED** renvoyée par **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="d2641-115">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing STORE_UNCOMPRESSED_RTF if the message store sets the STORE_UNCOMPRESSED_RTF bit in its **PR_STORE_SUPPORT_MASK** property, to get an uncompressed version of the **PR_RTF_COMPRESSED** stream returned from **OpenProperty**.</span></span>
    
3. <span data-ttu-id="d2641-116">Écrivez les données de texte du message dans le flux non compressé renvoyé par **WrapCompressedRTFStream**.</span><span class="sxs-lookup"><span data-stu-id="d2641-116">Write the message text data to the uncompressed stream returned from **WrapCompressedRTFStream**.</span></span>
    
4. <span data-ttu-id="d2641-117">Valider et libérer les flux non compressés et non compressés.</span><span class="sxs-lookup"><span data-stu-id="d2641-117">Commit and release both the uncompressed and compressed streams.</span></span>
    
<span data-ttu-id="d2641-118">À ce stade, si le fournisseur de magasin de messages prend en charge rtf, vous avez effectué tout ce qui est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d2641-118">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="d2641-119">Vous pouvez dépendre du fournisseur de la boutique de messages pour gérer le processus de synchronisation et la création de la **propriété PR_BODY,** si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d2641-119">You can depend on the message store provider to handle the synchronization process and the creation of the **PR_BODY** property, if necessary.</span></span> <span data-ttu-id="d2641-120">Toutefois, si le fournisseur de magasin de messages ne prend pas en charge le format RTF, vous devez appeler la fonction [RTFSync](rtfsync.md) pour synchroniser le texte avec la mise en forme, en RTF_SYNC_RTF_CHANGED’indicateur.</span><span class="sxs-lookup"><span data-stu-id="d2641-120">However, if the message store provider does not support RTF, you must call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting, setting the RTF_SYNC_RTF_CHANGED flag.</span></span> 
  

