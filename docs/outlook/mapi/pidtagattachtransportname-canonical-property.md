---
title: Propriété canonique PidTagAttachTransportName
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 90b09870e137631825c3b6c02322d5bf745780cd
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64454921"
---
# <a name="pidtagattachtransportname-canonical-property"></a>Propriété canonique PidTagAttachTransportName

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom d’un fichier de pièce jointe modifié afin qu’il puisse être associé à des messages TNEF. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W  <br/> |
|Identificateur :  <br/> |0x370C  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Le TNEF et le fournisseur de transport utilisent ces propriétés. Elles ne sont généralement pas disponibles pour les applications clientes. 
  
Ces propriétés sont couramment utilisées par TNEF lorsque le système de messagerie sous-jacent ne prend pas en charge les noms de fichiers fournis. Par exemple, ils sont utilisés lorsque l’utilisateur joint plusieurs fichiers portant le même nom, tels que cinq fichiers nommés CONFIG.SYS. Le fournisseur de transport doit modifier les noms pour s’assurer qu’ils sont uniques. Chaque nom modifié apparaît dans le nom de la pièce jointe et **PR_ATTACH_TRANSPORT_NAME** propriétés associées. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

