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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 44ecf095ad24dd266dc5f603ace9c7b9f21c1b41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348663"
---
# <a name="itabledatahrmodifyrow"></a>ITableData::HrModifyRow

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Insère une nouvelle ligne de tableau, éventuellement en remplaçant une ligne existante.
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a>Paramètres

 _lpSRow_
  
> dans Pointeur vers une structure [SRow](srow.md) qui décrit la ligne à ajouter ou pour remplacer une ligne existante. L'une des structures de valeurs de propriété vers lesquelles pointe le membre **lpProps** de la structure **SRow** doit contenir la colonne d'index, la valeur qui a été spécifiée dans le paramètre _ulPropTagIndexColumn_ dans l'appel à la [CreateTable ](createtable.md)fonction. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La ligne a été insérée ou modifiée.
    
MAPI_E_INVALID_PARAMETER 
  
> La ligne passée ne possède pas de colonne d'index.
    
## <a name="remarks"></a>Remarques

La méthode **ITableData:: HrModifyRow** insère la ligne décrite par la structure **SRow** vers laquelle pointe le paramètre _lpSRow_ . Si une ligne qui a la même valeur pour sa colonne d'index que la ligne sur laquelle pointe _lpSRow_ existe déjà dans le tableau, la ligne existante est remplacée. S'il n'existe aucune ligne correspondant à celle incluse dans la structure **SRow** , **HrModifyRow** ajoute la ligne à la fin du tableau. 
  
Toutes les vues de la table sont modifiées de façon à inclure la ligne sur laquelle pointe _lpSRow_. Toutefois, si une vue a une restriction en place qui exclut la ligne, elle peut ne pas être visible par l'utilisateur. 
  
Les colonnes de la ligne sur lesquelles pointe _lpSRow_ n'ont pas besoin d'être dans le même ordre que les colonnes du tableau. L'appelant peut également inclure en tant que propriétés de colonnes qui ne se trouvent pas actuellement dans le tableau. Pour les affichages existants, **HrModifyRow** rend ces nouvelles colonnes disponibles, mais ne les inclut pas dans le jeu de colonnes actuel. Pour les futures vues, **HrModifyRow** inclut les nouvelles colonnes dans l'ensemble de colonnes. 
  
Une fois que **HrModifyRow** a ajouté la ligne, des notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode [IMAPITable:: Advise](imapitable-advise.md) pour s'inscrire aux notifications. 
  
## <a name="see-also"></a>Voir aussi



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

