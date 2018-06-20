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
# <a name="rendering-an-attachment-in-rtf-text"></a>Rendu d’une pièce jointe dans le texte RTF

  
  
**S’applique à**: Outlook 
  
Rich Text Format (RTF)-clients qui n’utilisent peut récupérer des informations de position de rendu de texte du message au format RTF en recherchant la séquence d’échappement suivante dans la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) du message :
  
 `\objattph`
  
 **Pour rechercher des informations de rendu dans le texte mis en forme**
  
1. Appelez **IMessage::GetAttachmentTable** pour accéder à table de pièce jointe du message. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
2. Créer une restriction de propriété qui limite la table aux lignes qui ont **PR_RENDERING_POSITION** pas égal à -1. Pour plus d’informations, voir **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).
    
3. Appelez **IMAPITable** pour appliquer la restriction. Pour plus d’informations, voir [IMAPITable](imapitable-restrict.md).
    
4. Appelez **IMAPITable::SortTable** pour trier les pièces jointes. Pour plus d’informations, voir [IMAPITable::SortTable](imapitable-sorttable.md).
    
5. Appelez **IMAPITable::QueryRows** pour récupérer les lignes appropriées. Pour plus d’informations, voir [IMAPITable::QueryRows](imapitable-queryrows.md).
    
6. Appelez la méthode de **IMAPIProp::OpenProperty** du message pour récupérer **PR_RTF_COMPRESSED** avec l’interface **IStream** . Pour plus d’informations, voir [IMAPIProp::OpenProperty](imapiprop-openproperty.md) et **PR_RTF_COMPRESSED**.
    
7. Analyser le flux, recherchez l’espace réservé de rendu, `\objattph`. Le caractère suivant cet espace réservé est l’endroit de la pièce jointe suivante dans le tableau trié.
    

