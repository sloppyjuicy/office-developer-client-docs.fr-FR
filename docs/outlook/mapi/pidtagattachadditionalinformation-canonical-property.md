---
title: Propriété canonique PidTagAttachAdditionalInformation
description: Décrit la propriété canonique PidTagAttachAdditionalInformation, qui fournit des informations de type de fichier pour une pièce jointe non Windows.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachAdditionalInformation
api_type:
- HeaderDef
ms.assetid: 75f092f2-ee3f-45c2-a46f-e1dff2e22b2e
ms.openlocfilehash: ba3fce31eea5d3396a86f65175fdf64f1d4d8dd7
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817794"
---
# <a name="pidtagattachadditionalinformation-canonical-property"></a>Propriété canonique PidTagAttachAdditionalInformation

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit des informations de type de fichier pour une pièce jointe non Windows.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_ADDITIONAL_INFO  <br/> |
|Identificateur :  <br/> |0x370F  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété fournit des métadonnées sur une pièce jointe particulière en fonction de l’encodage de la pièce jointe. Par exemple, lorsque la propriété **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) contient MacBinary, **PR_ATTACH_ADDITIONAL_INFO** contient une chaîne qui représente le créateur et le type de fichier Macintosh, au format « :CREA:TYPE » pour le fichier Macintosh encodé. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

