---
title: Rendu d’une pièce jointe dans le texte RTF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: cf22e360a0319a662c9b7dd31856dbb6eccec02a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786988"
---
# <a name="rendering-an-attachment-in-rtf-text"></a><span data-ttu-id="c615b-103">Rendu d’une pièce jointe dans le texte RTF</span><span class="sxs-lookup"><span data-stu-id="c615b-103">Rendering an Attachment in RTF Text</span></span>

  
  
<span data-ttu-id="c615b-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c615b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c615b-105">Rich Text Format (RTF)-clients qui n’utilisent peut récupérer des informations de position de rendu de texte du message au format RTF en recherchant la séquence d’échappement suivante dans la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) du message :</span><span class="sxs-lookup"><span data-stu-id="c615b-105">Rich Text Format (RTF)-aware clients can retrieve rendering position information from RTF message text by looking for the following escape sequence in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property:</span></span>
  
 `\objattph`
  
 <span data-ttu-id="c615b-106">**Pour rechercher des informations de rendu dans le texte mis en forme**</span><span class="sxs-lookup"><span data-stu-id="c615b-106">**To locate rendering information in formatted text**</span></span>
  
1. <span data-ttu-id="c615b-107">Appelez **IMessage::GetAttachmentTable** pour accéder à table de pièce jointe du message.</span><span class="sxs-lookup"><span data-stu-id="c615b-107">Call **IMessage::GetAttachmentTable** to access the message's attachment table.</span></span> <span data-ttu-id="c615b-108">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span><span class="sxs-lookup"><span data-stu-id="c615b-108">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span></span>
    
2. <span data-ttu-id="c615b-109">Créer une restriction de propriété qui limite la table aux lignes qui ont **PR_RENDERING_POSITION** pas égal à -1.</span><span class="sxs-lookup"><span data-stu-id="c615b-109">Build a property restriction that limits the table to rows that have **PR_RENDERING_POSITION** not equal to -1.</span></span> <span data-ttu-id="c615b-110">Pour plus d’informations, voir **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c615b-110">For more information, see **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="c615b-111">Appelez **IMAPITable** pour appliquer la restriction.</span><span class="sxs-lookup"><span data-stu-id="c615b-111">Call **IMAPITable::Restrict** to enforce the restriction.</span></span> <span data-ttu-id="c615b-112">Pour plus d’informations, voir [IMAPITable](imapitable-restrict.md).</span><span class="sxs-lookup"><span data-stu-id="c615b-112">For more information, see [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
    
4. <span data-ttu-id="c615b-113">Appelez **IMAPITable::SortTable** pour trier les pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="c615b-113">Call **IMAPITable::SortTable** to sort the attachments.</span></span> <span data-ttu-id="c615b-114">Pour plus d’informations, voir [IMAPITable::SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="c615b-114">For more information, see [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
5. <span data-ttu-id="c615b-115">Appelez **IMAPITable::QueryRows** pour récupérer les lignes appropriées.</span><span class="sxs-lookup"><span data-stu-id="c615b-115">Call **IMAPITable::QueryRows** to retrieve the appropriate rows.</span></span> <span data-ttu-id="c615b-116">Pour plus d’informations, voir [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="c615b-116">For more information, see [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
    
6. <span data-ttu-id="c615b-117">Appelez la méthode de **IMAPIProp::OpenProperty** du message pour récupérer **PR_RTF_COMPRESSED** avec l’interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="c615b-117">Call the message's **IMAPIProp::OpenProperty** method to retrieve **PR_RTF_COMPRESSED** with the **IStream** interface.</span></span> <span data-ttu-id="c615b-118">Pour plus d’informations, voir [IMAPIProp::OpenProperty](imapiprop-openproperty.md) et **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="c615b-118">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
    
7. <span data-ttu-id="c615b-119">Analyser le flux, recherchez l’espace réservé de rendu, `\objattph`.</span><span class="sxs-lookup"><span data-stu-id="c615b-119">Scan the stream, looking for the rendering placeholder,  `\objattph`.</span></span> <span data-ttu-id="c615b-120">Le caractère suivant cet espace réservé est l’endroit de la pièce jointe suivante dans le tableau trié.</span><span class="sxs-lookup"><span data-stu-id="c615b-120">The character following this placeholder is the place for the next attachment in the sorted table.</span></span>
    

