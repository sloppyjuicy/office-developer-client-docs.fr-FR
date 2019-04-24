---
title: ITableDataHrNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrNotify
api_type:
- COM
ms.assetid: 98548b50-342e-434a-9ad3-c37ba418c5ce
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: aa2170bf4bedfb441ad4808f774f6f71d5caf85e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348635"
---
# <a name="itabledatahrnotify"></a>ITableData::HrNotify

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Envoie une notification pour une ligne de tableau.
  
```cpp
HRESULT HrNotify(
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _cValues_
  
> dans Nombre de valeurs de propriété dans la structure [SPropValue](spropvalue.md) vers laquelle pointe le paramètre _lpSPropValue_ . 
    
 _lpSPropValue_
  
> dans Pointeur vers une structure **SPropValue** qui décrit les valeurs des colonnes dans la ligne cible. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

La méthode **ITableData:: HrNotify** envoie une notification TABLE_ROW_MODIFIED pour la ligne qui correspond à la ligne décrite par le paramètre _lpSPropValue_ . **HrNotify** envoie la notification, que les modifications aient ou non été apportées à la ligne. Tous les clients et fournisseurs de services qui ont des vues de la table et qui ont appelé la méthode [IMAPITable:: conseille](imapitable-advise.md) de s'inscrire aux notifications sur leurs vues recevez cette notification. 
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

