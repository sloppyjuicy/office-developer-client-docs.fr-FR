---
title: Propriété canonique PidTagTextAttachmentCharset
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagTextAttachmentCharset
api_type:
- COM
ms.assetid: d347c949-d0c3-4a36-8447-3fa01111cdc1
description: Contient la valeur du jeu de caractères d’une pièce jointe de message. Les données de cette propriété sont dérivées d’un champ d’en-tête MIME content-type qui commence par « text/ ».
ms.openlocfilehash: d4193ac2e662219b27f19c5854ee9e448ea067bd
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64456328"
---
# <a name="pidtagtextattachmentcharset-canonical-property"></a>Propriété canonique PidTagTextAttachmentCharset

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur du jeu de caractères d’une pièce jointe de message.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |Aucun  <br/> |
|Identificateur :  <br/> |0x371B  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Les données de cette propriété sont dérivées d’un champ d’en-tête MIME content-type qui commence par « text/ », si un paramètre « charset » est présent.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions de messagerie standard Internet en objets de message.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

