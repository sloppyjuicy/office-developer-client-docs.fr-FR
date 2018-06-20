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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: a913f2f3a72a365ec7d5078eccf31c4212ca83a5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784468"
---
# <a name="itabledatahrgetview"></a>ITableData::HrGetView

  
  
**S’applique à**: Outlook 
  
Crée un affichage tableau, qui retourne un pointeur vers une implémentation [IMAPITable](imapitableiunknown.md) . 
  
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
  
> [in] Pointeur vers une structure d’ordre de tri qui décrit l’ordre de tri pour l’affichage tableau. Si NULL est indiqué dans le paramètre _lpSSortOrderSet_ , l’affichage n’est pas trié. 
    
 _lpfCallerRelease_
  
> [in] Pointeur vers une fonction de rappel selon le prototype [CALLERRELEASE](callerrelease.md) que les appels MAPI lorsqu’il le libère l’affichage. Si NULL est indiqué dans le paramètre _lpfCallerRelease_ , aucune fonction n’est appelée sur la version de la vue. 
    
 _ulCallerData_
  
> [in] Les données qui doivent être enregistrées avec la nouvelle vue et transmises à la fonction de rappel désignée par _lpfCallerRelease_.
    
 _lppMAPITable_
  
> [out] Pointeur vers un pointeur vers la vue nouvellement créée.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’affichage a été créé avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **ITableData::HrGetView** crée un affichage en lecture seule des données dans le tableau, trié dans l’ordre indiqué par le paramètre _lpSSortOrderSet_ . Le curseur est placé au début de la première ligne dans l’affichage. Une implémentation d’interface **IMAPITable** pour accéder à la vue est renvoyée. 
  
Fournisseurs de services d’appel **HrGetView** lorsqu’ils souhaitent accorder un accès au client à un tableau. **HrGetView** crée l’affichage et retourne le pointeur **IMAPITable** . Fournisseurs de services de passer à son tour le pointeur sur le client. Lorsque le client a terminé à l’aide de la table et appelle la méthode [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) , **HrGetView** appelle la fonction de rappel vers laquelle pointée le paramètre _lpfCallerRelease_ . 
  
Si un fournisseur de services doit renvoyer à un client une vue possédant une colonne personnalisée définie ou une restriction, le fournisseur peut appeler les méthodes la vue [IMAPITable::SetColumns](imapitable-setcolumns.md) et [IMAPITable](imapitable-restrict.md) avant d’autoriser l’accès au client. 
  
## <a name="see-also"></a>Voir aussi



[CALLERRELEASE](callerrelease.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[SSortOrderSet](ssortorderset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

