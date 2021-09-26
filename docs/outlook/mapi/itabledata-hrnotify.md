---
title: ITableDataHrNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITableData.HrNotify
api_type:
- COM
ms.assetid: 98548b50-342e-434a-9ad3-c37ba418c5ce
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b89aef1aff41f7fd1f84d687c72d37ce306cc31e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610397"
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
  
> [in] Nombre de valeurs de propriété dans la structure [SPropValue](spropvalue.md) pointée par _le paramètre lpSPropValue._ 
    
 _lpSPropValue_
  
> [in] Pointeur vers une structure **SPropValue** qui décrit les valeurs des colonnes de la ligne cible. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

La **méthode ITableData::HrNotify** envoie une notification TABLE_ROW_MODIFIED pour la ligne qui correspond à la ligne décrite par les propriétés pointées par le paramètre _lpSPropValue._ **HrNotify envoie** la notification, que des modifications soient apportées à la ligne ou non. Tous les clients et fournisseurs de services qui ont des vues de la table et qui ont appelé [IMAPITable::Advise](imapitable-advise.md) pour s’inscrire aux notifications sur leurs vues reçoivent cette notification. 
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

