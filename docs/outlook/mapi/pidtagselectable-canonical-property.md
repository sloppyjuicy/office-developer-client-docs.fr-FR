---
title: Propriété canonique PidTagSelectable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSelectable
api_type:
- COM
ms.assetid: eeecd957-dd50-4849-9698-8bc7106301e9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 17343a721cbcc642c8cffe95112f25710c0c130c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383456"
---
# <a name="pidtagselectable-canonical-property"></a>Propriété canonique PidTagSelectable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur TRUE si l’entrée dans la table unique peut être sélectionnée. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SELECTABLE  <br/> |
|Identificateur :  <br/> |0x3609  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Conteneur de carnet d’adresses  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée principalement pour la mise en forme visuelle d’une table unique. Les modèles peuvent être regroupés en créant une entrée qui indique le titre pour le groupe. Définir cette propriété sur FALSE pour l’en-tête garantit que l’utilisateur peut sélectionner uniquement les modèles réelles dans le groupe et pas cette entrée de titre. 
  
Cette propriété s’applique uniquement à une table unique, pas à une table de hiérarchie de livre adresse. 
  
MAPI permet à un fournisseur de carnet d’adresses pour regrouper les éléments visuellement de deux manières. Tout d’abord, certaines lignes peuvent fonctionner comme en-têtes en étant non sélectionnable. Deuxièmement, les éléments sélectionnables peuvent être mis en retrait par rapport à leurs en-têtes à l’aide de la propriété **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)). Cette propriété est utilisée dans ce regroupement pour indiquer si cet élément peut être sélectionné dans une liste pour créer une adresse unique. Par exemple, si un client a plusieurs modèles pour la création des adresses de télécopie, il peut afficher les comme suit : 
  
Modèles de télécopies (profondeur 0, pas sélectionnable)
  
 Local (profondeur 1, sélectionnable) 
  
 Appel longue distance (profondeur 1, sélectionnable) 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les modèles de carnet d’adresses.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[IABLogon::GetOneOffTable](iablogon-getoneofftable.md)
  
[Propriété canonique PidTagFolderType](pidtagfoldertype-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

