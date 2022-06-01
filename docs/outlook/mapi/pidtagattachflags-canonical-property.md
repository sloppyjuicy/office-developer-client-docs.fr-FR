---
title: Propriété canonique PidTagAttachFlags
description: Décrit la propriété canonique PidTagAttachFlags, qui contient un masque de bits d’indicateurs pour une pièce jointe.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachFlags
api_type:
- HeaderDef
ms.assetid: 47e01131-f399-43cb-9815-aba69638c3fb
ms.openlocfilehash: 6230c645fbce6aa8318fdc94af22def8dc3cac25
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812487"
---
# <a name="pidtagattachflags-canonical-property"></a>Propriété canonique PidTagAttachFlags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un masque de bits d’indicateurs pour une pièce jointe. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_FLAGS  <br/> |
|Identificateur :  <br/> |0x3714  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée pour la prise en charge de MHTML. 
  
Un ou plusieurs des indicateurs suivants peuvent être définis pour le **masque** de bits PR_ATTACH_FLAGS : 
  
ATT_INVISIBLE_IN_HTML 
  
> Indique que cette pièce jointe n’est pas disponible pour les applications de rendu HTML et doit être ignorée dans le traitement miME (Multipurpose Internet Mail Extensions). 
    
ATT_INVISIBLE_IN_RTF 
  
> Indique que cette pièce jointe n’est pas disponible pour le rendu des applications au format RTF (Rich Text Format) et doit être ignorée par MAPI.
    
Si la propriété **PR_ATTACH_FLAGS** est zéro ou absente, la pièce jointe doit être traitée par toutes les applications. 
  
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

