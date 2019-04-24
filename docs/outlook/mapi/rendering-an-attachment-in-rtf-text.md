---
title: Rendu d'une pièce jointe au format RTF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: b2a1a23f073d05e85c8203826e3407c5ae193f19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280359"
---
# <a name="rendering-an-attachment-in-rtf-text"></a>Rendu d'une pièce jointe au format RTF

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les clients compatibles RTF (Rich Text Format) peuvent récupérer les informations relatives à la position du rendu à partir du texte du message RTF en recherchant la séquence d'échappement suivante dans la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) du message:
  
 `\objattph`
  
 **Pour localiser les informations de rendu dans le texte mis en forme**
  
1. Appelez **IMessage:: GetAttachmentTable** pour accéder à la table des pièces jointes du message. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
2. Créez une restriction de propriété qui limite le tableau aux lignes qui n'ont pas **PR_RENDERING_POSITION** égal à-1. Pour plus d'informations, voir **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).
    
3. Appeler **IMAPITable:: Restrict** pour appliquer la restriction. Pour plus d'informations, consultez la rubrique [IMAPITable:: Restrict](imapitable-restrict.md).
    
4. Appelez **IMAPITable:: SortTable** pour trier les pièces jointes. Pour plus d'informations, consultez la rubrique [IMAPITable:: SortTable](imapitable-sorttable.md).
    
5. Appelez la fonction **IMAPITable:: QueryRows** pour extraire les lignes appropriées. Pour plus d'informations, consultez la rubrique [IMAPITable:: QueryRows](imapitable-queryrows.md).
    
6. Appelez la méthode **IMAPIProp:: OpenProperty** du message pour extraire **PR_RTF_COMPRESSED** avec l'interface **IStream** . Pour plus d'informations, voir [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) et **PR_RTF_COMPRESSED**.
    
7. Analysez le flux, en recherchant l'espace réservé `\objattph`de rendu,. Le caractère qui suit cet espace réservé est l'emplacement de la pièce jointe suivante dans le tableau trié.
    

