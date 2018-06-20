---
title: Propriété canonique PidTagAttachTransportName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTransportName
api_type:
- HeaderDef
ms.assetid: 701fca52-0f96-4019-80cd-c0ccd059ff9b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6828a6436946de27020fa1177223955e07a08faf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785753"
---
# <a name="pidtagattachtransportname-canonical-property"></a>Propriété canonique PidTagAttachTransportName

  
  
**S’applique à**: Outlook 
  
Contient le nom d’un fichier de pièce jointe modifié de sorte qu’il peut être associé à des messages TNEF. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W  <br/> |
|Identificateur :  <br/> |0x370C  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Zone :  <br/> |Pièce jointe du message  <br/> |
   
## <a name="remarks"></a>Remarques

TNEF et le fournisseur de transport utilisent ces propriétés. Ils ne sont généralement pas disponibles pour les applications clientes. 
  
Ces propriétés sont couramment utilisées par TNEF lorsque le système de messagerie sous-jacent ne prend pas en charge les noms de fichier fourni. Par exemple, ils sont utilisés lorsque l’utilisateur attache plusieurs fichiers portant le même nom, tels que les cinq fichiers nommée CONFIG. SYS. Le fournisseur de transport doit modifier les noms pour vous assurer qu’ils sont uniques. Chaque nom modifié apparaît dans la pièce jointe **PR_ATTACH_TRANSPORT_NAME** et propriétés associées. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

