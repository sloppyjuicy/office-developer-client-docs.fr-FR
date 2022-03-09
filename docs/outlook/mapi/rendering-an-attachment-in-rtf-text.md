---
title: Rendu d’une pièce jointe dans du texte RTF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
ms.openlocfilehash: 8d7cb94259d8636a61b106062dfcde8333ff48ec
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63373892"
---
# <a name="rendering-an-attachment-in-rtf-text"></a>Rendu d’une pièce jointe dans du texte RTF

**S’applique à** : Outlook 2013 | Outlook 2016
  
Les clients au format RTF (Rich Text Format) peuvent récupérer les informations de position de rendu à partir du texte du message RTF en cherchant la séquence d’échappatoire suivante dans la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) du message :
  
 `\objattph`
  
 **Pour localiser les informations de rendu dans du texte formaté**
  
1. **Appelez IMessage::GetAttachmentTable** pour accéder à la table des pièces jointes du message. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).

2. Créez une restriction de propriété qui limite le tableau aux lignes **PR_RENDERING_POSITION n’est** pas égale à -1. Pour plus d’informations, **voir PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).

3. Appelez **IMAPITable::Restrict** pour appliquer la restriction. Pour plus d’informations, [voir IMAPITable::Restrict](imapitable-restrict.md).

4. **Appelez IMAPITable::SortTable** pour trier les pièces jointes. Pour plus d’informations, [voir IMAPITable::SortTable](imapitable-sorttable.md).

5. **Appelez IMAPITable::QueryRows pour** récupérer les lignes appropriées. Pour plus d’informations, [voir IMAPITable::QueryRows](imapitable-queryrows.md).

6. Appelez la méthode **IMAPIProp::OpenProperty** du message pour récupérer **PR_RTF_COMPRESSED’interface** **IStream** . Pour plus d’informations, [voir IMAPIProp::OpenProperty](imapiprop-openproperty.md) et **PR_RTF_COMPRESSED**.

7. Analysez le flux, à la recherche de l’espace réservé de rendu, `\objattph`. Le caractère qui suit cet espace réservé est l’endroit où se trouve la pièce jointe suivante dans le tableau trié.
