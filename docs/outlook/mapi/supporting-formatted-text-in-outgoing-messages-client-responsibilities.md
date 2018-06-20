---
title: Prise en charge de texte mis en forme dans les responsabilités du Client les Messages sortants
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: d5ce2e6b0f10ff6c2f6fd91ca9f73953f3ee7cd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787273"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a><span data-ttu-id="827b2-103">Prise en charge au format texte dans les Messages sortants : responsabilités du Client</span><span class="sxs-lookup"><span data-stu-id="827b2-103">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="827b2-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="827b2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="827b2-105">Applications clientes définir la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou la propriété **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) pour un message sortant.</span><span class="sxs-lookup"><span data-stu-id="827b2-105">Client applications set the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, or the **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) property for an outgoing message.</span></span> <span data-ttu-id="827b2-106">Les clients qui prennent en charge que le texte brut définir uniquement la propriété **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="827b2-106">Clients that support only plain text set only the **PR_BODY** property.</span></span> <span data-ttu-id="827b2-107">Rich Text Format (RTF)-connaissance clients peuvent définir à la fois **PR_BODY** et propriétés **PR_RTF_COMPRESSED** , ou uniquement **PR_RTF_COMPRESSED**, selon le message Enregistrer fournisseur utilisé.</span><span class="sxs-lookup"><span data-stu-id="827b2-107">Rich Text Format (RTF)-aware clients might set both **PR_BODY** and **PR_RTF_COMPRESSED** properties, or only **PR_RTF_COMPRESSED**, depending on the message store provider being used.</span></span> <span data-ttu-id="827b2-108">Clients prenant en charge HTML définir la propriété **PR_HTML** .</span><span class="sxs-lookup"><span data-stu-id="827b2-108">HTML-aware clients set the **PR_HTML** property.</span></span> 
  
<span data-ttu-id="827b2-109">Il est important pour un client pour vérifier la propriété de **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de la banque de messages pour déterminer si la banque prend en charge au format RTF.</span><span class="sxs-lookup"><span data-stu-id="827b2-109">It is important for a client to check its message store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to determine whether the store supports RTF.</span></span> <span data-ttu-id="827b2-110">Si la banque de messages n’est pas en charge au format RTF, un client prenant en charge les RTF définit les propriétés de la **PR_BODY** et **PR_RTF_COMPRESSED** pour chaque message sortant.</span><span class="sxs-lookup"><span data-stu-id="827b2-110">If the message store is not RTF-aware, an RTF-aware client sets both the **PR_BODY** and **PR_RTF_COMPRESSED** properties for each outgoing message.</span></span> 
  
<span data-ttu-id="827b2-111">Si la banque de messages est prenant en charge au format RTF, seule la propriété **PR_RTF_COMPRESSED** doit être définie.</span><span class="sxs-lookup"><span data-stu-id="827b2-111">If the message store is RTF-aware, only the **PR_RTF_COMPRESSED** property needs to be set.</span></span> 
  
 <span data-ttu-id="827b2-112">**Pour définir les PR_RTF_COMPRESSED et vérifiez que la synchronisation processus se produit en tant que nécessaires, RTF prenant en charge des clients**</span><span class="sxs-lookup"><span data-stu-id="827b2-112">**To set PR_RTF_COMPRESSED and ensure that the synchronization process occurs as necessary, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="827b2-113">Appelez la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété **PR_RTF_COMPRESSED** , définition des indicateurs n’et MAPI_CREATE.</span><span class="sxs-lookup"><span data-stu-id="827b2-113">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, setting both the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="827b2-114">MAPI_CREATE garantit que toutes les nouvelles données remplacent les anciennes données et ne permet de rendre les remplacements.</span><span class="sxs-lookup"><span data-stu-id="827b2-114">MAPI_CREATE ensures that any new data replaces any old data and MAPI_MODIFY enables you to make those replacements.</span></span> 
    
2. <span data-ttu-id="827b2-115">Appelez la fonction [WrapCompressedRTFStream](wrapcompressedrtfstream.md) , en transmettant STORE_UNCOMPRESSED_RTF si la banque de messages définit le bit STORE_UNCOMPRESSED_RTF dans sa propriété **PR_STORE_SUPPORT_MASK** , pour obtenir une version non compressée de le **PR_RTF_COMPRESSED **flux renvoyé par **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="827b2-115">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing STORE_UNCOMPRESSED_RTF if the message store sets the STORE_UNCOMPRESSED_RTF bit in its **PR_STORE_SUPPORT_MASK** property, to get an uncompressed version of the **PR_RTF_COMPRESSED** stream returned from **OpenProperty**.</span></span>
    
3. <span data-ttu-id="827b2-116">Écrire les données de texte du message dans le flux non compressé renvoyé à partir de **WrapCompressedRTFStream**.</span><span class="sxs-lookup"><span data-stu-id="827b2-116">Write the message text data to the uncompressed stream returned from **WrapCompressedRTFStream**.</span></span>
    
4. <span data-ttu-id="827b2-117">Valider et libérer les flux et non compressées.</span><span class="sxs-lookup"><span data-stu-id="827b2-117">Commit and release both the uncompressed and compressed streams.</span></span>
    
<span data-ttu-id="827b2-118">À ce stade, si le fournisseur de banque de message prend en charge le format RTF, vous avez réalisé tout ce qui est requis.</span><span class="sxs-lookup"><span data-stu-id="827b2-118">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="827b2-119">Vous pouvez dépendent du fournisseur de magasin de message pour gérer le processus de synchronisation et la création de la propriété **PR_BODY** , si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="827b2-119">You can depend on the message store provider to handle the synchronization process and the creation of the **PR_BODY** property, if necessary.</span></span> <span data-ttu-id="827b2-120">Toutefois, si le fournisseur de banque de messages n’accepte pas le format RTF, vous devez appeler la fonction [RTFSync](rtfsync.md) pour synchroniser le texte avec mise en forme, l’indicateur RTF_SYNC_RTF_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="827b2-120">However, if the message store provider does not support RTF, you must call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting, setting the RTF_SYNC_RTF_CHANGED flag.</span></span> 
  

