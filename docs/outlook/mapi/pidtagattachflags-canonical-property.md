---
title: Propriété canonique PidTagAttachFlags
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 222780d2bd02b969304e9104631c89cd53ad28d8
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455152"
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

Cette propriété est utilisée pour la prise en charge MHTML. 
  
Un ou plusieurs des indicateurs suivants peuvent être définies pour **PR_ATTACH_FLAGS masque de** bits : 
  
ATT_INVISIBLE_IN_HTML 
  
> Indique que cette pièce jointe n’est pas disponible pour les applications de rendu HTML et qu’elle doit être ignorée dans le traitement MIME (Multipurpose Internet Mail Extensions). 
    
ATT_INVISIBLE_IN_RTF 
  
> Indique que cette pièce jointe n’est pas disponible pour les applications de rendu au format RTF (Rich Text Format) et qu’elle doit être ignorée par MAPI.
    
Si la **PR_ATTACH_FLAGS** est zéro ou absente, la pièce jointe doit être traitée par toutes les applications. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
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

