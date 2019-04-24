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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 17343a721cbcc642c8cffe95112f25710c0c130c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359016"
---
# <a name="pidtagselectable-canonical-property"></a>Propriété canonique PidTagSelectable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur TRUE si l'entrée dans la table ponctuelle peut être sélectionnée. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SELECTABLE  <br/> |
|Identificateur :  <br/> |0x3609  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Conteneur de carnet d'adresses  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est principalement utilisée pour la mise en forme visuelle d'une table ponctuelle. Les modèles peuvent être regroupés en créant une entrée qui indique l'en-tête du groupe. La définition de cette propriété sur FALSe pour l'en-tête garantit que l'utilisateur peut sélectionner uniquement les modèles réels dans le groupe et non cette entrée d'en-tête. 
  
Cette propriété s'applique uniquement à une table ponctuelle, et non à une table de hiérarchie de carnets d'adresses. 
  
MAPI permet à un fournisseur de carnets d'adresses de regrouper les éléments visuellement de deux manières. Tout d'abord, certaines lignes peuvent fonctionner comme des en-têtes en étant désélectionnées. Deuxièmement, les éléments sélectionnables peuvent être mis en retrait par rapport à leurs en-têtes à l'aide de la propriété **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)). Cette propriété est utilisée dans ce regroupement pour indiquer si cet élément peut être sélectionné ou non dans une liste pour créer une adresse ponctuelle. Par exemple, si un client dispose de plusieurs modèles pour créer des adresses de télécopie, il peut les afficher comme suit: 
  
Modèles de télécopie (profondeur 0, non sélectionnable)
  
 Local (profondeur 1, sélectionnable) 
  
 Longue distance (profondeur 1, sélectionnable) 
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations autorisées pour les modèles de carnet d'adresses.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés indiquées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[IABLogon::GetOneOffTable](iablogon-getoneofftable.md)
  
[Propriété canonique PidTagFolderType](pidtagfoldertype-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

