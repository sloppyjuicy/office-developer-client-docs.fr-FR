---
title: Rendu d'une pièce jointe au format RTF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b2a1a23f073d05e85c8203826e3407c5ae193f19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439792"
---
# <a name="rendering-an-attachment-in-rtf-text"></a><span data-ttu-id="17919-103">Rendu d'une pièce jointe au format RTF</span><span class="sxs-lookup"><span data-stu-id="17919-103">Rendering an Attachment in RTF Text</span></span>

  
  
<span data-ttu-id="17919-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17919-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17919-105">Les clients compatibles RTF (Rich Text Format) peuvent récupérer les informations relatives à la position du rendu à partir du texte du message RTF en recherchant la séquence d'échappement suivante dans la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) du message:</span><span class="sxs-lookup"><span data-stu-id="17919-105">Rich Text Format (RTF)-aware clients can retrieve rendering position information from RTF message text by looking for the following escape sequence in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property:</span></span>
  
 `\objattph`
  
 <span data-ttu-id="17919-106">**Pour localiser les informations de rendu dans le texte mis en forme**</span><span class="sxs-lookup"><span data-stu-id="17919-106">**To locate rendering information in formatted text**</span></span>
  
1. <span data-ttu-id="17919-107">Appelez **IMessage:: GetAttachmentTable** pour accéder à la table des pièces jointes du message.</span><span class="sxs-lookup"><span data-stu-id="17919-107">Call **IMessage::GetAttachmentTable** to access the message's attachment table.</span></span> <span data-ttu-id="17919-108">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span><span class="sxs-lookup"><span data-stu-id="17919-108">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span></span>
    
2. <span data-ttu-id="17919-109">Créez une restriction de propriété qui limite le tableau aux lignes qui n'ont pas **PR_RENDERING_POSITION** égal à-1.</span><span class="sxs-lookup"><span data-stu-id="17919-109">Build a property restriction that limits the table to rows that have **PR_RENDERING_POSITION** not equal to -1.</span></span> <span data-ttu-id="17919-110">Pour plus d'informations, voir **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="17919-110">For more information, see **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="17919-111">Appeler **IMAPITable:: Restrict** pour appliquer la restriction.</span><span class="sxs-lookup"><span data-stu-id="17919-111">Call **IMAPITable::Restrict** to enforce the restriction.</span></span> <span data-ttu-id="17919-112">Pour plus d'informations, consultez la rubrique [IMAPITable:: Restrict](imapitable-restrict.md).</span><span class="sxs-lookup"><span data-stu-id="17919-112">For more information, see [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
    
4. <span data-ttu-id="17919-113">Appelez **IMAPITable:: SortTable** pour trier les pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="17919-113">Call **IMAPITable::SortTable** to sort the attachments.</span></span> <span data-ttu-id="17919-114">Pour plus d'informations, consultez la rubrique [IMAPITable:: SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="17919-114">For more information, see [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
5. <span data-ttu-id="17919-115">Appelez la fonction **IMAPITable:: QueryRows** pour extraire les lignes appropriées.</span><span class="sxs-lookup"><span data-stu-id="17919-115">Call **IMAPITable::QueryRows** to retrieve the appropriate rows.</span></span> <span data-ttu-id="17919-116">Pour plus d'informations, consultez la rubrique [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="17919-116">For more information, see [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
    
6. <span data-ttu-id="17919-117">Appelez la méthode **IMAPIProp:: OpenProperty** du message pour extraire **PR_RTF_COMPRESSED** avec l'interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="17919-117">Call the message's **IMAPIProp::OpenProperty** method to retrieve **PR_RTF_COMPRESSED** with the **IStream** interface.</span></span> <span data-ttu-id="17919-118">Pour plus d'informations, voir [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) et **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="17919-118">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
    
7. <span data-ttu-id="17919-119">Analysez le flux, en recherchant l'espace réservé `\objattph`de rendu,.</span><span class="sxs-lookup"><span data-stu-id="17919-119">Scan the stream, looking for the rendering placeholder,  `\objattph`.</span></span> <span data-ttu-id="17919-120">Le caractère qui suit cet espace réservé est l'emplacement de la pièce jointe suivante dans le tableau trié.</span><span class="sxs-lookup"><span data-stu-id="17919-120">The character following this placeholder is the place for the next attachment in the sorted table.</span></span>
    

