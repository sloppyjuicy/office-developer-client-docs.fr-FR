---
title: Propriété canonique PidLidTaskActualEffort
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskActualEffort
api_type:
- COM
ms.assetid: 8e9a9432-bf50-4333-82ec-fba19dff8006
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7eb51396f4575a8f8f9ce15aff84eb894773e979
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331170"
---
# <a name="pidlidtaskactualeffort-canonical-property"></a>Propriété canonique PidLidTaskActualEffort

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique le nombre de minutes pendant lesquelles l'utilisateur a effectué une tâche.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskActualEffort  <br/> |
|Jeu de propriétés:  <br/> |PSETID_Task  <br/> |
|ID long (couvercle):  <br/> |0x00008110  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Tâche  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur doit être supérieure ou égale à 0 et inférieure à 0x5AE980DF (1 525 252 319), où 480 minutes correspondent à un jour et 2400 minutes à une semaine (huit heures dans un jour de travail et cinq jours dans une semaine de travail).
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets de liste de distribution personnelle et de contact.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

