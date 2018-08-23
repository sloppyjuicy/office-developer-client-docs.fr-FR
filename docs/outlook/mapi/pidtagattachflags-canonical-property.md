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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: bf92e62dc572a81b6e0aab4cb1b0fc8afe97800d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573095"
---
# <a name="pidtagattachflags-canonical-property"></a>Propriété canonique PidTagAttachFlags

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un masque binaire composé des indicateurs d’une pièce jointe. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_FLAGS  <br/> |
|Identificateur :  <br/> |0x3714  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée pour la prise en charge MHTML. 
  
Un ou plusieurs des indicateurs suivants peuvent être définies pour le masque de bits **PR_ATTACH_FLAGS** : 
  
ATT_INVISIBLE_IN_HTML 
  
> Indique que cette pièce jointe n’est pas disponible pour les applications de rendu HTML et doit être ignorée dans Multipurpose Internet Mail Extensions (MIME) de traitement. 
    
ATT_INVISIBLE_IN_RTF 
  
> Indique que cette pièce jointe n’est pas disponible pour les applications rendu au format RTF (RICH Text Format) et doit être ignorée par MAPI.
    
Si la propriété **PR_ATTACH_FLAGS** est égale à zéro ou absent, la pièce jointe doit être traité par toutes les applications. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

