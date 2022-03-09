---
title: ITableDataHrGetView
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITableData.HrGetView
api_type:
- COM
ms.assetid: 0e2a47be-497b-4031-87ce-60b2635e25f7
ms.openlocfilehash: af4807e625caaed110c8b000fde1a952ec93398f
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63381151"
---
# <a name="itabledatahrgetview"></a>ITableData::HrGetView

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une vue de tableau, renvoyant un pointeur vers une [implémentation IMAPITable](imapitableiunknown.md) . 
  
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
  
> [in] Pointeur vers une structure d’ordre de tri qui décrit l’ordre de tri pour l’affichage Tableau. Si NULL est transmis dans le _paramètre lpSSortOrderSet_ , l’affichage n’est pas trié. 
    
 _lpfCallerRelease_
  
> [in] Pointeur vers une fonction de rappel basée sur le prototype [CALLERRELEASE](callerrelease.md) que MAPI appelle lorsqu’il libère l’affichage. Si NULL est transmis dans le _paramètre lpfCallerRelease_ , aucune fonction n’est appelée lors de la publication de l’affichage. 
    
 _ulCallerData_
  
> [in] Données devant être enregistrées avec la nouvelle vue et transmises à la fonction de rappel pointée par  _lpfCallerRelease_.
    
 _lppMAPITable_
  
> [out] Pointeur vers un pointeur vers la vue nouvellement créée.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’affichage a été créé avec succès.
    
## <a name="remarks"></a>Remarques

La **méthode ITableData::HrGetView** crée une vue en lecture seule des données de la table, triées dans l’ordre indiqué par le paramètre  _lpSSortOrderSet_ . Le curseur est placé au début de la première ligne de l’affichage. Une **implémentation d’interface IMAPITable** pour accéder à l’affichage est renvoyée. 
  
Les fournisseurs de services **appellent HrGetView** lorsqu’ils ont besoin d’accorder à un client l’accès à une table. **HrGetView crée** l’affichage et renvoie le **pointeur IMAPITable** . À leur tour, les fournisseurs de services passent le pointeur au client. Lorsque le client a terminé d’utiliser la table et appelle sa méthode [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) , **HrGetView** appelle la fonction de rappel pointée par le paramètre  _lpfCallerRelease_ . 
  
Si un fournisseur de services doit revenir à un client avec un ensemble de colonnes personnalisé ou une restriction, il peut appeler les méthodes [IMAPITable::SetColumns](imapitable-setcolumns.md) et [IMAPITable::Restrict](imapitable-restrict.md) de l’affichage avant d’autoriser l’accès au client. 
  
## <a name="see-also"></a>Voir aussi



[CALLERRELEASE](callerrelease.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[SSortOrderSet](ssortorderset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

