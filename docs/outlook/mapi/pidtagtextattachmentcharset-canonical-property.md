---
title: Propriété canonique PidTagTextAttachmentCharset
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTextAttachmentCharset
api_type:
- COM
ms.assetid: d347c949-d0c3-4a36-8447-3fa01111cdc1
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1db41bc5c7ea71d65d892da520d4258354eb53cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358813"
---
# <a name="pidtagtextattachmentcharset-canonical-property"></a>Propriété canonique PidTagTextAttachmentCharset

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur du jeu de caractères d'une pièce jointe de message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |Aucun  <br/> |
|Identificateur :  <br/> |0x371B  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Les données de cette propriété proviennent d'un champ d'en-tête MIME Content-type qui commence par «Text/», si un paramètre «charset» est présent.
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> ConVertit des conventions de messagerie standard Internet en objets message.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

