---
title: Propriété canonique PidTagInitialDetailsPane
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInitialDetailsPane
api_type:
- HeaderDef
ms.assetid: c4712133-6fbd-4c50-a258-5f4317120476
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0ea7d0a17fdb6dba047cb97290d991ce384d4750
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573935"
---
# <a name="pidtaginitialdetailspane-canonical-property"></a>Propriété canonique PidTagInitialDetailsPane

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Indique la page d’un modèle d’affichage pour afficher le premier.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_INITIAL_DETAILS_PANE  <br/> |
|Identificateur :  <br/> |0x3F08  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Afficher des Tables MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Il doit être présent sur tous les objets de carnet d’adresses sur un serveur du Service fournisseur Interface NSPI (Name) et doit avoir la valeur zéro (0). Il ne doit pas être défini pour tous les objets dans un carnet d’adresses en mode hors connexion.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

