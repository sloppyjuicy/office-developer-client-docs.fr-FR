---
title: Propriété canonique PidTagSensitivity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagSensitivity
api_type:
- COM
ms.assetid: 5b678475-f2a8-4831-ad68-11654e09c821
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7b1de5f524a62c1684c8554a537827b80cabb205
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613337"
---
# <a name="pidtagsensitivity-canonical-property"></a>Propriété canonique PidTagSensitivity

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur qui indique l’avis de l’expéditeur du message sur la sensibilité d’un message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SENSITIVITY  <br/> |
|Identificateur :  <br/> |0x0036  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Il est recommandé que les objets de message exposent cette propriété.
  
Cette propriété peut avoir exactement l’une des valeurs suivantes :
  
SENSITIVITY_NONE 
  
> Le message n’a pas de sensibilité particulière.
    
SENSITIVITY_PERSONAL 
  
> Le message est personnel.
    
SENSITIVITY_PRIVATE 
  
> Le message est privé.
    
SENSITIVITY_COMPANY_CONFIDENTIAL 
  
> Le message est désigné comme confidentiel de l’entreprise.
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et pièce jointe.
    
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

