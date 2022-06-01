---
title: Propriété canonique PidTagAttachTransportName
description: Décrit la propriété canonique PidTagAttachTransportName, qui contient le nom d’un fichier pièce jointe modifié afin qu’il puisse être associé aux messages TNEF.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachTransportName
api_type:
- HeaderDef
ms.assetid: 701fca52-0f96-4019-80cd-c0ccd059ff9b
ms.openlocfilehash: c5ebdaf2d5155b271ab7eb829cab4dcbeeac59b3
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812494"
---
# <a name="pidtagattachtransportname-canonical-property"></a>Propriété canonique PidTagAttachTransportName

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom d’un fichier pièce jointe modifié afin qu’il puisse être associé aux messages TNEF. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W  <br/> |
|Identificateur :  <br/> |0x370C  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

TNEF et le fournisseur de transport utilisent ces propriétés. Elles ne sont généralement pas disponibles pour les applications clientes. 
  
Ces propriétés sont couramment utilisées par TNEF lorsque le système de messagerie sous-jacent ne prend pas en charge les noms de fichiers fournis. Par exemple, ils sont utilisés lorsque l’utilisateur attache plusieurs fichiers portant le même nom, tels que cinq fichiers nommés CONFIG.SYS. Le fournisseur de transport doit modifier les noms pour s’assurer qu’ils sont uniques. Chaque nom modifié apparaît dans le **PR_ATTACH_TRANSPORT_NAME** de sa pièce jointe et les propriétés associées. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

