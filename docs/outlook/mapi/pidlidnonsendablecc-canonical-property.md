---
title: Propriété canonique PidLidNonSendableCc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableCc
api_type:
- COM
ms.assetid: 170afe1f-1223-4689-825c-d21ab14b213b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d9f166b0d1e180fdb087fbf602e6841c3fdac3dc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395986"
---
# <a name="pidlidnonsendablecc-canonical-property"></a>Propriété canonique PidLidNonSendableCc

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une liste de tous les participants de rédaction qui sont également des participants facultatifs.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidNonSendableCC  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID de type long (capot) :  <br/> |0x00008537  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Réunions  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de chaque participant est la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de carnet d’adresses du participant. Des entrées doivent être séparées par un point-virgule suivi d’un espace. Cette propriété n’est pas requise.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

