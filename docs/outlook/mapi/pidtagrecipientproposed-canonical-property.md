---
title: Propriété canonique PidTagRecipientProposed
description: Décrit la propriété canonique PidTagRecipientProposed, qui indique si un participant à la réunion a répondu.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRecipientProposed
api_type:
- COM
ms.assetid: 8cb0e46c-0937-482f-be78-1f2e5261b210
ms.openlocfilehash: 7ec546542c62efa85b87446778b9371753a49883
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752728"
---
# <a name="pidtagrecipientproposed-canonical-property"></a>Propriété canonique PidTagRecipientProposed

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique si un participant à la réunion a répondu.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RECIPIENT_PROPOSED  <br/> |
|Identificateur :  <br/> |0x5FE1  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Destinataire du transport  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur TRUE pour cette propriété indique que le participant a proposé une nouvelle date et/ou heure. La valeur FALSE ou l’absence de cette propriété signifie que le participant n’a pas encore répondu ou que la réponse la plus récente du participant n’a pas inclus de nouvelle proposition de date/heure. Cette valeur ne doit pas être TRUE pour les participants d’une série périodique.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
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

