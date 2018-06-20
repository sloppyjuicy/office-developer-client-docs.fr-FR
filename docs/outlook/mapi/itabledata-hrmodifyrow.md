---
title: ITableDataHrModifyRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrModifyRow
api_type:
- COM
ms.assetid: 9e255b3e-dd17-4528-ba4e-c3a1aef32b04
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: a1388545597cf0000f270bf693c93f9349fb6426
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784485"
---
# <a name="itabledatahrmodifyrow"></a>ITableData::HrModifyRow

  
  
**S’applique à**: Outlook 
  
Insérer une nouvelle ligne de tableau, en remplaçant éventuellement une ligne existante.
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a>Paramètres

 _lpSRow_
  
> [in] Pointeur vers une structure [SRow](srow.md) qui décrit la ligne à ajouter ou pour remplacer une ligne existante. Une des structures de valeur de propriété vers laquelle pointés le membre **lpProps** de la structure **SRow** doit contenir la colonne d’index, la même valeur que celle qui a été spécifiée dans le paramètre _ulPropTagIndexColumn_ dans l’appel à la [Create table ](createtable.md)fonction. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La ligne a été correctement insérée ou modifiée.
    
MAPI_E_INVALID_PARAMETER 
  
> La ligne dans le passé ne dispose pas d’une colonne d’index.
    
## <a name="remarks"></a>Remarques

La méthode **ITableData::HrModifyRow** insère la ligne décrite par la structure **SRow** désignée par le paramètre _lpSRow_ . Si une ligne qui possède la même valeur pour la colonne d’index en tant que la ligne qui pointe _lpSRow_ existe déjà dans le tableau, la ligne existante est remplacée. Si aucune ligne n’existe qui correspond à celui qui est inclus dans la structure **SRow** , **HrModifyRow** ajoute la ligne à la fin de la table. 
  
Toutes les vues de la table sont modifiées pour inclure la ligne désignée par _lpSRow_. Toutefois, si un affichage a une restriction en place qui exclut de la ligne, il peut être pas visible à l’utilisateur. 
  
Les colonnes de la ligne désignés par _lpSRow_ n’ont pas à inclure dans le même ordre que les colonnes de la table. L’appelant peut également inclure en tant que propriétés de colonnes qui ne sont pas actuellement dans le tableau. Pour des vues existantes, **HrModifyRow** rend ces nouvelles colonnes disponibles, mais n’inclut pas les dans la colonne en cours. Pour les affichages futures, **HrModifyRow** inclut les nouvelles colonnes dans la colonne. 
  
Une fois que **HrModifyRow** ajoute la ligne, les notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode la table [IMAPITable::Advise](imapitable-advise.md) pour inscrire les notifications. 
  
## <a name="see-also"></a>Voir aussi



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

