---
title: PpropFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PpropFindProp
api_type:
- HeaderDef
ms.assetid: f23dd6f4-915b-4fe8-ab3f-6d625c7d6061
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f720160193613bbbb4bbd447f78c14e6e5378eb8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565654"
---
# <a name="ppropfindprop"></a>PpropFindProp

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Recherche une propriété spécifiée dans une propriété définie.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Paramètres

 _rgprop_
  
> [in] Tableau de structures [SPropValue](spropvalue.md) qui définissent les propriétés à rechercher. 
    
 _cprop_
  
> [in] Nombre de propriétés dans le jeu de propriétés indiqué par le paramètre _rgprop_ . 
    
 _ulPropTag_
  
> [in] Balise de propriété pour la propriété à rechercher dans le jeu de propriétés indiqué par le paramètre _rgprop_ . 
    
## <a name="return-value"></a>Valeur renvoy�e

 **PpropFindProp** renvoie une structure [SPropValue](spropvalue.md) définissant la propriété qui correspond à la balise de propriété d’entrée, ou NULL si aucune correspondance n’existe. 
  
## <a name="remarks"></a>Remarques

Si la balise de propriété donnée indique une propriété de type PT_UNSPECIFIED, la fonction **PpropFindProp** trouve une correspondance uniquement pour l’identificateur de propriété dans la balise. Dans le cas contraire, elle trouve une correspondance pour la balise de propriété entière, y compris le type de propriété et renvoie la propriété identifiée. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::BuildDataItem  <br/> |MFCMAPI utilise la méthode **PpropFindProp** pour rechercher des propriétés dans une propriété définie en cours d’ajout à la liste.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

