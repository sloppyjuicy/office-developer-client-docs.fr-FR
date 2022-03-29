---
title: Propriété canonique PidTagSelectable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagSelectable
api_type:
- COM
ms.assetid: eeecd957-dd50-4849-9698-8bc7106301e9
description: Contient TRUE si l’entrée du tableau one-off peut être sélectionnée. Cette propriété est principalement utilisée pour la mise en forme visuelle d’un tableau one-off.
ms.openlocfilehash: e6c3a4049e65b4ce20450d752ff1f11f284600d6
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455593"
---
# <a name="pidtagselectable-canonical-property"></a>Propriété canonique PidTagSelectable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient TRUE si l’entrée du tableau one-off peut être sélectionnée. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SELECTABLE  <br/> |
|Identificateur :  <br/> |0x3609  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Conteneur de carnet d’adresses  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est principalement utilisée pour la mise en forme visuelle d’un tableau one-off. Les modèles peuvent être regroupés en créant une entrée qui indique le titre du groupe. La définition de cette propriété sur FALSE pour le titre garantit que l’utilisateur peut sélectionner uniquement les modèles réels du groupe et non cette entrée de titre. 
  
Cette propriété s’applique uniquement à une table unique, et non à une table de hiérarchie de carnet d’adresses. 
  
MAPI permet à un fournisseur de carnet d’adresses de grouper visuellement les éléments par deux moyens. Tout d’abord, certaines lignes peuvent fonctionner en tant qu’en-tête en étant désélectionnables. Ensuite, les éléments sélectionnables peuvent être en retrait par rapport à leurs titres à l’aide de la propriété **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)). Cette propriété est utilisée dans ce regroupement pour indiquer si cet élément peut être sélectionné dans une liste pour créer une adresse unique. Par exemple, si un client possède plusieurs modèles de création d’adresses de télécopie, il peut les afficher comme suit : 
  
Modèles FAX (profondeur 0, sélectionnable)
  
 Local (profondeur 1, sélectionnable) 
  
 Longue distance (profondeur 1, sélectionnable) 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées pour les modèles de carnet d’adresses.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[IABLogon::GetOneOffTable](iablogon-getoneofftable.md)
  
[Propriété canonique PidTagFolderType](pidtagfoldertype-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

