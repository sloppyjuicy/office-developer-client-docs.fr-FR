---
title: Propriété canonique PidTagRenderingPosition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRenderingPosition
api_type:
- COM
ms.assetid: bce46687-17dc-4a3f-96be-303d8755158e
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 649490f18bb1a14a7056b49fd846e893fba304bd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575209"
---
# <a name="pidtagrenderingposition-canonical-property"></a>Propriété canonique PidTagRenderingPosition

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un décalage, en caractères, à utiliser dans le rendu d’une pièce jointe dans le texte du message principal.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RENDERING_POSITION  <br/> |
|Identificateur :  <br/> |0x370B  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Pièce jointe MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque le décalage fourni est -1 (0xFFFFFFFF), la pièce jointe n’est pas restituée à l’aide de cette propriété. Toutes les valeurs autres que -1 indiquent la position dans la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) à laquelle la pièce jointe doit être affiché.
  
 **Remarque** Le caractère indiqué par cette propriété dans **PR_BODY** est remplacé par la pièce jointe. Ce caractère est généralement un espace, bien qu’un espace réservé spéciale caractère peut également être utilisé. 
  
Cette propriété est exprimée en caractères. Dans certains jeux de caractères, ce n’est pas équivalent à octets. Les applications Unicode peuvent calculer la position en fonction de caractères codés sur deux octets. Applications définir de caractères codés sur deux octets (DBCS) doivent analyser le texte jusqu'à la valeur de cette propriété, car la représentation sous forme de leur caractère varie entre 1 et 2 octets par caractère.
  
Cette propriété ne doit pas être utilisée avec le texte RTF (RICH Text Format). La position de rendu est indiquée au format RTF par une séquence d’échappement appelée l’espace réservé d’objet pièce jointe. Cette séquence se compose de la chaîne `\objattph` suivi d’un seul caractère, généralement un espace, qui sera remplacé par le rendu de la pièce jointe. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
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

