---
title: ITableDataHrGetView
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrGetView
api_type:
- COM
ms.assetid: 0e2a47be-497b-4031-87ce-60b2635e25f7
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 375a0f1d39b09b7ad453120f20752e00ffda0e15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278714"
---
# <a name="itabledatahrgetview"></a>ITableData::HrGetView

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un affichage tableau en renvoyant un pointeur vers une implémentation [IMAPITable](imapitableiunknown.md) . 
  
```cpp
HRESULT HrGetView(
  LPSSortOrderSet lpSSortOrderSet,
  CALLERRELEASE FAR * lpfCallerRelease,
  ULONG_PTR ulCallerData,
  LPMAPITABLE FAR * lppMAPITable
);
```

## <a name="parameters"></a>Paramètres

 _lpSSortOrderSet_
  
> dans Pointeur vers une structure d'ordre de tri qui décrit l'ordre de tri de la vue de table. Si NULL est transmis dans le paramètre _lpSSortOrderSet_ , la vue n'est pas triée. 
    
 _lpfCallerRelease_
  
> dans Pointeur vers une fonction de rappel basée sur le prototype [CALLERRELEASE](callerrelease.md) que MAPI appelle lorsqu'il libère la vue. Si NULL est passé dans le paramètre _lpfCallerRelease_ , aucune fonction n'est appelée sur la version de la vue. 
    
 _ulCallerData_
  
> dans Les données qui doivent être enregistrées avec la nouvelle vue et transmises à la fonction de rappel pointée par _lpfCallerRelease_.
    
 _lppMAPITable_
  
> remarquer Pointeur vers un pointeur vers l'affichage nouvellement créé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'affichage a été créé avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **ITableData:: HrGetView** crée une vue en lecture seule des données de la table, triée dans l'ordre dans lequel le paramètre _lpSSortOrderSet_ . Le curseur est placé au début de la première ligne de la vue. Une implémentation d'interface **IMAPITable** pour accéder à la vue est retournée. 
  
Les fournisseurs de services appellent **HrGetView** lorsqu'ils doivent accorder à un client l'accès à une table. **HrGetView** crée l'affichage et renvoie le pointeur **IMAPITable** . Les fournisseurs de services passent à leur tour le pointeur sur le client. Une fois que le client a terminé d'utiliser la table et appelle sa méthode [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) , **HrGetView** appelle la fonction de rappel pointée par le paramètre _lpfCallerRelease_ . 
  
Si un fournisseur de services doit retourner à un client une vue avec un jeu de colonnes personnalisé ou une restriction, le fournisseur peut appeler les méthodes [IMAPITable:: SetColumns](imapitable-setcolumns.md) et [IMAPITable:: Restrict](imapitable-restrict.md) avant d'autoriser l'accès au client. 
  
## <a name="see-also"></a>Voir aussi



[CALLERRELEASE](callerrelease.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[SSortOrderSet](ssortorderset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

