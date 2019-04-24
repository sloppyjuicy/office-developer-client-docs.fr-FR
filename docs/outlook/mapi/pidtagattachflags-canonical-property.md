---
title: Propriété canonique PidTagAttachFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachFlags
api_type:
- HeaderDef
ms.assetid: 47e01131-f399-43cb-9815-aba69638c3fb
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: efccd75cce04e4e392a7fbd9feecc7c8b49ab57e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339332"
---
# <a name="pidtagattachflags-canonical-property"></a>Propriété canonique PidTagAttachFlags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un masque de masque des indicateurs d'une pièce jointe. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_FLAGS  <br/> |
|Identificateur :  <br/> |0x3714  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée pour la prise en charge de MHTML. 
  
Un ou plusieurs des indicateurs suivants peuvent être définis pour le masque de masque **PR_ATTACH_FLAGS** : 
  
ATT_INVISIBLE_IN_HTML 
  
> Indique que cette pièce jointe n'est pas disponible pour les applications de rendu HTML et qu'elle doit être ignorée dans le traitement MIME (Multipurpose Internet Mail Extensions). 
    
ATT_INVISIBLE_IN_RTF 
  
> Indique que cette pièce jointe n'est pas disponible pour le rendu des applications au format RTF (Rich Text Format) et qu'elle doit être ignorée par MAPI.
    
Si la propriété **PR_ATTACH_FLAGS** est nulle ou absente, la pièce jointe doit être traitée par toutes les applications. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et Attachment.
    
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

