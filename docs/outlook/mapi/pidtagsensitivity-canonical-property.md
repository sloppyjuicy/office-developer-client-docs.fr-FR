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
description: Contient une valeur qui indique l’opinion de l’expéditeur du message sur la sensibilité d’un message pour Outlook 2013 ou Outlook 2016.
ms.openlocfilehash: 133dd0a5de1b11be2746b7cbed1bdb99fcb67f71
ms.sourcegitcommit: 06224e0d198beda57d2e6d76b34f8897afbfd84d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2022
ms.locfileid: "65132586"
---
# <a name="pidtagsensitivity-canonical-property"></a>Propriété canonique PidTagSensitivity

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur qui indique l’opinion de l’expéditeur du message sur la sensibilité d’un message.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SENSITIVITY  <br/> |
|Identificateur :  <br/> |0x0036  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Il est recommandé que les objets de message exposent cette propriété.
  
Les remarques de [SPropertyRestriction](spropertyrestriction.md) spécifient que les programmes MAPI doivent utiliser une SExistRestriction supplémentaire pour éviter les résultats non définis. Outlook (au moins 16.0.15028.20204 (v2203)) ne parvient pas à suivre ces instructions mêmes lorsqu’elle récupère la table de contenu d’un dossier. Par conséquent, Outlook affiche des résultats non définis lorsqu’un objet message ne dispose pas de la propriété PR_SENSITIVITY.
  
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
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
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

