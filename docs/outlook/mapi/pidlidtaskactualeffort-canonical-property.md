---
title: Propriété canonique PidLidTaskActualEffort
description: Décrit la propriété canonique PidLidTaskActualEffort, qui indique le nombre de minutes pendant lesquelles l’utilisateur a effectué une tâche.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTaskActualEffort
api_type:
- COM
ms.assetid: 8e9a9432-bf50-4333-82ec-fba19dff8006
ms.openlocfilehash: cdc1dcebf305a9e3b9bda7fe777f95b48c1069c4
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817409"
---
# <a name="pidlidtaskactualeffort-canonical-property"></a>Propriété canonique PidLidTaskActualEffort

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique le nombre de minutes pendant lesquelles l’utilisateur a effectué une tâche.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskActualEffort  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Task  <br/> |
|ID long (LID) :  <br/> |0x00008110  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Tâche  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur doit être supérieure ou égale à 0 et inférieure à 0x5AE980DF (1 525 252 319), où 480 minutes correspondent à un jour et 2 400 minutes à une semaine (huit heures par jour de travail et cinq jours par semaine).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations autorisées pour les objets de liste de distribution de contacts et personnels.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

